---
title: "함수 선언이 포함된 저장소 클래스 지정자 | Microsoft Docs"
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
  - "함수 선언, 지정자"
  - "외부 선언"
  - "외부 링크, 함수 선언"
  - "외부 링크, 저장소 클래스 지정자"
  - "함수 지정자, 저장소 클래스"
  - "지정자, 함수"
ms.assetid: 801d7df2-efa9-4924-a725-274a5654cfd4
caps.latest.revision: 7
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 7
---
# 함수 선언이 포함된 저장소 클래스 지정자
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

함수 선언에서 **static** 또는 `extern` 저장소 클래스 지정자를 사용할 수 있습니다.  함수에는 항상 전역 수명이 있습니다.  
  
 **Microsoft 전용**  
  
 내부 수준의 함수 선언은 외부 수준의 함수 선언과 동일한 의미를 갖습니다.  즉, 함수가 지역 범위에서 선언되더라도 나머지 변환을 통해 선언 시점부터 표시됩니다.  
  
 **Microsoft 전용 종료**  
  
 함수의 표시 유형 규칙은 다음과 같이 변수의 규칙과 약간 다릅니다.  
  
-   **static**으로 선언된 함수는 정의된 소스 파일 내에서만 볼 수 있습니다.  같은 소스 파일의 함수는 **static** 함수를 호출할 수 있지만 다른 소스 파일의 함수는 이름으로 직접 액세스할 수 없습니다.  충돌 없이 다른 소스 파일에서 같은 이름을 사용하여 다른 **static** 함수를 선언할 수 있습니다.  
  
-   `extern`으로 선언된 함수는 나중에 **static**으로 재선언하지 않는 한 프로그램의 모든 소스 파일에서 볼 수 있습니다.  모든 함수는 `extern` 함수를 호출할 수 있습니다.  
  
-   저장소 클래스 지정자를 생략하는 함수 선언은 기본적으로 `extern`입니다.  
  
 **Microsoft 전용**  
  
 Microsoft에서는 `extern` 식별자를 **static**으로 재선언하도록 허용합니다.  
  
 **Microsoft 전용 종료**  
  
## 참고 항목  
 [C 저장소 클래스](../c-language/c-storage-classes.md)