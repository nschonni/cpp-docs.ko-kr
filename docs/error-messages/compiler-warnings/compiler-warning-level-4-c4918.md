---
title: 컴파일러 경고 (수준 4) C4918 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4918
dev_langs:
- C++
helpviewer_keywords:
- C4918
ms.assetid: 1bcf6d35-3467-4aa8-b2ef-cb33f4e70238
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: cb4cc66359c28ffc23afa64da1e5bdbaadd8fb9b
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46023230"
---
# <a name="compiler-warning-level-4-c4918"></a>컴파일러 경고(수준 4) C4918

'character': pragma 최적화 목록에 잘못된 문자가 있습니다.

[optimize](../../preprocessor/optimize.md) pragma 문의 최적화 목록에 알 수 없는 문자가 있습니다.

예를 들어 다음 문은 C4918을 생성합니다.

```
// C4918.cpp
// compile with: /W4
#pragma optimize("X", on) // C4918 expected
int main()
{
}
```