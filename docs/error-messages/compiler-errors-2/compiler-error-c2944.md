---
title: 컴파일러 오류 C2944 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2944
dev_langs:
- C++
helpviewer_keywords:
- C2944
ms.assetid: f209e668-e72f-442a-a438-8c4ff43a404a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: be9052ddc42c2f13e971c8655ac3382e3e1c89a7
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46083082"
---
# <a name="compiler-error-c2944"></a>컴파일러 오류 C2944

'class': type-class-id가 템플릿의 값 인수로 재정의되었습니다.

제네릭 또는 템플릿 클래스를 기호 대신 템플릿 값 인수로 사용할 수 없습니다.

다음 샘플에서는 C2944를 생성합니다.

```
// C2944.cpp
// compile with: /c
template<class T>
class TC { };

template <int TC<int> > struct X1 { };   // C2944

template <class T > struct X2 {};
```

C2944는 제네릭을 사용하는 경우에도 발생할 수 있습니다.

```
// C2944b.cpp
// compile with: /clr /c
generic<class T>
ref class GC {};

template <int GC<int> > struct X2 { };   // C2944
template <class T> struct X3 {};   // OK
```