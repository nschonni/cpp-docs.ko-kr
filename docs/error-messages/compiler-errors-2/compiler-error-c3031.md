---
title: 컴파일러 오류 C3031 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3031
dev_langs:
- C++
helpviewer_keywords:
- C3031
ms.assetid: 7e621e7e-eda7-45b5-8836-29599cd05255
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1e604e6d15e0f7d336b2e439c80f7150d4d88510
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46054664"
---
# <a name="compiler-error-c3031"></a>컴파일러 오류 C3031

'var': 'reduction' 절의 변수는 스칼라 산술 형식이어야 합니다.

잘못된 형식의 변수가 reduction 절에 전달되었습니다.

다음 샘플에서는 C3031을 생성합니다.

```
// C3031.cpp
// compile with: /openmp /link vcomps.lib
#include <stdio.h>
#include "omp.h"

typedef struct {
   int n;
} Incomplete;

extern Incomplete inc;
int i = 9;

int main() {
   #pragma omp parallel reduction(+: inc)   // C3031
      ;

   #pragma omp parallel reduction(+: i)     // OK
      ;
}
```