---
title: 컴파일러 경고 (수준 2) C4094 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4094
dev_langs:
- C++
helpviewer_keywords:
- C4094
ms.assetid: e68929fb-3a1c-4be7-920b-d5f79f534f99
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2b9317cbc31ef8bddb14da11af1087a148fd3188
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46078714"
---
# <a name="compiler-warning-level-2-c4094"></a>컴파일러 경고 (수준 2) C4094

태그가 지정 되지 않은 ' token' 기호가 없는 선언

컴파일러는 태그가 지정 되지 않은 구조체, 공용 구조체 또는 클래스를 사용 하 여 빈 선언을 발견 했습니다. 선언이 무시 됩니다.

## <a name="example"></a>예제

```
// C4094.cpp
// compile with: /W2
struct
{
};   // C4094

int main()
{
}
```

ANSI 호환성 오류를 생성 하는이 조건 ([/Za](../../build/reference/za-ze-disable-language-extensions.md)).