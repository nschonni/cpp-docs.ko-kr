---
title: 컴파일러 오류 C3623 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3623
dev_langs:
- C++
helpviewer_keywords:
- C3623
ms.assetid: a0341b45-062a-4f67-beb9-ba74201ed1ed
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 90198a3ea7cfb96b75717550b551c55915187211
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46085305"
---
# <a name="compiler-error-c3623"></a>컴파일러 오류 C3623

'variable': 관리되는 형식 또는 WinRT 형식에서는 비트 필드가 지원되지 않습니다.

'variable': 관리되는 클래스 또는 WinRT 클래스의 변수에서는 비트 필드를 사용할 수 없습니다.

다음 샘플에서는 C3623 오류가 발생하는 경우를 보여 줍니다.

```
// C3623.cpp
// compile with: /clr
using namespace System;
ref class CMyClass {
public:
   int i : 1;   // C3623
};

int main() {
   CMyClass^ pMyClass = gcnew CMyClass();
   pMyClass->i = 3;
   Console::Out->WriteLine(pMyClass->i);
}
```
