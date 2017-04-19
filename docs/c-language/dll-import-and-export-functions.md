---
title: "DLL 가져오기 및 내보내기 함수 | Microsoft Docs"
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
  - "함수 선언, dllexport 및 dllimport"
  - "DLL 내보내기[C++]"
  - "dllexport 특성[C++], 저장소 클래스 특성"
  - "dllimport 특성[C++], 저장소 클래스 특성"
  - "DLL[C++], 가져오기"
  - "확장 저장소 클래스 특성"
ms.assetid: 08d164b9-770a-4e14-afeb-c6f21d9e33e4
caps.latest.revision: 9
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 9
---
# DLL 가져오기 및 내보내기 함수
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

**Microsoft 전용**  
  
 이 내용에 대한 가장 완벽한 최신 정보는 [dllexport, dllimport](../cpp/dllexport-dllimport.md)에서 확인할 수 있습니다.  
  
 **dllimport** 및 `dllexport` 저장소 클래스 한정자는 Microsoft 전용 C 언어 확장입니다.  이러한 한정자는 해당 클라이언트에 대한 DLL 인터페이스\(실행 파일 또는 다른 DLL\)를 명시적으로 정의합니다.  함수를 `dllexport`로 선언하면 모듈 정의\(.DEF\) 파일을 사용할 필요가 없습니다.  또한 **dllimport** 및 `dllexport` 한정자는 데이터 및 개체와 함께 사용할 수 있습니다.  
  
 다음 예제와 같이 **dllimport** 및 `dllexport` 저장소 클래스 한정자는 확장된 특성 구문 키워드인 `__declspec`와 함께 사용해야 합니다.  
  
```  
#define DllImport   __declspec( dllimport )  
#define DllExport   __declspec( dllexport )  
  
DllExport void func();  
DllExport int i = 10;  
DllExport int j;  
DllExport int n;  
```  
  
 확장된 저장소 클래스 한정자에 사용되는 구문에 대한 자세한 내용은 [확장된 저장소 클래스 특성](../c-language/c-extended-storage-class-attributes.md)을 참조하십시오.  
  
 **Microsoft 전용 종료**  
  
## 참고 항목  
 [C 함수 정의](../c-language/c-function-definitions.md)