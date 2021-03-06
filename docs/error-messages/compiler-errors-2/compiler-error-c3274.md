---
title: 컴파일러 오류 C3274 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3274
dev_langs:
- C++
helpviewer_keywords:
- C3274
ms.assetid: 1f03f18e-b569-48eb-9249-11c70122a305
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 424b6be69559932ac6f16dc83e39257e414a2120
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46088490"
---
# <a name="compiler-error-c3274"></a>컴파일러 오류 C3274

짝이 되는 try 없이 __finally/finally만 있습니다.

[__finally](../../cpp/try-finally-statement.md) 또는 [finally](../../dotnet/finally.md) 문이 일치하는 `try`없이 발견되었습니다. 이를 해결하려면 `__finally` 문을 삭제하거나 `try` 에 대해 `__finally`문을 추가합니다.

다음 샘플에서는 C3274를 생성합니다.

```
// C3274.cpp
// compile with: /clr
// C3274 expected
using namespace System;
int main() {
   try {
      try {
         throw gcnew ApplicationException();
      }
      catch(...) {
         Console::Error->WriteLine(L"Caught an exception");
      }
      finally {
         Console::WriteLine(L"In finally");
      }
   } finally {
      Console::WriteLine(L"In finally");
   }

   // Uncomment the following 3 lines to resolve.
   // try {
   //   throw gcnew ApplicationException();
   // }

   finally {
      Console::WriteLine(L"In finally");
   }
   Console::WriteLine(L"**FAIL**");
}
```