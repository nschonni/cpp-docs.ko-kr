---
title: 심각한 오류 C1103 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1103
dev_langs:
- C++
helpviewer_keywords:
- C1103
ms.assetid: 9d276939-9c47-4235-9d20-76b8434f9731
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d9e48d827c58ebf41ce3cf3862cbfbeaa494cf76
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46055951"
---
# <a name="fatal-error-c1103"></a>심각한 오류 C1103

progid를 가져오는 동안 심각한 오류가 발생했습니다. 'message'

컴파일러가 형식 라이브러리를 가져오는 동안 문제를 발견했습니다.  예를 들어 progid를 사용하여 형식 라이브러리를 지정하고 `no_registry`도 지정할 수는 없습니다.

자세한 내용은 [#import 지시문](../../preprocessor/hash-import-directive-cpp.md)합니다.

다음 샘플에서는 C1103을 생성합니다.

```
// C1103.cpp
#import "progid:a.b.id.1.5" no_registry auto_search   // C1103
```