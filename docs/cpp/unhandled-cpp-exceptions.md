---
title: "처리되지 않은 C++ 예외 | Microsoft Docs"
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
  - "C++ 예외 처리, 처리되지 않은 예외"
  - "catch 키워드[C++], 처리기를 찾을 수 없음"
  - "이벤트 처리기, 처리되지 않은 예외"
  - "예외, 처리되지 않은"
  - "처리되지 않은 예외"
ms.assetid: 13f09c53-9254-4407-9db9-14e730e047cc
caps.latest.revision: 7
caps.handback.revision: 7
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# 처리되지 않은 C++ 예외
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

현재 예외에 대해 일치하는 처리기\(또는 줄임표 **catch** 처리기\)를 찾을 수 없는 경우 미리 정의된 `terminate` 런타임 함수가 호출됩니다. `terminate`는 모든 처리기에서 명시적으로 호출할 수도 있습니다. `terminate`의 기본 작업은 `abort`를 호출하는 것입니다.  응용 프로그램을 종료하기 전에 `terminate`로 프로그램의 몇 가지 다른 함수를 호출하려면 단일 인수로 호출되는 함수 이름을 사용하여 `set_terminate` 함수를 호출합니다.  `set_terminate`는 프로그램에서 언제든지 호출할 수 있습니다.  `terminate` 루틴은 `set_terminate`에 대한 인수로 주어진 마지막 함수를 항상 호출합니다.  
  
## 예제  
 다음 예제는  `char *` 예외를 throw하지만 `char *` 형식의 예외를 catch하도록 지정된 처리기를 포함하지 않습니다.  `set_terminate` 호출은 `terminate`가 `term_func`를 호출하도록 명령합니다.  
  
```  
// exceptions_Unhandled_Exceptions.cpp  
// compile with: /EHsc  
#include <iostream>  
using namespace std;  
void term_func() {  
   cout << "term_func was called by terminate." << endl;  
   exit( -1 );  
}  
int main() {  
   try  
   {  
      set_terminate( term_func );  
      throw "Out of memory!"; // No catch handler for this exception  
   }  
   catch( int )  
   {  
      cout << "Integer exception raised." << endl;  
   }  
   return 0;  
}  
```  
  
## Output  
  
```  
term_func was called by terminate.  
```  
  
 `term_func` 함수는 `exit`를 호출하여 프로그램이나 현재 스레드를 종료합니다.  이 호출이 호출자로 반환되면 `abort`가 호출됩니다.  
  
## 참고 항목  
 [C\+\+ 예외 처리](../cpp/cpp-exception-handling.md)