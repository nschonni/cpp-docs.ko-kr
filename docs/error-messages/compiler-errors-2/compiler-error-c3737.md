---
title: 컴파일러 오류 C3737 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3737
dev_langs:
- C++
helpviewer_keywords:
- C3737
ms.assetid: ca2aeb23-2491-4ccb-8838-884abf7065c8
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 99ab9394f2c475079ee226dd294cca346ec68e32
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46039259"
---
# <a name="compiler-error-c3737"></a>컴파일러 오류 C3737

'delegate': 대리자에서 명시적 호출 규칙에 없을 수 있습니다

지정할 수 없습니다는 [호출 규칙이](../../cpp/calling-conventions.md) 에 대 한는 `delegate`합니다.

## <a name="example"></a>예제

다음 샘플에서는 C3737 오류가 생성 됩니다.

```
// C3737a.cpp
// compile with: /clr
delegate void __stdcall MyFunc();   // C3737
// Try the following line instead.
// delegate void MyFunc();

int main() {
}
```
