---
title: 컴파일러 오류 C2911 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2911
dev_langs:
- C++
helpviewer_keywords:
- C2911
ms.assetid: 83c7c01a-ab6a-4179-9fb0-289a9ec8d44e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c242e72ab4f13f56644b9ab73c2a168e0591012d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46041183"
---
# <a name="compiler-error-c2911"></a>컴파일러 오류 C2911

'member': 현재 범위에서 선언하거나 정의할 수 없습니다.

네임스페이스, 클래스 또는 함수 내에서는 동일한 네임스페이스, 클래스 또는 함수의 멤버 또는 동일한 네임스페이스, 클래스 또는 함수로 묶인 멤버만 정의할 수 있습니다.

다음 샘플에서는 C2911을 생성합니다.

```
// C2911.cpp
struct A;

namespace M {
   struct D;
}

namespace N {
   struct C;

   namespace O {
      struct B;
   }

   // in N
   struct ::A {};   // C2911  A is member of global NS
   struct O::B{};   // OK B is in O, O is inside of N
   struct C {};     // OK C is member of N
   struct M::D {};  // C2911 D is member of M, M not enclosed by N
}
```