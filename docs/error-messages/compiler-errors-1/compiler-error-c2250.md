---
title: 컴파일러 오류 C2250 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2250
dev_langs:
- C++
helpviewer_keywords:
- C2250
ms.assetid: f990986f-5c7d-4af4-a25c-b35540f1e217
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: bee638b3e716460f54def3dc347810c874706708
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46070134"
---
# <a name="compiler-error-c2250"></a>컴파일러 오류 C2250

'identifier': 'class::member'의 상속이 모호

파생된 클래스는 둘 이상의 가상 기본 클래스의 가상 함수 재정의 상속합니다. 이러한 재정의 파생된 클래스에서 모호 합니다.

다음 샘플에서는 C2286을 생성합니다.

```
// C2250.cpp
// compile with: /c
// C2250 expected
struct V {
   virtual void vf();
};

struct A : virtual V {
   void vf();
};

struct B : virtual V {
   void vf();
};

struct D : A, B {
   // Uncomment the following line to resolve.
   // void vf();
};
```