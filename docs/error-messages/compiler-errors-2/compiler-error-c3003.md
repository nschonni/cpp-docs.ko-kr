---
title: 컴파일러 오류 C3003 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3003
dev_langs:
- C++
helpviewer_keywords:
- C3003
ms.assetid: 22e74f99-bb7f-4518-ab0d-934d5d49bcc7
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 749199401e399a21b4b8c2c98532aa5449f2cce1
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46027884"
---
# <a name="compiler-error-c3003"></a>컴파일러 오류 C3003

'directive': 지시문 절 다음에는 OpenMP 지시문 이름이 올 수 없습니다.

OpenMP 지시문 이름이 OpenMP 지시문 절 다음에 올 수 없습니다.

다음 샘플에서는 C3003을 생성합니다.

```
// C3003.c
// compile with: /openmp
int main()
{
   int x, y, z;
   #pragma omp parallel shared(x, y, z) for   // C3003
}
```