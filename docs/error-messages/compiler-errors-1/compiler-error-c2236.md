---
title: 컴파일러 오류 C2236 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2236
dev_langs:
- C++
helpviewer_keywords:
- C2236
ms.assetid: 0b6771a7-a783-4729-9c3d-7a3339c432cc
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4fba2f795c3b786e82331a4b14f2c4530731db64
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46053702"
---
# <a name="compiler-error-c2236"></a>컴파일러 오류 C2236

예기치 않은 토큰 'identifier'입니다. ';'이 없습니다.

식별자가 이미 형식으로 정의되었으며 사용자 정의 형식으로 재정의할 수 없습니다.

다음 샘플에서는 C2236을 생성합니다.

```
// C2236.cpp
// compile with: /c
int class A {};  // C2236 "int class" is unexpected
int i;
class B {};
```