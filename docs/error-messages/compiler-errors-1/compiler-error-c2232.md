---
title: 컴파일러 오류 C2232 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2232
dev_langs:
- C++
helpviewer_keywords:
- C2232
ms.assetid: 76f302b7-30a7-4a81-9a39-b4edde33b54c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c0e7c20de3de097fc09b80459e96158282ef7bba
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46026051"
---
# <a name="compiler-error-c2232"></a>컴파일러 오류 C2232

'->': 왼쪽된 피연산자 형식이 ' 클래스 키 '를 사용 하 여 '.'

`->` 연산자의 왼쪽에 있는 피연산자가 포인터가 아닙니다. 마침표 (.) 연산자를 사용 하 여 클래스, 구조체 또는 공용 구조체에 대 한 합니다.

다음 샘플에서는 C2232를 생성합니다.

```
// C2232.c
struct X {
    int member;
} x, *px;
int main() {
    x->member = 0;   // C2232, x is not a pointer

    px->member = 0;
    x.member = 0;
}
```