---
title: __noop | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __noop_cpp
- __noop
dev_langs:
- C++
helpviewer_keywords:
- __noop keyword [C++]
ms.assetid: 81ac6e97-7bf8-496b-b3c4-fd02837573e5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 97820367f0960925dfcac1db339260cd3f52b8bc
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46430217"
---
# <a name="noop"></a>__noop

**Microsoft 전용**

`__noop` 내장 함수를 무시 해야 함을 지정 및 인수 목록을 구문 분석할 수 있지만 코드가 없는 인수를 생성 합니다. 가변 개수의 인수를 사용 하는 전역 디버그 함수에서 사용할 것입니다.

컴파일러는 변환 된 `__noop` 컴파일 시간에 0으로 내장 함수입니다.

## <a name="example"></a>예제

다음 코드를 사용 하는 방법을 보여 줍니다. `__noop`합니다.

```
// compiler_intrinsics__noop.cpp
// compile with or without /DDEBUG
#include <stdio.h>

#if DEBUG
   #define PRINT   printf_s
#else
   #define PRINT   __noop
#endif

int main() {
   PRINT("\nhello\n");
}
```

## <a name="see-also"></a>참고 항목

[컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)<br/>
[키워드](../cpp/keywords-cpp.md)