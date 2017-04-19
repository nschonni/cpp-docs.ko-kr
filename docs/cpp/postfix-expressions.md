---
title: "후위 식 | Microsoft Docs"
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
  - "식[C++], 후위"
  - "연산자[C++], 후위"
  - "후위 식"
ms.assetid: 7ac62a57-06df-422f-b012-a75b37d7cb9b
caps.latest.revision: 8
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 8
---
# 후위 식
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

후위 식은 기본 식 또는 후위 연산자가 기본 식 뒤에 오는 식으로 구성됩니다.  다음 표에서는 후위 연산자를 보여 줍니다.  
  
### 후위 연산자  
  
|연산자 이름|연산자 표기법|  
|------------|-------------|  
|[첨자 연산자](../cpp/subscript-operator.md)|**\[ \]**|  
|[함수 호출 연산자](../cpp/function-call-operator-parens.md)|**\( \)**|  
|[명시적 형식 변환 연산자](../cpp/explicit-type-conversion-operator-parens.md)|*type\-name* **\( \)**|  
|[멤버 액세스 연산자](../cpp/member-access-operators-dot-and.md)|**.** 또는 **–\>**|  
|[후위 증가 연산자](../cpp/postfix-increment-and-decrement-operators-increment-and-decrement.md)|`++`|  
|[후위 감소 연산자](../cpp/postfix-increment-and-decrement-operators-increment-and-decrement.md)|**––**|  
  
 다음 구문에서는 가능한 후위 식을 설명합니다.  
  
```  
  
          primary-expression   
postfix-expression [ expression ]  
postfix-expression ( expression-list)  
simple-type-name ( expression-list)  
postfix-expression . name  
postfix-expression –> name  
postfix-expression ++  
postfix-expression ––  
cast-keyword < typename > (expression ) typeid ( typename )  
```  
  
 위에서 *postfix\-expression*은 기본 식 또는 다른 후위 식일 수 있습니다.  **기본 식**을 참조하세요.  후위 식은 왼쪽에서 오른쪽까지 그룹화되므로 식이 다음과 같이 연결될 수 있습니다.  
  
```  
func(1)->GetValue()++  
```  
  
 위 식에서 func는 기본 식, func\(1\)은 함수 후위 식, func\(1\)\-\>GetData는 클래스 멤버를 지정하는 후위 식, func\(1\)\-\>GetData\(\)는 또 다른 함수 후위 식이며, 전체 식은 GetData의 반환 값을 증가시키는 후위 식입니다.  이 식은 1을 인수로 전달하는 함수를 호출하거나 클래스의 포인터를 반환 값으로 가져오라는 의미입니다.  그다음에 해당 클래스에서 GetValue\(\)를 호출하고 반환되는 값을 증가시킵니다.  
  
 위에 나열된 식은 할당 식입니다. 이는 이 식의 결과가 r\-value여야 한다는 의미입니다.  
  
 후위 식 형식  
  
```  
simple-type-name ( expression-list )  
```  
  
 생성자의 호출을 나타냅니다.  simple\-type\-name이 기본 형식인 경우 식 목록은 단일 식이어야 하며 이 식은 식 값의 기본 형식으로의 캐스트를 나타냅니다.  이 형식의 캐스트 식은 생성자를 모방합니다.  이 형식을 사용하면 기본 형식 및 클래스를 같은 구문을 사용하여 생성할 수 있기 때문에 이 형식은 특히 템플릿 클래스를 정의할 때 유용합니다.  
  
 *cast\-keyword*는 `dynamic_cast`, `static_cast` 또는 `reinterpret_cast` 중 하나입니다.  자세한 정보는 **dynamic\_cast**, **static\_cast** 및 **reinterpet\_cast**에서 찾을 수 있습니다.  
  
 `typeid` 연산자는 후위 식으로 간주됩니다.  **typeid 연산자**를 참조하세요.  
  
## 형식 및 실제 인수  
 호출하는 프로그램은 "실제 인수"에서 호출되는 함수에 정보를 전달합니다. 호출되는 함수는 해당하는 "형식 인수"를 사용하여 정보에 액세스합니다.  
  
 함수가 호출되면 다음 작업이 수행됩니다.  
  
-   모든 실제 인수\(호출자가 제공한 인수\)가 계산됩니다.  이 인수가 계산되는 암시적 순서는 없지만 함수에 진입하기 전에 인수가 모두 계산되고 의도하지 않은 결과가 모두 완료됩니다.  
  
-   식 목록에서 해당하는 실제 인수를 사용하여 각 형식 인수가 초기화됩니다.  형식 인수는 함수 헤더에 선언되며 함수 본문에 사용되는 인수입니다. 실제 인수를 올바른 형식으로 변환할 때 초기화에 의해 표준 변환과 사용자 정의 변환이 둘 다 수행되는 것처럼 변환이 수행됩니다.  다음 코드는 수행된 초기화를 개념적으로 보여 줍니다.  
  
    ```  
    void Func( int i ); // Function prototype  
    ...  
    Func( 7 );          // Execute function call  
    ```  
  
     호출 전의 개념적 초기화는 다음과 같습니다.  
  
    ```  
    int Temp_i = 7;  
    Func( Temp_i );  
    ```  
  
     괄호 구문 대신 등호 구문을 사용하는 것처럼 초기화가 수행됩니다.  함수에 값을 전달하기 전에 `i`의 복사본을 만듭니다.  자세한 내용은 [이니셜라이저](../cpp/initializers.md) 및[변환](../cpp/user-defined-type-conversions-cpp.md), [특수 멤버 함수를 사용한 초기화](http://msdn.microsoft.com/ko-kr/82223d73-64cb-4923-b678-78f9568ff3ca) 및 [명시적 초기화](http://msdn.microsoft.com/ko-kr/c89724f8-ddd3-4d77-b86d-77fcd8bd8595)를 참조하세요.  
  
     따라서 함수 프로토타입\(선언\)이 **long** 형식의 인수를 호출하고 호출하는 프로그램이 `int` 형식의 실제 인수를 제공하는 경우 **long** 형식에 대한 표준 형식 변환을 사용하여 실제 인수가 승격됩니다\([표준 변환](../cpp/standard-conversions.md) 참조\).  
  
     형식 인수의 형식에 대한 표준 또는 사용자 정의 변환이 없는 실제 인수를 제공하는 것은 오류입니다.  
  
     클래스 형식의 실제 인수의 경우 클래스의 생성자를 호출하여 형식 인수가 초기화됩니다.  이 특수 클래스 멤버 함수에 대한 자세한 내용은 [생성자](../cpp/constructors-cpp.md)를 참조하세요.  
  
-   함수 호출이 실행됩니다.  
  
 다음 프로그램 조각은 함수 호출을 보여 줍니다.  
  
```  
// expre_Formal_and_Actual_Arguments.cpp  
void func( long param1, double param2 );  
  
int main()  
{  
    long i = 1;  
    double j = 2;  
  
    // Call func with actual arguments i and j.  
    func( i, j );  
}  
  
// Define func with formal parameters param1 and param2.  
void func( long param1, double param2 )  
{  
}  
```  
  
 main에서 `func`가 호출되면 정식 매개 변수 `param1`이 `i`의 값으로 초기화됩니다. `i`는 표준 변환을 사용하여 올바른 형식에 맞게 **long** 형식으로 변환됩니다. 정식 매개 변수 `param2`는 `j`의 값으로 초기화됩니다. `j`는 표준 변환을 사용하여 **double** 형식으로 변환됩니다.  
  
## 인수 형식 처리  
 const 형식으로 선언된 형식 인수는 함수 본문 내에서 변경할 수 없습니다.  함수는 **const** 형식이 아닌 모든 인수를 변경할 수 있습니다.  그러나 이러한 변경은 함수에 대해 로컬이며 실제 인수가 **const** 형식이 아닌 개체에 대한 참조가 아닌 경우 실제 인수의 값에 영향을 주지 않습니다.  
  
 다음 함수는 이러한 개념을 몇 가지 보여 줍니다.  
  
```  
// expre_Treatment_of_Argument_Types.cpp  
int func1( const int i, int j, char *c ) {  
   i = 7;   // C3892 i is const.  
   j = i;   // value of j is lost at return  
   *c = 'a' + j;   // changes value of c in calling function  
   return i;  
}  
  
double& func2( double& d, const char *c ) {  
   d = 14.387;   // changes value of d in calling function.  
   *c = 'a';   // C3892 c is a pointer to a const object.  
    return d;  
}  
```  
  
## 줄임표 및 기본 인수  
 함수는 줄임표\(`...`\) 또는 기본 인수 메서드 중 하나를 사용하여 함수 정의에 지정된 것보다 적은 인수를 받도록 선언할 수 있습니다.  
  
 줄임표는 선언에 인수가 필요할 수 있지만 숫자와 형식은 지정되지 않음을 나타냅니다.  이는 C\+\+의 장점인 형식 안전성을 없애기 때문에 일반적으로 좋지 않은 C\+\+ 프로그래밍 관행입니다.  형식 및 실제 인수 형식을 보여 주는 함수보다는 줄임표로 선언된 함수에 다양한 변환이 적용됩니다.  
  
-   실제 인수가 **float** 형식인 경우 해당 인수는 함수 호출 전에 **double** 형식으로 승격됩니다.  
  
-   signed\/unsigned `char`, **short**, enumerated 형식 또는 비트 필드는 정수 계열 확장을 사용하여 signed\/unsigned `int`로 변환됩니다.  
  
-   클래스 형식의 인수는 데이터 구조 값에 의해 전달됩니다. 사본은 클래스의 복사 생성자\(있을 경우\) 호출을 통해서가 아닌 이진 복사를 통해 만들어집니다.  
  
 줄임표를 사용할 경우 인수 목록 마지막에 선언해야 합니다.  인수의 가변 수 전달에 대한 자세한 내용은 [](../c-runtime-library/reference/va-arg-va-copy-va-end-va-start.md "va_arg, va_copy, va_end, va_start")런타임 라이브러리 참조에서 *va\_arg, va\_start 및 va\_list*의 설명을 참조하세요.  
  
 CLR 프로그래밍의 기본 인수에 대한 자세한 내용은 [Variable Argument Lists \(...\) \(C\+\+\/CLI\)](../windows/variable-argument-lists-dot-dot-dot-cpp-cli.md)을 참조하세요.  
  
 기본 인수를 사용하면 함수 호출에 아무것도 제공되지 않은 경우 인수가 가정하는 값을 지정할 수 있습니다.  다음 코드는 기본 인수의 작동 방법을 보여 줍니다.  기본 인수 지정 제한에 대한 자세한 내용은 [기본 인수](../cpp/default-arguments.md)를 참조하세요.  
  
```  
// expre_Ellipses_and_Default_Arguments.cpp  
// compile with: /EHsc  
#include <iostream>  
  
// Declare the function print that prints a string,  
// then a terminator.  
void print( const char *string,  
            const char *terminator = "\n" );  
  
int main()  
{  
    print( "hello," );  
    print( "world!" );  
  
    print( "good morning", ", " );  
    print( "sunshine." );  
}  
  
using namespace std;  
// Define print.  
void print( const char *string, const char *terminator )  
{  
    if( string != NULL )  
        cout << string;  
  
    if( terminator != NULL )  
        cout << terminator;  
}  
```  
  
 앞의 프로그램은 두 개의 인수를 사용하는 `print` 함수를 선언합니다.  그러나 두 번째 인수 `terminator`의 기본값은 `"\n"`입니다.  **main**에서 `print`에 대한 처음 두 개의 호출은 기본 두 번째 인수가 새 줄을 제공하여 인쇄된 문자열을 종료할 수 있도록 합니다.  세 번째 호출은 두 번째 인수에 대해 명시적 값을 지정합니다.  프로그램의 출력:  
  
```  
hello,  
world!  
good morning, sunshine.  
```  
  
## 참고 항목  
 [식의 형식](../cpp/types-of-expressions.md)