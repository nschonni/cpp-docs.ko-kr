---
title: 컴파일러 오류 C2135 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2135
dev_langs:
- C++
helpviewer_keywords:
- C2135
ms.assetid: aa360d22-4f79-4de1-b384-93cadd10975f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d4945753bec1ab8d315c8f8028bf10513dcb21c1
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46070071"
---
# <a name="compiler-error-c2135"></a>컴파일러 오류 C2135

'비트 연산자': 비트 필드 연산이 잘못되었습니다.

address-of 연산자(`&`)는 비트 필드에 적용할 수 없습니다.

다음 샘플에서는 C2135를 생성합니다.

```
// C2135.cpp
struct S {
   int i : 1;
};

struct T {
   int j;
};
int main() {
   &S::i;   // C2135 address of a bit field
   &T::j;   // OK
}
```