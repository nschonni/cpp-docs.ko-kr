---
title: "_fullpath_dbg, _wfullpath_dbg | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- _wfullpath_dbg
- _fullpath_dbg
apilocation:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
apitype: DLLExport
f1_keywords:
- wfullpath_dbg
- _wfullpath_dbg
- _fullpath_dbg
- fullpath_dbg
dev_langs:
- C++
helpviewer_keywords:
- _fullpath_dbg function
- relative file paths
- absolute paths
- fullpath_dbg function
- _wfullpath_dbg function
- wfullpath_dbg function
ms.assetid: 81f72f85-07da-4f5c-866a-598e0fb03f6b
caps.latest.revision: 16
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
translationtype: Machine Translation
ms.sourcegitcommit: a937c9d083a7e4331af63323a19fb207142604a0
ms.openlocfilehash: 13dea0e3f4fdaef74d4806373376d5c84904ce8f
ms.lasthandoff: 02/24/2017

---
# <a name="fullpathdbg-wfullpathdbg"></a>_fullpath_dbg, _wfullpath_dbg
`malloc`의 디버그 버전을 사용하여 메모리를 할당하는 [_fullpath, _wfullpath](../../c-runtime-library/reference/fullpath-wfullpath.md)의 버전입니다.  
  
## <a name="syntax"></a>구문  
  
```  
char *_fullpath_dbg(   
   char *absPath,  
   const char *relPath,  
   size_t maxLength,  
   int blockType,  
   const char *filename,  
   int linenumber   
);  
wchar_t *_wfullpath_dbg(   
   wchar_t *absPath,  
   const wchar_t *relPath,  
   size_t maxLength,  
   int blockType,  
   const char *filename,  
   int linenumber   
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `absPath`  
 절대 또는 전체 경로 이름이나 `NULL`이 포함된 버퍼에 대한 포인터입니다.  
  
 `relPath`  
 상대 경로 이름입니다.  
  
 `maxLength`  
 절대 경로 이름 버퍼(`absPath`)의 최대 길이입니다. 이 길이는 `_fullpath`의 바이트 수로, `wchar_t`의 경우에는 와이드 문자 수입니다(`_wfullpath`).  
  
 `blockType`  
 요청된 메모리 블록 형식으로 `_CLIENT_BLOCK` 또는 `_NORMAL_BLOCK`입니다.  
  
 `filename`  
 할당 작업 또는 `NULL`을 요청한 소스 파일의 이름에 대한 포인터입니다.  
  
 `linenumber`  
 할당 작업이 요청되었거나 `NULL`인 소스 파일의 줄 번호입니다.  
  
## <a name="return-value"></a>반환 값  
 각 함수는 절대 경로 이름(`absPath`)이 포함된 버퍼에 대한 포인터를 반환합니다. 오류가 있는 경우(예: `relPath`에서 전달된 값에 잘못되었거나 찾을 수 없는 드라이브 문자가 포함된 경우 또는 작성된 절대 경로 이름(`absPath`)의 길이가 `maxLength`보다 큰 경우) 함수는 `NULL`을 반환합니다.  
  
## <a name="remarks"></a>설명  
 NULL이 첫 번째 매개 변수로 전달된 경우 **_**`DEBUG`가 정의되면 이러한 함수가 , `malloc`, `_malloc_dbg`의 디버그 버전을 사용하여 메모리를 할당한다는 점을 제외하면 `_fullpath_dbg` 및 `_wfullpath_dbg` 함수는 `_fullpath` 및 `_wfullpath`와 동일합니다. `_malloc_dbg`의 디버깅 기능에 대한 자세한 내용은 [_malloc_dbg](../../c-runtime-library/reference/malloc-dbg.md)를 참조하세요.  
  
 대부분의 경우 이러한 함수를 명시적으로 호출할 필요가 없습니다. 대신 `_CRTDBG_MAP_ALLOC` 플래그를 정의할 수 있습니다. `_CRTDBG_MAP_ALLOC`를 정의하면 `_fullpath` 및 `_wfullpath`에 대한 호출이 각각 `_fullpath_dbg` 및 `_wfullpath_dbg`로 다시 매핑되고 `blockType`은 `_NORMAL_BLOCK`으로 설정됩니다. 따라서 힙 블록을 `_CLIENT_BLOCK`으로 표시하려는 경우가 아니면 이러한 함수를 명시적으로 호출할 필요가 없습니다. 자세한 내용은 [디버그 힙의 블록 형식](/visualstudio/debugger/crt-debug-heap-details)을 참조하세요.  
  
### <a name="generic-text-routine-mappings"></a>제네릭 텍스트 라우팅 매핑  
  
|Tchar.h 루틴|_UNICODE 및 _MBCS 정의되지 않음|_MBCS 정의됨|_UNICODE 정의됨|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_tfullpath_dbg`|`_fullpath_dbg`|`_fullpath_dbg`|`_wfullpath_dbg`|  
  
## <a name="requirements"></a>요구 사항  
  
|함수|필수 헤더|  
|--------------|---------------------|  
|`_fullpath_dbg`|\<crtdbg.h>|  
|`_wfullpath_dbg`|\<crtdbg.h>|  
  
 호환성에 대한 자세한 내용은 소개에서 [호환성](../../c-runtime-library/compatibility.md)을 참조하세요.  
  
## <a name="net-framework-equivalent"></a>.NET Framework의 해당 값  
 <xref:System.IO.File.Create%2A>  
  
## <a name="see-also"></a>참고 항목  
 [파일 처리](../../c-runtime-library/file-handling.md)   
 [_fullpath, _wfullpath](../../c-runtime-library/reference/fullpath-wfullpath.md)   
 [힙 할당 함수의 디버그 버전](/visualstudio/debugger/debug-versions-of-heap-allocation-functions)