---
title: 컴파일러 오류 C3894 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3894
dev_langs:
- C++
helpviewer_keywords:
- C3894
ms.assetid: 6d5ac903-1dea-431d-8e3a-cebca4342983
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 373da78257ee0f5ce7307ab521cccb0297933240
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46080092"
---
# <a name="compiler-error-c3894"></a>컴파일러 오류 C3894

'var': 'class' 클래스의 클래스 생성자에서 에서만 initonly 정적 데이터 멤버 l-value가 사용할 수는

정적 [initonly](../../dotnet/initonly-cpp-cli.md) 데이터 멤버는 선언 또는 정적 생성자에서는 해당 지점에서 l-value로만 사용할 수 있습니다.

인스턴스 (비정적) initonly 데이터 멤버 또는 인스턴스 (비정적) 생성자 선언에 대 한 해당 지점에서 l-value로 사용할 수 있습니다.

다음 샘플에서는 C3894 오류가 생성 됩니다.

```
// C3894.cpp
// compile with: /clr
ref struct Y1 {
   initonly static int data_var = 0;

public:
   // class constructor
   static Y1() {
      data_var = 99;   // OK
      System::Console::WriteLine("in static constructor");
   }

   // not the class constructor
   Y1(int i) {
      data_var = i;   // C3894
   }

   static void Test() {}

};

int main() {
   Y1::data_var = 88;   // C3894
   int i = Y1::data_var;
   Y1 ^ MyY1 = gcnew Y1(99);
   Y1::Test();
}
```