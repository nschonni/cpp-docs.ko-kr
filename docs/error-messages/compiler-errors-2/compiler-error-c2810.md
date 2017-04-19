---
title: "컴파일러 오류 C2810 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C2810"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2810"
ms.assetid: f63e8f24-d7f6-42ac-904f-72ff49592ba6
caps.latest.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 8
---
# 컴파일러 오류 C2810
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'interface' : 인터페이스는 다른 인터페이스에서만 상속될 수 있습니다.  
  
 [interface](../../cpp/interface.md)는 다른 인터페이스에서만 상속할 수 있습니다. 클래스나 구조체에서는 상속할 수 없습니다.  
  
 다음 샘플에서는 C2810 오류가 발생하는 경우를 보여 줍니다.  
  
```  
// C2810.cpp  
#include <unknwn.h>  
class CBase1 {  
public:  
  HRESULT mf1();  
  int  m_i;  
};  
  
[object, uuid="40719E20-EF37-11D1-978D-0000F805D73B"]  
__interface IDerived : public CBase1 {  // C2810  
// try the following line instead  
// __interface IDerived {  
   HRESULT mf2(void *a);  
};  
  
struct CBase2 {  
   HRESULT mf1(int a, char *b);  
   HRESULT mf2();  
};  
```