---
title: 컴파일러 경고 (수준 4) C4254 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- c4254
dev_langs:
- C++
helpviewer_keywords:
- C4254
ms.assetid: c7dcef24-d535-4c98-bb41-fc3d2b88fd11
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 039ce69f624fdcdd6beba2d6d262f920b7848687
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46115939"
---
# <a name="compiler-warning-level-4-c4254"></a>컴파일러 경고(수준 4) C4254

'operator': 'type1'에서 'type2', 데이터 손실으로 변환

큰 비트 필드를 더 작은 비트 필드에 할당 되었습니다. 데이터 손실이 있을 수 있습니다.

기본적으로 이 경고는 해제되어 있습니다. 자세한 내용은 [기본적으로 해제되어 있는 컴파일러 경고](../../preprocessor/compiler-warnings-that-are-off-by-default.md) 를 참조하세요.

다음 샘플에서는 C4254 오류가 생성 됩니다.

```
// C4254.cpp
// compile with: /W4
#pragma warning(default: 4254)

struct X {
   int a : 20;
   int b : 12;
};

int main() {
   X *x = new X();
   x->b = 10;
   x->a = 4;
   x->a = x->b;    // OK
   x->b = x->a;    // C4254
};
```