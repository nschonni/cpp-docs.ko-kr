---
title: "반복 문 (C++) | Microsoft Docs"
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
  - "반복문"
  - "루프 구조, 반복문"
ms.assetid: bf6d75f7-ead2-426a-9c47-33847f59b8c7
caps.latest.revision: 8
caps.handback.revision: 8
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# 반복 문 (C++)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

반복 문을 사용하면 루프 종료 조건에 따라 문\(또는 복합 문\)이 0회 이상 실행됩니다.  이러한 문이 복합 문인 경우 [break](../cpp/break-statement-cpp.md) 문 또는 [continue](../cpp/continue-statement-cpp.md) 문이 있는 경우를 제외하고 순서대로 실행됩니다.  
  
 C\+\+에서는 [while](../cpp/while-statement-cpp.md), [do](../cpp/do-while-statement-cpp.md), [for](../cpp/for-statement-cpp.md) 및 [range\-based for](../cpp/range-based-for-statement-cpp.md)라는 네 가지 반복 문을 제공합니다.  이러한 각 반복 문은 종료 식이 0\(false\)으로 평가되거나 **break** 문으로 루프가 종료될 때까지 반복됩니다.  다음 표에는 이러한 문과 해당 작업이 요약되어 있습니다. 각 문에 대해서는 뒤에 나오는 단원에서 자세히 설명합니다.  
  
### 반복 문  
  
|문|평가 위치|초기화|증가|  
|-------|-----------|---------|--------|  
|`while`|루프의 맨 위|아니요|아니요|  
|**do**|루프의 맨 아래|아니요|아니요|  
|**for**|루프의 맨 위|예|예|  
|**range\-based for**|루프의 맨 위|예|예|  
  
 반복 문의 문 부분은 선언일 수 없지만,  선언을 포함하는 복합 문일 수 있습니다.  
  
## 참고 항목  
 [C\+\+문 개요](../cpp/overview-of-cpp-statements.md)