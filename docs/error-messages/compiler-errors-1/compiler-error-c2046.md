---
title: 컴파일러 오류 C2046 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2046
dev_langs:
- C++
helpviewer_keywords:
- C2046
ms.assetid: f0c8f9dd-dbd7-4c4a-8838-fde54208ec71
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4ee043be0a5b7f259f51082c5d48d77b77f0a6db
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46060072"
---
# <a name="compiler-error-c2046"></a>컴파일러 오류 C2046

대/소문자가 잘못되었습니다.

`case` 키워드는 `switch` 문에만 나타날 수 있습니다.

다음 샘플에서는 C2046을 생성합니다.

```
// C2046.cpp
int main() {
   case 0:   // C2046
}
```

해결 방법:

```
// C2046b.cpp
int main() {
   int i = 0;

   switch(i) {
      case 0:
      break;

      default:
      break;
   }
}
```