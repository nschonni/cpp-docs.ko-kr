---
title: "컴파일러 오류 C2259 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2259
dev_langs:
- C++
helpviewer_keywords:
- C2259
ms.assetid: e458236f-bdea-4786-9aa6-a98d8bffa5f4
caps.latest.revision: 16
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
translationtype: Machine Translation
ms.sourcegitcommit: c243063a9770542f137d5950e8a269f771960f74
ms.openlocfilehash: 0837d8f5e48ccf0de0ba8630801667da2ddb6bfa
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-error-c2259"></a>컴파일러 오류 C2259
'class': 추상 클래스를 인스턴스화할 수 없습니다  
  
 코드는 추상 클래스 또는 구조체의 인스턴스를 선언합니다.  
  
 클래스 또는 구조체와 하나 이상의 순수 가상 함수를 인스턴스화할 수 없습니다. 파생된 클래스의 개체를 인스턴스화할 때 파생된 클래스는 각 순수 가상 함수를 재정의 해야 합니다.  
  
 자세한 내용은 참조 [암시적 추상 클래스](../../dotnet/how-to-define-and-consume-classes-and-structs-cpp-cli.md#BKMK_Implicitly_abstract_classes)합니다.  
  
 다음 샘플에서는 C2259 오류가 생성 됩니다.  
  
```  
// C2259.cpp  
// compile with: /c  
class V {  
public:  
   void virtual func() = 0;  
};  
class A : public V {};  
class B : public V {  
public:  
   void func();  
};  
V v;  // C2259, V is an abstract class  
A a;  // C2259, A inherits func() as pure virtual  
B b;  // OK, B defines func()  
```  
  
 인터페이스에서 파생 하 고 공용 액세스 권한 사용 하 여 파생된 클래스에서 인터페이스 메서드를 구현할 때마다 C2259 나타날 수 있습니다.  이 컴파일러는 공용 액세스 하려면 파생된 클래스에서 구현 된 인터페이스 메서드를 예상 하기 때문에 발생 합니다. 더 제한적인 액세스 권한 사용 하 여 인터페이스에 대 한 멤버 함수를 구현 하는 경우 컴파일러는 파생된 클래스는 추상 클래스 인터페이스에 정의 된 인터페이스 메서드에 대 한 구현으로 고려 하지 않습니다.  
  
 이 문제를 해결할 수 있는 방법은 두 가지가 있습니다.  
  
-   구현 된 메서드에 대 한 공용 액세스 권한을 확인 합니다.  
  
-   파생된 클래스에서 구현 된 인터페이스 메서드에 대 한 범위 확인 연산자를 사용 하 여 구현 된 메서드 이름을 인터페이스의 이름으로 한정 합니다.  
  
 Visual c + + 2005에서 수행 된 규칙 작업의 결과로 C2259도 발생할 수 있습니다 **/zc: wchar_t** 는 이제 기본적으로 설정 합니다. 이 경우 C2599 사용 하 여 컴파일하거나 확인 될 수 **/Zc:wchar_t-**, 이전 버전에서 컴파일하거나 호환 되도록 형식이 업데이트 하 여 동작을 활용할 수 있습니다. 자세한 내용은 [/Zc:wchar_t(wchar_t는 네이티브 형식임)](../../build/reference/zc-wchar-t-wchar-t-is-native-type.md)를 참조하세요.  
  
 다음 샘플에서는 C2259 오류가 생성 됩니다.  
  
```  
// C2259b.cpp  
// compile with: /c  
#include <windows.h>   
  
class MyClass {  
public:  
   // WCHAR now typedef'ed to wchar_t  
   virtual void func(WCHAR*) = 0;  
};  
  
class MyClass2 : MyClass {  
public:  
   void func(unsigned short*);  
};  
  
MyClass2 x;   // C2259  
  
// OK  
class MyClass3 {  
public:  
   virtual void func(WCHAR*) = 0;  
   virtual void func2(wchar_t*) = 0;  
   virtual void func3(unsigned short*) = 0;  
};  
  
class MyClass4 : MyClass3 {  
public:  
   void func(WCHAR*) {}  
   void func2(wchar_t*) {}  
   void func3(unsigned short*) {}  
};  
  
MyClass4 y;  
```  
  
 다음 샘플에서는 C2259 오류가 생성 됩니다.  
  
```  
// C2259c.cpp  
// compile with: /clr  
interface class MyInterface {  
   void MyMethod();  
};  
  
ref class MyDerivedClass: public MyInterface {  
private:  
   // Uncomment the following line to resolve.  
   // public:  
   void MyMethod(){}  
   // or the following line  
   // void MyInterface::MyMethod() {};  
};  
  
int main() {  
   MyDerivedClass^ instance = gcnew MyDerivedClass; // C2259  
}  
```  
