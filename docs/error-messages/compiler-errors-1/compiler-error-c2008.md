---
title: 컴파일러 오류 C2008 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2008
dev_langs:
- C++
helpviewer_keywords:
- C2008
ms.assetid: e748ccbe-ffd4-4008-aca7-e53c25225209
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a00c2a55d7176beae88f7e5db3045722568bd293
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46051245"
---
# <a name="compiler-error-c2008"></a>컴파일러 오류 C2008

'character': 매크로 정의에 사용할 수 없습니다.

매크로 이름 바로 뒤에 문자가 표시 됩니다. 오류를 해결 하려면 매크로 이름 뒤에 오는 한 공간 이어야 합니다.

다음 샘플에서는 C2008을 생성합니다.

```
// C2008.cpp
#define TEST1"mytest1"    // C2008
```

해결 방법:

```
// C2008b.cpp
// compile with: /c
#define TEST2 "mytest2"
```