---
title: "컴파일러 경고 (수준 1) C4722 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C4722
dev_langs:
- C++
helpviewer_keywords:
- C4722
ms.assetid: d8660710-f67b-4f59-a5fd-59259475529e
caps.latest.revision: 6
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
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: a88d734f0f17437efe3b4a60a3439135b7feec4e
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-warning-level-1-c4722"></a>컴파일러 경고(수준 1) C4722
'function': 소멸자가 반환하지 않습니다. 메모리 누수가 발생할 수 있습니다.  
  
 제어 흐름이 소멸자에서 종료됩니다. 스레드 또는 전체 프로그램이 종료되고 할당된 리소스를 해제할 수 없습니다.  또한 예외 처리 중 스택 해제를 위해 소멸자가 호출될 경우 실행 파일의 동작이 정의되지 않습니다.  
  
 이 문제를 해결하려면 소멸자 반환을 방해하는 함수 호출을 제거합니다.  
  
## <a name="example"></a>예제  
 다음 샘플에서는 C4722를 생성합니다.  
  
```  
// C4722.cpp  
// compile with: /O1 /W1 /c  
#include <stdlib.h>  
class C {  
public:  
   C();  
   ~C() { exit(1); };   // C4722  
};  
  
extern void func (C*);  
  
void Test(){  
   C x;  
   func(&x);  
   // control will not leave Test because destructor will exit  
}  
```