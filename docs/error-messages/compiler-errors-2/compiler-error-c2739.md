---
title: 컴파일러 오류 C2739 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2739
dev_langs:
- C++
helpviewer_keywords:
- C2739
ms.assetid: 5b63e435-7631-43d7-805e-f2adefb7e517
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b4e6c757823caa25bd9df890dce35035642e5212
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46046669"
---
# <a name="compiler-error-c2739"></a>컴파일러 오류 C2739

'number' : 관리되는 배열 또는 WinRT 배열의 명시적 차원은 1에서 32 사이여야 합니다.

배열 차원이 1에서 32 사이가 아니었습니다.

다음 샘플에서는 C2739 오류가 발생하는 경우 및 이를 해결하는 방법을 보여 줍니다.

```
// C2739.cpp
// compile with: /clr
int main() {
   array<int, -1>^a;   // C2739
   // try the following line instead
   // array<int, 2>^a;
}
```