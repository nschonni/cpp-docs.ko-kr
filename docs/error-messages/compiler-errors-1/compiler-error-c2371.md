---
title: 컴파일러 오류 C2371 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2371
dev_langs:
- C++
helpviewer_keywords:
- C2371
ms.assetid: d383993d-05ef-4e35-8129-3b58a6f7b7b7
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e16cf4869b8f94408c09cc2f58e50d380c247091
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46041300"
---
# <a name="compiler-error-c2371"></a>컴파일러 오류 C2371

'identifier': 재정의. 기본 형식이 다릅니다.

식별자가 이미 선언되었습니다.

다음 샘플에서는 C2371을 생성합니다.

```
// C2371.cpp
int main() {
   int i;
   float i;   // C2371, redefinition
   float f;   // OK
}
```