---
title: 컴파일러 경고 (수준 1) C4717 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4717
dev_langs:
- C++
helpviewer_keywords:
- C4717
ms.assetid: 5ef3c6c7-8599-4714-a973-0f5b69cdab3c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e9bb7c37cd4a9da8844f30463c6e2d73fcc04609
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46022424"
---
# <a name="compiler-warning-level-1-c4717"></a>컴파일러 경고(수준 1) C4717

'function': 모든 제어 경로에서 재귀적 함수로 인해 런타임 스택 오버플로

함수를 통해 모든 경로 함수에 대 한 호출을 포함합니다. 자체는 먼저 호출 하지 않고 함수를 재귀적으로 종료 하는 방법이 이므로 함수 종료 되지 않습니다.

다음 샘플에서는 C4717 오류가 생성 됩니다.

```
// C4717.cpp
// compile with: /W1 /c
// C4717 expected
int func(int x) {
   if (x > 1)
      return func(x - 1); // recursive call
   else {
      int y = func(0) + 1; // recursive call
      return y;
   }
}

int main(){
   func(1);
}
```