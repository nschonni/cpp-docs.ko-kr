---
title: 컴파일러 오류 C2881 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2881
dev_langs:
- C++
helpviewer_keywords:
- C2881
ms.assetid: b49c63c2-b064-4d4b-a75e-ddd2af947522
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a7f74a4336af3b8ce8bfe0fa87f7f1a84746ff11
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46052493"
---
# <a name="compiler-error-c2881"></a>컴파일러 오류 C2881

'namespace1': 이미 'namespace2'에 대 한 별칭으로 사용

두 개의 네임 스페이스에 대 한 별칭으로 동일한 이름을 사용할 수 없습니다.

다음 샘플에서는 C2881 오류가 생성 됩니다.

```
// C2881.cpp
// compile with: /c
namespace A {
   int k;
}

namespace B {
   int i;
}

namespace C = A;
namespace C = B;   // C2881 C is already an alias for A
```