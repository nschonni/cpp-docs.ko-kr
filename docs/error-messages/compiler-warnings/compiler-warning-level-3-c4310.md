---
title: 컴파일러 경고 (수준 3) C4310 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4310
dev_langs:
- C++
helpviewer_keywords:
- C4310
ms.assetid: cba3eca1-f1ed-499c-9243-337446bdbdd8
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 410db9aa1dee4c0a75b3e1df9d1b019cef736e34
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46039454"
---
# <a name="compiler-warning-level-3-c4310"></a>컴파일러 경고(수준 3) C4310

캐스트 상수 값을 자릅니다.

상수 값을 더 작은 형식으로 캐스팅 됩니다. 컴파일러에서 캐스트 데이터를 자릅니다를 수행 합니다. 다음 샘플에서는 C4310 오류가 생성 됩니다.

```
// C4310.cpp
// compile with: /W4
int main() {
   long int a;
   a = (char) 128;   // C4310, use value 0-127 to resolve
}
```