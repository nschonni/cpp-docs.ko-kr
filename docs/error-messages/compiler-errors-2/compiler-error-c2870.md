---
title: 컴파일러 오류 C2870 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2870
dev_langs:
- C++
helpviewer_keywords:
- C2870
ms.assetid: 80523ee9-1fd3-4dc4-8a77-5083deb99066
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 47101cbc2fb1be48ba54166b9c6ef99fc0c6c35e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46073878"
---
# <a name="compiler-error-c2870"></a>컴파일러 오류 C2870

'name': 네임 스페이스 정의 다른 네임 스페이스 정의 내에서 파일 범위 또는 즉시 나타나야 합니다.

네임 스페이스를 정의한 `name` 잘못 됩니다. (모든 블록 및 클래스) 외부 파일 범위에서 네임 스페이스를 정의 해야 합니다 또는 다른 네임 스페이스 내에서 바로.

다음 샘플에서는 C2870 오류가 생성 됩니다.

```
// C2870.cpp
// compile with: /c
int main() {
   namespace A { int i; };   // C2870
}
```