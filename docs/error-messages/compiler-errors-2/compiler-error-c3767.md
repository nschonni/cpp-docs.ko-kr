---
title: 컴파일러 오류 C3767 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3767
dev_langs:
- C++
helpviewer_keywords:
- C3767
ms.assetid: 5247cdcd-639c-4527-bd37-37e74c4e8fab
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e4e5f73016060ccc17dfe0218d8b518b2f5dbdbd
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46081444"
---
# <a name="compiler-error-c3767"></a>컴파일러 오류 C3767

'function' 후보 함수에 액세스할 수 없습니다.

클래스에서 정의 된 friend 함수 정의 및 전역 네임 스페이스 범위에서 선언 된 것 처럼 간주 해서는 안 됩니다. 그러나 인수 종속 조회 하 여 찾을 수를 해당 수 있습니다.

C3767 때문일 수 있습니다도 주요 변경 내용: 네이티브 형식은 이제 기본적으로 개인을 **/clr** 컴파일; 참조 [가시성 입력](../../dotnet/how-to-define-and-consume-classes-and-structs-cpp-cli.md#BKMK_Type_visibility) 자세한 합니다.

## <a name="example"></a>예제

다음 샘플에서는 C3767를 생성합니다.

```
// C3767a.cpp
// compile with: /clr
using namespace System;
public delegate void TestDel();

public ref class MyClass {
public:
   static event TestDel^ MyClass_Event;
};

public ref class MyClass2 : public MyClass {
public:
   void Test() {
      MyClass^ patient = gcnew MyClass;
      patient->MyClass_Event();
    }
};

int main() {
   MyClass^ x = gcnew MyClass;
   x->MyClass_Event();   // C3767

   // OK
   MyClass2^ y = gcnew MyClass2();
   y->Test();
};
```

다음 샘플에서는 C3767를 생성합니다.

```
// C3767c.cpp
// compile with: /clr /c

ref class Base  {
protected:
   void Method() {
      System::Console::WriteLine("protected");
   }
};

ref class Der : public Base {
   void Method() {
      ((Base^)this)->Method();   // C3767
      // try the following line instead
      // Base::Method();
   }
};
```

