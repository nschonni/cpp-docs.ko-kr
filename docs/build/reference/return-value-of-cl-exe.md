---
title: "cl.exe의 반환 값 | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "cl.exe 컴파일러, 반환 값"
ms.assetid: 7c2d7f33-ee0d-4199-8ef4-75fe2b007670
caps.latest.revision: 8
caps.handback.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# cl.exe의 반환 값
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

성공한 경우\(오류가 없는 경우\) cl.exe는 0을 반환하고 그렇지 않은 경우 0이 아닌 값을 반환합니다.  
  
 cl.exe의 반환 값은 스크립트, powershell, .cmd 또는 .bat 파일에서 컴파일하는 경우 유용할 수 있습니다.  오류나 경고가 발생할 경우 해결할 수 있도록 이 경우에도 컴파일러의 출력을 캡처하기 위한 계획을 세우는 것이 좋습니다.  
  
 가능한 오류 종료 코드가 너무 많아 cl.exe가 모두 나열할 수 없습니다.  %ProgramFiles\(x86\)%\\Windows Kits\\`version`\\Include\\shared\\ 디렉터리의 Windows 소프트웨어 개발 키트에 포함된 winerror.h 또는 ntstatus.h 파일에서 오류 코드를 조회할 수 있습니다.  10진수로 반환된 오류 코드는 검색을 위해 16진수로 변환해야 합니다.  예를 들어 오류 코드 \-1073741620를 16진수로 변환하면 0xC00000CC입니다.  이 오류는 ntstatus.h에서 찾을 수 있는데, 여기에서 해당 메시지는 "원격 서버에서 지정된 공유 이름을 찾을 수 없습니다."입니다. 다운로드할 수 있는 Windows 오류 코드 목록은 [&#91;MS\-ERREF&#93;: Windows Error Codes](http://msdn.microsoft.com/ko-kr/1bc92ddf-b79e-413c-bbaa-99a5281a6c90)를 참조하십시오.  
  
 Visual Studio의 오류 조회 유틸리티를 사용하여 컴파일러 오류 메시지의 의미를 찾을 수도 있습니다.  유틸리티를 시작하려면 Visual Studio 명령 셸에 **errlook.exe**를 입력합니다. 또는 Visual Studio IDE의 메뉴 모음에서 **도구**, **오류 조회**를 선택합니다.  오류와 연결된 설명 텍스트를 찾으려면 오류 값을 입력합니다.  자세한 내용은 [ERRLOOK 참조](../../build/reference/errlook-reference.md)을 참조하십시오.  
  
## 설명  
 아래의 예제 .bat 파일에서는 cl.exe의 반환 값을 사용합니다.  
  
```  
echo off  
cl /W4 t.cpp  
@if ERRORLEVEL == 0 (  
   goto good  
)  
  
@if ERRORLEVEL != 0 (  
   goto bad  
)  
  
:good  
   echo "clean compile"  
   echo %ERRORLEVEL%  
   goto end  
  
:bad  
   echo "error or warning"  
   echo %ERRORLEVEL%  
   goto end  
  
:end  
```  
  
## 참고 항목  
 [컴파일러 명령줄 구문](../../build/reference/compiler-command-line-syntax.md)