---
title: "다른 테이블에 행에 대한 참조가 들어 있는 경우의 열 업데이트 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "행 집합, 열 업데이트"
ms.assetid: abb5db69-055d-431f-b12d-ad2940a661ba
caps.latest.revision: 7
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 7
---
# 다른 테이블에 행에 대한 참조가 들어 있는 경우의 열 업데이트
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

일부 공급자는 행에서 변경된 열을 감지할 수 있지만, 대부분의 공급자는 그렇게 하지 못합니다.  따라서, 업데이트하려는 행에 대한 참조가 있는 경우, 열을 업데이트하면 오류가 발생할 수 있습니다.  이 문제를 해결하려면, 변경하려는 열만 들어 있는 개별 접근자를 만드십시오.  해당 접근자의 번호를 `SetData`에 전달하십시오.  
  
## 참고 항목  
 [접근자 사용](../../data/oledb/using-accessors.md)