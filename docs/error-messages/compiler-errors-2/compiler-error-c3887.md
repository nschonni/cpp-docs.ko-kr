---
title: 컴파일러 오류 C3887 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3887
dev_langs:
- C++
helpviewer_keywords:
- C3887
ms.assetid: a7e82426-ef99-437b-9562-2822004e18fe
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1238f648c7e5481127562d34dde193a278c3cf0f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46047631"
---
# <a name="compiler-error-c3887"></a>컴파일러 오류 C3887

'var': 리터럴 데이터 멤버에 대 한 이니셜라이저는 상수 식 이어야 합니다.

A [리터럴](../../windows/literal-cpp-component-extensions.md) 데이터 멤버는 상수 식만 초기화할 수 있습니다.

다음 샘플에서는 C3887 오류가 생성 됩니다.

```
// C3887.cpp
// compile with: /clr
ref struct Y1 {
   static int i = 9;
   literal
   int staticConst = i;   // C3887
};
```

해결 방법:

```
// C3887b.cpp
// compile with: /clr /c
ref struct Y1 {
   literal
   int staticConst = 9;
};
```