---
title: 컴파일러 경고 (수준 4) C4125 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4125
dev_langs:
- C++
helpviewer_keywords:
- C4125
ms.assetid: a081d1f4-0789-4915-91df-7ff0b28ca245
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7042dd8689bf5a9bafc35d6bdaa6028f0c52df2a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46087242"
---
# <a name="compiler-warning-level-4-c4125"></a>컴파일러 경고(수준 4) C4125

10진수가 8진수 이스케이프 시퀀스를 마칩니다.

컴파일러가 10진수 없는 8진수를 계산하고 10진수를 문자로 가정합니다.

## <a name="example"></a>예제

```
// C4125a.cpp
// compile with: /W4
char array1[] = "\709"; // C4125
int main()
{
}
```

숫자 9가 문자로 사용된 경우 예제를 다음과 같이 수정합니다.

```
// C4125b.cpp
// compile with: /W4
char array[] = "\0709";  // C4125 String containing "89"
int main()
{
}
```