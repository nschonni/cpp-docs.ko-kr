---
title: 컴파일러 오류 C2908 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2908
dev_langs:
- C++
helpviewer_keywords:
- C2908
ms.assetid: 49cd2a21-cad8-4ba0-9a0b-3a0190d9344c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 913a01a21c75933688c55bbb79c3621124601745
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46053117"
---
# <a name="compiler-error-c2908"></a>컴파일러 오류 C2908

명시적 특수화 이미 인스턴스화된 'template'

기본 템플릿의 특수화는 명시적 특수화는 그것이 전에 발생합니다.

다음 샘플에서는 C2908를 생성합니다.

```
// C2908.cpp
// compile with: /c
template<class T> class X {};

void f() {
X<int> x;   //specialization and instantiation
            //of X<int>
}

template<> class X<int> {}  // C2908, explicit specialization
```