---
title: 컴파일러 오류 C3232 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3232
dev_langs:
- C++
helpviewer_keywords:
- C3232
ms.assetid: 3119b3a9-0eff-4a3f-b805-e4d160af9e39
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7e7b3e8c306b8e883fd3edb0b2781b297842bb0a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46018368"
---
# <a name="compiler-error-c3232"></a>컴파일러 오류 C3232

'param': 정규화된 이름에는 제네릭 형식 매개 변수를 사용할 수 없습니다.

제네릭 형식 매개 변수가 잘못 사용되었습니다.

다음 샘플에서는 C3232를 생성합니다.

```
// C3232.cpp
// compile with: /clr
generic <class T>
ref class C {
   typename T::TYPE t;   // C3232
};
```