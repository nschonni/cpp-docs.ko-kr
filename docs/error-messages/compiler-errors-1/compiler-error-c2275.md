---
title: 컴파일러 오류 C2275 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2275
dev_langs:
- C++
helpviewer_keywords:
- C2275
ms.assetid: c1eafa71-48de-46e0-82f3-b575538ef205
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: deedbf10edd3d9fd870dfbb1a896e504bfe9d877
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46052366"
---
# <a name="compiler-error-c2275"></a>컴파일러 오류 C2275

'identifier':이 형식 식으로 잘못 사용

식을 사용 하는 `->` 연산자는 `typedef` 식별자입니다.

다음 샘플에서는 C2275 오류가 생성 됩니다.

```
// C2275.cpp
typedef struct S {
    int mem;
} *S_t;
void func1( int *parm );
void func2() {
    func1( &S_t->mem );   // C2275, S_t is a typedef
}
```