---
title: 컴파일러 오류 C2287 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2287
dev_langs:
- C++
helpviewer_keywords:
- C2287
ms.assetid: 64556299-4e1f-4437-88b7-2464fc0b95bb
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3a57d2738ba55d4964274c3c25038b8ebf248b24
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46072578"
---
# <a name="compiler-error-c2287"></a>컴파일러 오류 C2287

'class': 상속 표현: 'representation1' 필수 'representation2' 보다 덜 일반적은

클래스는 필요한 것 보다 더 간단한 표현으로 선언 됩니다.

다음 샘플에서는 C2287 오류가 생성 됩니다.

```
// C2287.cpp
// compile with: /vmg /c
class __single_inheritance X;
class __single_inheritance Y;

struct A { };
struct B { };
struct X : A, B { };  // C2287  X uses multiple inheritance
struct Y : A { };  // OK
```