---
title: "따옴표로 묶인 파일 이름 포함 | Microsoft Docs"
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
ms.assetid: 789a047e-ea38-4c99-b71d-a2ad9c81daee
caps.latest.revision: 7
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 7
---
# 따옴표로 묶인 파일 이름 포함
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

**ANSI 3.8.2** 포함 가능한 소스 파일에 대한 따옴표 붙은 이름 지원  
  
 두 큰따옴표\(" "\) 사이의 포함 파일에 대해 완전하고 명확한 경로 지정을 지정하는 경우 전처리기는 해당 경로 지정만 검색하고 표준 디렉터리를 무시합니다.  
  
 [\#include](../preprocessor/hash-include-directive-c-cpp.md) "path\-spec"으로 지정된 포함 파일의 경우 디렉터리 검색은 부모 파일의 디렉터리에서 시작한 다음 모든 조부모 파일의 디렉터리를 통해 진행됩니다.  따라서 검색이 현재 처리 중인 소스 파일을 포함하는 디렉터리를 기준으로 시작됩니다.  조부모 파일이 없고 파일이 검색되지 않은 경우 파일 이름이 꺾쇠 괄호로 묶여 있는 것처럼 검색이 계속됩니다.  
  
## 참고 항목  
 [전처리 지시문](../c-language/preprocessing-directives.md)