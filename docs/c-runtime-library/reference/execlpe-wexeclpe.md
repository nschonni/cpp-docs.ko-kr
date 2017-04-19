---
title: "_execlpe, _wexeclpe | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
apiname: 
  - "_execlpe"
  - "_wexeclpe"
apilocation: 
  - "msvcrt.dll"
  - "msvcr80.dll"
  - "msvcr90.dll"
  - "msvcr100.dll"
  - "msvcr100_clr0400.dll"
  - "msvcr110.dll"
  - "msvcr110_clr0400.dll"
  - "msvcr120.dll"
  - "msvcr120_clr0400.dll"
  - "ucrtbase.dll"
  - "api-ms-win-crt-process-l1-1-0.dll"
apitype: "DLLExport"
f1_keywords: 
  - "_wexeclpe"
  - "execlpe"
  - "wexeclpe"
  - "_execlpe"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "_execlpe 함수"
  - "_wexeclpe 함수"
  - "execlpe 함수"
  - "wexeclpe 함수"
ms.assetid: 07b861da-3e7e-4f1d-bb80-ad69b55e5162
caps.latest.revision: 21
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 21
---
# _execlpe, _wexeclpe
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

새 자식 프로세스를 로드하고 실행합니다.  
  
> [!IMPORTANT]
>  이 API는 Windows 런타임에서 실행되는 응용 프로그램에서 사용할 수 없습니다.  자세한 내용은 [\/ZW에서 지원하지 않는 CRT 함수](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx)를 참조하십시오.  
  
## 구문  
  
```  
intptr_t _execlpe(   
   const char *cmdname,  
   const char *arg0,  
   ... const char *argn,  
   NULL,  
   const char *const *envp   
);  
intptr_t _wexeclpe(   
   const wchar_t *cmdname,  
   const wchar_t *arg0,  
   ... const wchar_t *argn,  
   NULL,  
   const wchar_t *const *envp   
);  
```  
  
#### 매개 변수  
 `cmdname`  
 실행할 파일의 경로입니다.  
  
 `arg0`, `...``argn`  
 매개 변수에 대한 포인터 배열입니다.  
  
 `envp`  
 환경 설정에 대한 포인터 배열입니다.  
  
## 반환 값  
 성공하면 이러한 함수는 호출 프로세스에 값을 반환하지 않습니다.  반환 값 \-1은 오류를 나타내며, 이 경우 `errno` 전역 변수가 설정됩니다.  
  
|`errno` 값|설명|  
|---------------|--------|  
|`E2BIG`|인수 및 환경 설정에 필요한 공간의 크기가 32KB를 초과합니다.|  
|`EACCES`|지정한 파일이 잠금 또는 공유 위반이 되었습니다.|  
|`EINVAL`|잘못된 매개 변수입니다.|  
|`EMFILE`|실행 파일인지 여부를 확인하려면 지정한 파일이 열려 있어야 하지만, 열려 있는 파일이 너무 많습니다.|  
|`ENOENT`|파일 또는 경로를 찾을 수 없습니다.|  
|`ENOEXEC`|지정한 파일이 실행할 수 없거나 실행 파일 형식이 잘못되었습니다.|  
|`ENOMEM`|메모리가 부족하여 새 프로세스를 실행할 수 없습니다. 사용 가능한 메모리가 손상되었거나 잘못된 블록이 있습니다. 이는 호출 프로세스가 제대로 할당되지 않았음을 나타냅니다.|  
  
 이러한 반환 코드 및 기타 반환 코드에 대한 자세한 내용은 [\_doserrno, errno, \_sys\_errlist 및 \_sys\_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md)을 참조하십시오.  
  
## 설명  
 이러한 각각의 함수는 만들어지고 새로운 프로세스를 실행합니다, 별도 매개 변수로 각 명령줄 인수를 전달하고 환경 설정에 포인터의 배열을 전달 합니다.  이러한 함수는 `PATH` 환경 변수를 사용하여 실행할 파일을 찾습니다.  
  
 이러한 `_execlpe` 함수는 해당 함수 매개 변수의 유효성을 검사합니다.  `cmdname` 또는 `arg0` 은 null 포인터이거나 빈 문자열일 경우, 이러한 함수에 [매개 변수 유효성 검사](../../c-runtime-library/parameter-validation.md) 로 설명된대로 잘못된 매개 변수 처리기를 호출합니다.  계속해서 실행하도록 허용된 경우, 이러한 함수는 `errno`를 `EINVAL` 로 설정하고 \-1을 반환합니다.  프로세스가 시작되지 않습니다.  
  
## 요구 사항  
  
|Function|필수 헤더|선택적 헤더|  
|--------------|-----------|------------|  
|`_execlpe`|\<process.h\>|\<\<errno.h\>\>|  
|`_wexeclpe`|\<process.h\> 또는 \<wchar.h\>|\<\<errno.h\>\>|  
  
 호환성 정보에 대한 자세한 내용은 [호환성](../../c-runtime-library/compatibility.md)을 참조하십시오.  
  
## 예제  
 [\_exec, \_wexec 함수](../../c-runtime-library/exec-wexec-functions.md)의 예제를 참조하십시오.  
  
## 해당 .NET Framework 항목  
  
-   [System::Diagnostics::Process 클래스](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.aspx)  
  
-   [System::Diagnostics::ProcessStartInfo 클래스](https://msdn.microsoft.com/en-us/library/system.diagnostics.processstartinfo.aspx)  
  
## 참고 항목  
 [프로세스 및 환경 제어](../../c-runtime-library/process-and-environment-control.md)   
 [\_exec, \_wexec 함수](../../c-runtime-library/exec-wexec-functions.md)   
 [abort](../../c-runtime-library/reference/abort.md)   
 [atexit](../../c-runtime-library/reference/atexit.md)   
 [exit, \_Exit, \_exit](../../c-runtime-library/reference/exit-exit-exit.md)   
 [\_onexit, \_onexit\_m](../../c-runtime-library/reference/onexit-onexit-m.md)   
 [\_spawn, \_wspawn 함수](../../c-runtime-library/spawn-wspawn-functions.md)   
 [system, \_wsystem](../../c-runtime-library/reference/system-wsystem.md)