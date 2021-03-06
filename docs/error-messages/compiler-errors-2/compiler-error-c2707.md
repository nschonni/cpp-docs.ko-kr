---
title: 컴파일러 오류 C2707 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2707
dev_langs:
- C++
helpviewer_keywords:
- C2707
ms.assetid: 3deaf45c-74da-4c9d-acc6-b82412720b74
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a8a9709b4bd6c66ec303ad61e2000ddc97976e87
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46107262"
---
# <a name="compiler-error-c2707"></a>컴파일러 오류 C2707

'identifier': 내장 함수의 컨텍스트가 잘못 되었습니다

구조적된 예외 처리 내장 함수는 특정 컨텍스트에서 유효 하지 않습니다.

- `_exception_code()` 예외 필터 외부 또는 `__except` 블록

- `_exception_info()` 예외 필터 외부

- `_abnormal_termination()` 외부는 `__finally` 블록

이 오류를 해결 하려면 예외 처리 내장 함수는 적절 한 컨텍스트에 배치 되도록 해야 합니다.

## <a name="example"></a>예제

다음 샘플에서는 C2707 오류가 발생 합니다.

```
// C2707.cpp
#include <windows.h>
#include <stdio.h>

LONG MyFilter(LONG excode)
{
    return (excode == EXCEPTION_ACCESS_VIOLATION ?
        EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH);   // OK
}

LONG func(void)
{
    int x, y;
    return(GetExceptionCode() == EXCEPTION_ACCESS_VIOLATION ?  // C2707
             EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH);

    __try
    {
        y = 0;
        x = 4 / y;
        return 0;
     }

    __except(MyFilter(GetExceptionCode()))
    {
        return(GetExceptionCode() == EXCEPTION_ACCESS_VIOLATION ? // ok
               EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH);
    }
}

int main()
{
    __try
    {
        func();
    } __except(EXCEPTION_EXECUTE_HANDLER)
    {
        printf_s("Caught exception\n");
    }
}
```