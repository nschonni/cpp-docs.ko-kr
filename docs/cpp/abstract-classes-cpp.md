---
title: "추상 클래스 (C++) | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "추상 클래스"
  - "기본 클래스, 추상 클래스"
  - "클래스[C++], abstract"
  - "파생 클래스, 추상 클래스"
ms.assetid: f0c5975b-39de-4d68-9640-6ce57f4632e6
caps.latest.revision: 7
caps.handback.revision: 7
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# 추상 클래스 (C++)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

추상 클래스는 보다 구체적인 클래스가 파생될 수 있는 일반 개념의 식 역할을 합니다.  추상 클래스 형식의 개체를 만들 수는 없지만, 추상 클래스 형식에 대한 포인터와 참조를 사용할 수 있습니다.  
  
 순수 가상 함수가 하나 이상 포함된 클래스는 추상 클래스로 간주됩니다.  추상 클래스에서 파생 클래스는 순수 가상 함수를 구현해야 합니다. 이렇게 하지 않으면 파생 클래스도 추상 클래스가 됩니다.  
  
 가상 함수는 *pure\-specifier* 구문을 사용하여 "순수" 함수로 선언됩니다\([클래스 프로토콜 구현](http://msdn.microsoft.com/ko-kr/a319f1b3-05e8-400e-950a-1ca6eb105ab5) 참조\).  [가상 함수](../cpp/virtual-functions.md)에 소개된 예제를 살펴보세요.  `Account` 클래스의 용도는 일반적인 기능을 제공하는 것이지만, `Account` 형식의 개체는 너무 일반적이어서 유용하게 사용하기가 어렵습니다.  따라서 `Account`는 적합한 추상 클래스 후보입니다.  
  
```  
// deriv_AbstractClasses.cpp  
// compile with: /LD  
class Account {  
public:  
   Account( double d );   // Constructor.  
   virtual double GetBalance();   // Obtain balance.  
   virtual void PrintBalance() = 0;   // Pure virtual function.  
private:  
    double _balance;  
};  
  
```  
  
 이 선언과 이전 선언의 유일한 차이점은 `PrintBalance`가 순수 지정자\(`= 0`\)를 사용하여 선언되었다는 것입니다.  
  
## 추상 클래스에 대한 제한  
 추상 클래스는 다음 용도로 사용할 수 없습니다.  
  
-   변수 또는 멤버 데이터  
  
-   인수 형식  
  
-   함수 반환 형식  
  
-   명시적 변환 형식  
  
 또 다른 제한 사항은 추상 클래스에 대한 생성자가 직\/간접적으로 순수 가상 함수를 호출하는 경우 결과가 정의되지 않는다는 것입니다.  하지만 추상 클래스의 생성자 및 소멸자는 다른 멤버 함수를 호출할 수 있습니다.  
  
 순수 가상 함수에 대한 추상 클래스를 정의할 수 있지만 직접 호출하려면 반드시 다음의 구문을 사용해야 합니다.  
  
 *abstract\-class\-name* `::` *function\-name***\( \)**  
  
 개체를 소멸시키는 과정에서 기본 클래스 소멸자가 항상 호출되기 때문에 기본 클래스가 순수 가상 소멸자를 포함하는 클래스 계층 구조를 설계할 때 도움이 됩니다.  다음 예제를 참조하세요.  
  
```  
// Declare an abstract base class with a pure virtual destructor.  
// deriv_RestrictionsonUsingAbstractClasses.cpp  
class base {  
public:  
    base() {}  
    virtual ~base()=0;  
};  
  
// Provide a definition for destructor.  
base::~base() {}  
  
class derived:public base {  
public:  
    derived() {}  
    ~derived(){}  
};  
  
int main() {  
    derived *pDerived = new derived;  
    delete pDerived;  
}  
```  
  
 `pDerived`가 가리키는 개체가 소멸하면, 클래스 소멸자인 `derived`가 호출된 다음 클래스 소멸자, `base`가 호출됩니다.  순수 가상 함수에 비어 있는 구현을 사용하면 해당 함수에 대해 최소한의 구현이 존재하게 됩니다.  
  
> [!NOTE]
>  앞의 예제에서 순수 가상 함수인 `base::~base`는 `derived::~derived`에서 암시적으로 호출됩니다.  명시적으로 전체 정규화된 멤버 함수 이름을 사용하여 순수 가상 함수를 호출할 수도 있습니다.  
  
## 참고 항목  
 [상속](../cpp/inheritance-cpp.md)