---
title: 컴파일러 오류 C2327 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2327
dev_langs:
- C++
helpviewer_keywords:
- C2327
ms.assetid: 95278c95-d1f9-4487-ad27-53311f5e8112
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4d8b5b0172d73ab76eb9500dddc6dfe264064ccd
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46097954"
---
# <a name="compiler-error-c2327"></a>컴파일러 오류 C2327

'symbol': 형식 이름, 정적 또는 열거자가 아닙니다

중첩된 된 클래스 내의 코드는 없거나 형식 이름, 정적 멤버를 열거자는 바깥쪽 클래스의 멤버에 액세스 하려고 합니다.

사용 하 여 컴파일하면 **/clr**, C2327 일반적으로 속성 형식으로 동일한 이름 가진 속성입니다.

다음 샘플에서는 C2327를 생성합니다.

```
// C2327.cpp
int x;
class enclose {
public:
   int x;
   static int s;
   class inner {
      void f() {
         x = 1;   // C2327; enclose::x is not static
         s = 1;   // ok; enclose::s is static
         ::x = 1;   // ok; ::x refers to global
      }
   };
};
```

C2327은 이름을 형식 멤버의 이름으로 숨겨진 경우에 발생할 수 있습니다.

```
// C2327b.cpp
class X {};

class S {
   X X;
   // try the following line instead
   // X MyX;
   X other;   // C2327, rename member X
};
```

C2327 매개 변수의 데이터 형식을 완전히 지정 해야 하는이 이런 경우에 발생할 수도 있습니다.

```
// C2327c.cpp
// compile with: /c
struct A {};

struct B {
   int A;
   void f(A a) {   // C2327
   void f2(struct A a) {}   // OK
   }
};
```

다음 샘플에서는 C2327를 생성합니다.

```
// C2327d.cpp
// compile with: /clr /c
using namespace System;

namespace NA {
   public enum class E : Int32 {
      one = 1,
      two = 2,
      three = 3
   };

   public ref class A {
   private:
      E m_e;
   public:
      property E E {
         NA::E get() {
            return m_e;
         }
         // At set, compiler doesn't know whether E is get_E or
         // Enum E, therefore fully qualifying Enum E is necessary
         void set( E e ) {   // C2327
            // try the following line instead
            // void set(NA::E e) {
            m_e = e;
         }
      }
   };
}
```

다음 샘플에서는 속성 이름이 같은 속성 형식으로 하는 경우 C2327를 보여 줍니다.

```
// C2327f.cpp
// compile with: /clr /c
public value class Address {};

public ref class Person {
public:
   property Address Address {
      ::Address get() {
         return address;
      }
      void set(Address addr) {   // C2327
      // try the following line instead
      // set(::Address addr) {
         address = addr;
      }
   }
private:
   Address address;   // C2327
   // try the following line instead
   // ::Address address;
};
```
