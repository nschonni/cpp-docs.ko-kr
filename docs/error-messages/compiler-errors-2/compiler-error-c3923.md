---
title: "컴파일러 오류 C3923 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C3923"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3923"
ms.assetid: db8838e9-6344-4cd6-83e0-a8abeb12c4c0
caps.latest.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 8
---
# 컴파일러 오류 C3923
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'member': WinRT 또는 관리되는 클래스의 멤버 함수에는 지역 클래스, 구조체 또는 공용 구조체 정의를 사용할 수 없습니다.  
  
## 예제  
 다음 샘플에서는 C3923 오류가 발생하는 경우를 보여 줍니다.  
  
```  
// C3923.cpp  
// compile with: /clr /c  
ref struct x {  
   void Test() {  
      struct a {};   // C3923  
      class b {};   // C3923  
      union c {};   // C3923  
   }  
};  
```