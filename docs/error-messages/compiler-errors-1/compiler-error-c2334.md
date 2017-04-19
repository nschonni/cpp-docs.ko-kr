---
title: "컴파일러 오류 C2334 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C2334"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2334"
ms.assetid: 36142855-e00b-4bbf-80f5-a301edeff46e
caps.latest.revision: 9
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 9
---
# 컴파일러 오류 C2334
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

': or {' 앞에 예기치 않은 토큰이 있습니다. 명백한 함수 본문을 건너뜁니다.  
  
 다음 샘플에서는 C2334 오류가 발생하는 경우를 보여 줍니다.  이 오류는 오류 C2059가 발생한 후에 발생합니다.  
  
```  
// C2334.cpp  
// compile with: /c  
// C2059 expected  
struct s1 {  
   s1   {}   // C2334  
   s1() {}   // OK  
};  
```