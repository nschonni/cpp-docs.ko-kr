---
title: "함수 템플릿 호출의 오버로드 확인 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "함수 템플릿 오버로드 확인"
ms.assetid: a2918748-2cbb-4fc6-a176-e256f120bee4
caps.latest.revision: 11
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 9
---
# 함수 템플릿 호출의 오버로드 확인
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

함수 템플릿은 동일한 이름의 비템플릿 함수를 오버로드할 수 있습니다.  이 시나리오에서 함수 호출은 첫 번째 템플릿 인수 추론을 사용하여 고유한 특수화를 통해 함수 템플릿을 인스턴스화할 수 있습니다.  템플릿 인수 추론이 실패하는 경우 다른 함수 오버로드가 호출을 해결하기 위해 고려됩니다.  후보 집합이라고도 불리는 이러한 다른 오버로드는 비템플릿 함수와 다른 인스턴스화된 함수 템플릿을 포함합니다.  템플릿 인수 추론이 성공하는 경우 생성된 함수는 오버로드 확인 규칙에 따라 다른 함수와 비교하여 최상의 경우를 결정합니다.  자세한 내용은 [오버 로딩](../misc/overloading-cpp.md) 및 [인수 일치](../misc/argument-matching.md)를 참조하십시오.  
  
## 예제  
 비템플릿 함수가 템플릿 함수와 동일하게 일치하는 경우 다음 예제에서 템플릿 인수가 명시적으로 지정되지 않은 경우 비템플릿 함수가 호출 `f(1, 1)`로써 선택됩니다.  
  
```  
// template_name_resolution9.cpp  
// compile with: /EHsc  
#include <iostream>  
using namespace std;  
  
void f(int, int) { cout << "f(int, int)" << endl; }  
void f(char, char) { cout << "f(char, char)" << endl; }  
  
template <class T1, class T2>  
void f(T1, T2)  
{  
   cout << "void f(T1, T2)" << endl;  
};  
  
int main()  
{  
   f(1, 1);   // Equally good match; choose the nontemplate function.  
   f('a', 1); // Chooses the template function.  
   f<int, int>(2, 2);  // Template arguments explicitly specified.  
}  
```  
  
  **f\(int, int\)**  
**void f\(T1, T2\)**  
**void f\(T1, T2\)**   
## 예제  
 다음 예제는 비템플릿 함수를 변환해야 하는 경우 정확하게 일치하는 템플릿 함수가 선호됨을 보여 줍니다.  
  
```  
// template_name_resolution10.cpp  
// compile with: /EHsc  
#include <iostream>  
using namespace std;  
  
void f(int, int) { cout << "f(int, int)" << endl; }  
  
template <class T1, class T2>  
void f(T1, T2)  
{  
   cout << "void f(T1, T2)" << endl;  
};  
  
int main()  
{  
   long l = 0;  
   int i = 0;  
   // Call the template function f(long, int) because f(int, int)  
   // would require a conversion from long to int.  
   f(l, i);  
}  
```  
  
  **void f\(T1, T2\)**   
## 참고 항목  
 [이름 확인](../cpp/templates-and-name-resolution.md)   
 [typename](../cpp/typename.md)   
 [템플릿 인수 추론](../Topic/Template%20Argument%20Deduction.md)