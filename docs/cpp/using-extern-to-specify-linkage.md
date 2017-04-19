---
title: "extern을 사용하여 링크 지정 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
f1_keywords: 
  - "extern"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "선언, 외부"
  - "extern 키워드[C++], 비C++ 함수에 대한 링크"
  - "외부 링크, extern 한정자"
ms.assetid: 1e2f0ae3-ae98-4410-85b5-222d6abc865a
caps.latest.revision: 11
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 11
---
# extern을 사용하여 링크 지정
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

## 구문  
  
```  
  
        extern string-literal { declaration-list }  
extern string-literal declaration  
```  
  
## 설명  
 `extern` 키워드는 변수 또는 함수를 선언하며 외부 링크를 포함하도록 지정합니다. 외부 링크의 이름은 해당 링크가 정의된 파일이 아닌 다른 파일에 표시됩니다.  `extern`은 변수를 한정할 때 변수에 정적 지속 기간을 지정합니다. 정적 지속 기간은 프로그램 시작 시 할당되고 프로그램 종료 시 할당 해제됩니다.  변수 또는 함수는 다른 소스 파일에서 정의하거나 나중에 같은 파일에서 정의할 수 있습니다.  파일 범위의 변수 및 함수는 기본적으로 외부에서 선언됩니다.  
  
## 예제  
  
```  
// specifying_linkage1.cpp  
int i = 1;  
void other();  
  
int main() {  
   // Reference to i, defined above:  
   extern int i;  
}  
  
void other() {  
   // Address of global i assigned to pointer variable:  
   static int *external_i = &i;  
  
   // i will be redefined; global i no longer visible:  
   // int i = 16;  
}  
```  
  
 C\+\+에서 `extern`을 문자열과 함께 사용하면 다른 언어의 링크 규칙이 선언자에 대해 사용 중임을 지정합니다.  C 함수 및 데이터는 이전에 C 링크가 있는 것으로 선언된 경우에만 액세스할 수 있습니다.  단, 별도로 컴파일된 변환 단위로 정의되어야 합니다.  
  
 Microsoft C\+\+는 문자열 리터럴 필드에서 문자열 **"C"** 및 *"C\+\+"*를 지원합니다.  모든 표준 include 파일은 `extern` "C" 구문을 사용하여 C\+\+ 프로그램에 사용할 런타임 라이브러리 함수를 허용합니다.  
  
## 예제  
 다음 예제에서는 C 링크가 있는 이름을 선언하는 또 다른 방법을 보여 줍니다.  
  
```  
// specifying_linkage2.cpp  
// compile with: /c  
// Declare printf with C linkage.  
extern "C" int printf( const char *fmt, ... );  
  
//  Cause everything in the specified header files  
//   to have C linkage.  
extern "C" {  
   // add your #include statements here  
   #include <stdio.h>  
}  
  
//  Declare the two functions ShowChar and GetChar  
//   with C linkage.  
extern "C" {  
   char ShowChar( char ch );  
   char GetChar( void );  
}  
  
//  Define the two functions ShowChar and GetChar  
//   with C linkage.  
extern "C" char ShowChar( char ch ) {  
   putchar( ch );  
   return ch;  
}  
  
extern "C" char GetChar( void ) {  
   char ch;  
  
   ch = getchar();  
   return ch;  
}  
  
// Declare a global variable, errno, with C linkage.  
extern "C" int errno;  
```  
  
 함수에 둘 이상의 링크 사양이 있는 경우 두 사양은 일치해야 합니다. C 및 C\+\+ 링크가 둘 다 있는 것으로 함수를 선언하면 오류가 발생합니다.  뿐만 아니라 함수에 대한 두 선언\(링크 사양이 있는 선언과 없는 선언\)이 프로그램에서 발생할 경우 링크 사양이 있는 선언이 첫 번째여야 합니다.  이미 링크 사양이 있는 함수의 모든 중복 선언에는 첫 번째 선언에서 지정된 링크가 제공됩니다.  예:  
  
```  
extern "C" int CFunc1();  
...  
int CFunc1();            // Redeclaration is benign; C linkage is  
                         //  retained.  
  
int CFunc2();  
...  
extern "C" int CFunc2(); // Error: not the first declaration of  
                         //  CFunc2;  cannot contain linkage  
                         //  specifier.  
```  
  
 복합 링크 지정자\(**{ }**\)의 본문 내에서 **static**으로 명시적으로 선언된 함수와 개체는 정적 함수 또는 개체로 취급되며 링크 지정자는 무시됩니다.  다른 함수와 개체는 `extern` 키워드를 사용하여 선언된 것처럼 동작합니다.  [extern을 사용하여 링크 지정](../cpp/using-extern-to-specify-linkage.md) 키워드에 대한 자세한 내용은 `extern` 을 참조하십시오.  
  
## 참고 항목  
 [C\+\+ 키워드](../cpp/keywords-cpp.md)   
 [\(NOTINBUILD\)Linkage Specifications](http://msdn.microsoft.com/ko-kr/d2b0cff1-7798-4c38-9ac8-61c3bfe2bfb9)   
 [extern 저장소 클래스 지정자](../c-language/extern-storage-class-specifier.md)   
 [식별자 동작](../c-language/behavior-of-identifiers.md)   
 [링크](../c-language/linkage.md)