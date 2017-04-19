---
title: "_acmdln, _tcmdln, _wcmdln | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
apiname: 
  - "_wcmdln"
  - "_acmdln"
apilocation: 
  - "msvcrt.dll"
apitype: "DLLExport"
f1_keywords: 
  - "_acmdln"
  - "acmdln"
  - "_wcmdln"
  - "wcmdln"
  - "_tcmdln"
  - "tcmdln"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "_acmdln 전역 변수"
  - "_tcmdln 전역 변수"
  - "_wcmdln 전역 변수"
  - "acmdln 전역 변수"
  - "tcmdln 전역 변수"
  - "wcmdln 전역 변수"
ms.assetid: 4fc0a6a0-3f93-420a-a19f-5276061ba539
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# _acmdln, _tcmdln, _wcmdln
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

내부 CRT 전역 변수입니다.  명령줄입니다.  
  
## 구문  
  
```  
char * _acmdln; wchar_t * _wcmdln;  #ifdef WPRFLAG    #define _tcmdln _wcmdln #else    #define _tcmdln _acmdln  
```  
  
## 설명  
 이러한 CRT 내부 변수는 전체 명령줄을 저장하고  CRT의 내보낸 기호에 노출되지만 사용자 코드에 사용할 수는 없습니다.  `_acmdln`은 데이터를 문자열로 저장합니다.  `_wcmdln`은 데이터를 와이드 문자열로 저장합니다.  `_tcmdln`은 어떤 것이 적절한지에 따라 `_acmdln` 또는  `_wcmdln`으로 정의할 수 있습니다.  
  
## 참고 항목  
 [전역 변수](../c-runtime-library/global-variables.md)