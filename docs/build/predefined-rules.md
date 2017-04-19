---
title: "미리 정의된 규칙 | Microsoft Docs"
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
  - "규칙, 미리 정의됨"
  - "NMAKE 프로그램, 미리 정의된 규칙"
  - "NMAKE의 미리 정의된 규칙"
ms.assetid: 638cdc3f-4aba-4b4f-96e3-ad65b0364f12
caps.latest.revision: 9
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 9
---
# 미리 정의된 규칙
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

미리 정의된 규칙은 NMAKE에서 제공한 명령과 옵션 매크로를 사용합니다.  
  
|규칙|명령|기본<br /><br /> action|일괄 처리<br /><br /> 규칙|nmake 실행 플랫폼|  
|--------|--------|-------------------|------------------|------------------|  
|.asm.exe|$\(AS\) $\(AFLAGS\) $\<|ml $\<|no|x86|  
|.asm.obj|$\(AS\) $\(AFLAGS\) \/c $\<|ml \/c $\<|yes|x86|  
|.asm.exe|$\(AS\) $\(AFLAGS\) $\<|ml64 $\<|no|[!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]|  
|.asm.obj|$\(AS\) $\(AFLAGS\) \/c $\<|ml64 \/c $\<|yes|[!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]|  
|.c.exe|$\(CC\) $\(CFLAGS\) $\<|cl $\<|no|모두|  
|.c.obj|$\(CC\) $\(CFLAGS\) \/c $\<|cl \/c $\<|yes|모두|  
|.cc.exe|$\(CC\) $\(CFLAGS\) $\<|cl $\<|no|모두|  
|.cc.obj|$\(CC\) $\(CFLAGS\) \/c $\<|cl \/c $\<|yes|모두|  
|.cpp.exe|$\(CPP\) $\(CPPFLAGS\) $\<|cl $\<|no|모두|  
|.cpp.obj|$\(CPP\) $\(CPPFLAGS\) \/c $\<|cl \/c $\<|yes|모두|  
|.cxx.exe|$\(CXX\) $\(CXXFLAGS\) $\<|cl $\<|no|모두|  
|.cxx.obj|$\(CXX\) $\(CXXFLAGS\) \/c $\<|cl \/c $\<|yes|모두|  
|.rc.res|$\(RC\) $\(RFLAGS\) \/r $\<|rc \/r $\<|no|모두|  
  
## 참고 항목  
 [유추 규칙](../build/inference-rules.md)