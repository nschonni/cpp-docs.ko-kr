---
title: "멀티바이트 및 와이드 문자 | Microsoft Docs"
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
  - "문자 코드[C++], 멀티바이트"
  - "문자 코드[C++], 와이드"
  - "문자 데이터 형식[C]"
  - "문자[C++], 코드"
  - "문자[C++], 와이드"
  - "전역화[C++], 문자 집합"
  - "국가별 응용 프로그램[C++], 문자 표시"
  - "멀티바이트 문자[C++]"
  - "형식[C], 문자"
  - "유니코드[C++], 와이드 문자 집합"
  - "와이드 문자[C++]"
ms.assetid: 1943c469-200d-4724-b18f-781d70520f9e
caps.latest.revision: 6
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 6
---
# 멀티바이트 및 와이드 문자
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

멀티바이트 문자는 하나 이상의 바이트의 시퀀스로 구성된 문자입니다.  각 바이트 시퀀스는 확장된 문자 집합에서 단일 문자를 나타냅니다.  멀티바이트 문자는 한자와 같은 문자 집합에 사용됩니다.  
  
 와이드 문자는 항상 16비트 크기의 다국어 문자 코드입니다.  문자 상수 형식은 `char`이며 와이드 문자 형식은 `wchar_t`입니다.  와이드 문자의 크기는 항상 고정되어 있으므로 와이드 문자를 사용하면 국제 공용 문자 집합으로 단순하게 프로그래밍할 수 있습니다.  
  
 와이드 문자열 리터럴, `L"hello"`는 `wchar_t` 형식의 6개의 정수 배열이 됩니다.  
  
```  
{L'h', L'e', L'l', L'l', L'o', 0}  
```  
  
 유니코드 사양은 와이드 문자에 대한 사양입니다.  멀티바이트 및 와이드 문자 간 변환을 위한 런타임 라이브러리 루틴에는 `mbstowcs`, `mbtowc`, `wcstombs` 및 `wctomb`가 있습니다.  
  
## 참고 항목  
 [C 식별자](../c-language/c-identifiers.md)