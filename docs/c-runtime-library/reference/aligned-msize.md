---
title: "_aligned_msize | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- _aligned_msize
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
- api-ms-win-crt-heap-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- _aligned_msize
- aligned_msize
dev_langs:
- C++
helpviewer_keywords:
- aligned_msize function
- _aligned_msize function
ms.assetid: 10995edc-2110-4212-9ca9-5e0220a464f4
caps.latest.revision: 6
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
ms.sourcegitcommit: 84964b0a49b236bae056125de8155b18880eb378
ms.openlocfilehash: 375eb2921ac47be819eeb050fa87643c50a52289
ms.lasthandoff: 02/24/2017

---
# <a name="alignedmsize"></a>_aligned_msize
힙에 할당된 메모리 블록의 크기를 반환합니다.  
  
## <a name="syntax"></a>구문  
  
```  
size_t _msize(  
   void *memblock,  
   size_t alignment,  
   size_t offset  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 [in] `memblock`  
 메모리 블록에 대한 포인터입니다.  
  
 [in] `alignment`  
 맞춤 값으로 2의 정수 거듭제곱이어야 합니다.  
  
 [in] `offset`  
 맞춤을 강제하는 메모리 할당으로의 오프셋입니다.  
  
## <a name="return-value"></a>반환 값  
 크기(바이트)를 부호 없는 정수로 반환합니다.  
  
## <a name="remarks"></a>설명  
 `_aligned_msize` 함수는 [_aligned_malloc](../../c-runtime-library/reference/aligned-malloc.md) 또는 [_aligned_realloc](../../c-runtime-library/reference/aligned-realloc.md) 호출에 의해 할당된 메모리 블록의 크기를 바이트 단위로 반환합니다. `alignment` 및 `offset` 값은 블록을 할당한 함수에 전달된 값과 동일해야 합니다.  
  
 응용 프로그램이 디버그 버전의 C 런타임 라이브러리에 연결되면 `_aligned_msize`는 [_aligned_msize_dbg](../../c-runtime-library/reference/aligned-msize-dbg.md)가 됩니다. 디버깅 프로세스 동안 힙을 관리하는 방법에 대한 자세한 내용은 [CRT 디버그 힙](/visualstudio/debugger/crt-debug-heap-details)을 참조하세요.  
  
 이 함수는 해당 매개 변수의 유효성을 검사합니다. `memblock`이 null 포인터이거나 `alignment`가 2의 거듭제곱이 아닌 경우 `_msize`는 [매개 변수 유효성 검사](../../c-runtime-library/parameter-validation.md)에서 설명한 대로 잘못된 매개 변수 처리기를 호출합니다. 오류가 처리되면 함수는 `errno`를 `EINVAL`로 설정하고 -1을 반환합니다.  
  
## <a name="requirements"></a>요구 사항  
  
|루틴|필수 헤더|  
|-------------|---------------------|  
|`_msize`|\<malloc.h>|  
  
 호환성에 대한 자세한 내용은 소개에서 [호환성](../../c-runtime-library/compatibility.md)을 참조하세요.  
  
## <a name="libraries"></a>라이브러리  
 모든 버전의 [C 런타임 라이브러리](../../c-runtime-library/crt-library-features.md)입니다.  
  
## <a name="net-framework-equivalent"></a>.NET Framework의 해당 값  
 해당 사항 없음. 표준 C 함수를 호출하려면 `PInvoke`를 사용합니다. 자세한 내용은 [플랫폼 호출 예제](http://msdn.microsoft.com/Library/15926806-f0b7-487e-93a6-4e9367ec689f)를 참조하세요.  
  
## <a name="see-also"></a>참고 항목  
 [메모리 할당](../../c-runtime-library/memory-allocation.md)