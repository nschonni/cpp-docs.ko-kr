---
title: "C Pragma | Microsoft Docs"
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
  - "pragma, C/C++"
ms.assetid: 3d6d36b4-d565-4632-a4cd-e39aeaded5ad
caps.latest.revision: 13
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 13
---
# C Pragma
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

**Microsoft 전용**  
  
 "pragma"는 컴파일러가 컴파일 타임에 특정 작업을 수행하도록 지시합니다.  Pragma는 컴파일러마다 서로 다릅니다.  예를 들어 **optimize** pragma를 사용하여 프로그램에서 수행하는 최적화를 설정할 수 있습니다.  Microsoft C pragma는 다음과 같습니다.  
  
|||||  
|-|-|-|-|  
|**alloc\_text**|**data\_seg**|**inline\_recursion**|**setlocale**|  
|**auto\_inline**|**function**|**intrinsic**|**warning**|  
|**check\_stack**|**hdrstop**|**message**||  
|**code\_seg**|**include\_alias**|**optimize**||  
|**comment**|**inline\_depth**|**pack**||  
  
 Microsoft C 컴파일러 pragmas에 대한 설명은 *전처리기 참조*의 [Pragma 지시문 및 \_\_Pragma 키워드](../preprocessor/pragma-directives-and-the-pragma-keyword.md)를 참조하십시오.  
  
 **Microsoft 전용 종료**  
  
## 참고 항목  
 [원본 파일 및 원본 프로그램](../c-language/source-files-and-source-programs.md)