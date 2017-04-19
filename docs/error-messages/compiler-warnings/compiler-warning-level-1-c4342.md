---
title: "컴파일러 경고 (수준 1) C4342 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C4342
dev_langs:
- C++
helpviewer_keywords:
- C4342
ms.assetid: 47d4d5ab-069f-4cdc-98c3-10d649577a37
caps.latest.revision: 10
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: c4a2afbc3ced186b0db63b22b3cc5c2b27204c71
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-warning-level-1-c4342"></a>컴파일러 경고(수준 1) C4342
동작 변경: '*함수*' 호출 되었지만 이전 버전에서는 멤버 연산자가 호출  
  
 Visual Studio 2002 하기 전에 Visual c + + 버전에서는 멤버를 호출 되지만이 동작이 변경 되었습니다 찾은 컴파일러 이제 가장 일치 하는 네임 스페이스 범위에서입니다.  
  
 멤버 연산자를 찾은 경우 컴파일러는 이전에 고려 하지 않습니다 모든 네임 스페이스 범위 연산자입니다. 네임 스페이스 범위에 더 적합 한 경우 현재 컴파일러가 올바르게 호출 하는, 반면 이전 컴파일러를 고려 하지 않습니다.  
  
 이 경고는 코드를 현재 버전으로 올바르게 이식 해제 되어야 합니다.  컴파일러는 코드에 대 한이 경고를 생성 하는 거짓 긍정을 제공할 수 있습니다는 동작이 변경 되지 않습니다.  
  
 기본적으로 이 경고는 해제되어 있습니다. 자세한 내용은 참조 [기본적으로 해제 되어 있는 컴파일러 경고](../../preprocessor/compiler-warnings-that-are-off-by-default.md)합니다.  
  
 다음 샘플에서는 C4342 오류가 생성 됩니다.  
  
```cpp  
// C4342.cpp  
// compile with: /EHsc /W1  
#include <fstream>  
#pragma warning(default: 4342)  
using namespace std;  
struct X : public ofstream {  
   X();  
};  
  
X::X() {  
   open( "ofs_bug_ev.txt." );  
   if ( is_open() ) {  
      *this << "Text" << "<-should be text" << endl;   // C4342  
      *this << ' ' << "<-should be space symbol" << endl;   // C4342  
   }  
}  
  
int main() {  
   X b;  
   b << "Text" << "<-should be text" << endl;  
   b << ' ' << "<-should be space symbol" << endl;  
}  
```