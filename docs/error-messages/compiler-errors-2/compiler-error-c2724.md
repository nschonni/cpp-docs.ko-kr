---
title: 컴파일러 오류 C2724 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2724
dev_langs:
- C++
helpviewer_keywords:
- C2724
ms.assetid: 4e4664bc-8c96-4156-b79f-03436f532ea8
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d637892a71f9a2c9bafdced6cb3a6e51e23ae463
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46029340"
---
# <a name="compiler-error-c2724"></a>컴파일러 오류 C2724

'identifier': 'static' 해서는 안 파일 범위에서 정의 된 멤버 함수에서

외부 링크가 있는 정적 멤버 함수를 선언 해야 합니다.

다음 샘플에서는 C2724를 생성합니다.

```
// C2724.cpp
class C {
   static void func();
};

static void C::func(){};   // C2724
// try the following line instead
// void C::func(){};
```