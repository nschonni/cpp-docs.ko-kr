---
title: 컴파일러 경고 (수준 3) C4995 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4995
dev_langs:
- C++
helpviewer_keywords:
- C4995
ms.assetid: c6b61755-4730-4947-ad4d-d1c2bc82585a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c5ae389fef72681c6a8b31c9790c6773535f467d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46053481"
---
# <a name="compiler-warning-level-3-c4995"></a>컴파일러 경고 (수준 3) C4995

'function': 사용 되지 않는 #pragma로 표시 되어 이름

컴파일러가 pragma를 사용 하 여 표시 된 함수를 발견 했습니다 [사용 되지 않는](../../preprocessor/deprecated-c-cpp.md)합니다. 이 함수는 이후 릴리스에서 제공되지 않을 수 있습니다. 이 경고를 사용 하 여 해제 해제할 수 있습니다 합니다 [경고](../../preprocessor/warning.md) pragma (아래 예제).

## <a name="example"></a>예제

다음 샘플에서는 C4995 오류가 생성 됩니다.

```
// C4995.cpp
// compile with: /W3
#include <stdio.h>

// #pragma warning(disable : 4995)
void func1(void)
{
    printf("\nIn func1");
}

int main()
{
    func1();
    #pragma deprecated(func1)
    func1();   // C4995
}
```