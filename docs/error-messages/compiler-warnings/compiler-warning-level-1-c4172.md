---
title: 컴파일러 경고 (수준 1) C4172 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4172
dev_langs:
- C++
helpviewer_keywords:
- C4172
ms.assetid: a8d2bf65-d8b1-4fe3-8340-a223d7e7fde6
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 56f606b48fb060472dd67d34800c06946bc41712
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46043510"
---
# <a name="compiler-warning-level-1-c4172"></a>컴파일러 경고 (수준 1) C4172

지역 변수 또는 임시 주소를 반환합니다.

함수 지역 변수 또는 임시 개체의 주소를 반환 합니다. 지역 변수 및 임시 개체는 소멸 함수는 반환 될 때 반환 하는 주소는 잘못.

로컬 개체의 주소를 반환 하지 않는 되도록 함수를 다시 디자인 합니다.

다음 샘플에서는 C4172 오류가 생성 됩니다.

```
// C4172.cpp
// compile with: /W1 /LD
float f = 10;

const double& bar() {
// try the following line instead
// const float& bar() {
   return f;   // C4172
}
```