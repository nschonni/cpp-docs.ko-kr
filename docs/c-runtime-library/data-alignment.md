---
title: 데이터 정렬 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: conceptual
f1_keywords:
- data.alignment
dev_langs:
- C++
helpviewer_keywords:
- data alignment [C++]
ms.assetid: 35ac3d2d-a4b3-421b-954f-b7372b1f18e1
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: aa83c067e8a2f6794adde13ed8f163ac7ee52680
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32392460"
---
# <a name="data-alignment"></a>데이터 맞춤

다음 C 런타임 함수는 데이터 정렬을 지원합니다.

## <a name="data-alignment-routines"></a>데이터 정렬 루틴

|루틴에서 반환된 값|사용|
|-------------|---------|
|[_aligned_free](../c-runtime-library/reference/aligned-free.md)|[_aligned_malloc](../c-runtime-library/reference/aligned-malloc.md) 또는 [_aligned_offset_malloc](../c-runtime-library/reference/aligned-offset-malloc.md)를 사용하여 할당된 메모리 블록을 해제합니다.|
|[_aligned_free_dbg](../c-runtime-library/reference/aligned-free-dbg.md)|[_aligned_malloc](../c-runtime-library/reference/aligned-malloc.md) 또는 [_aligned_offset_malloc](../c-runtime-library/reference/aligned-offset-malloc.md)를 사용하여 할당된 메모리 블록을 해제합니다(디버그에만 해당).|
|[_aligned_malloc](../c-runtime-library/reference/aligned-malloc.md)|지정된 맞춤 경계에 메모리를 할당합니다.|
|[_aligned_malloc_dbg](../c-runtime-library/reference/aligned-malloc-dbg.md)|디버깅 헤더에 대한 추가 공간이 있는 지정된 정렬 경계에서 메모리 블록을 할당하고 버퍼를 덮어씁니다(디버그 버전에만 해당).|
|[_aligned_msize](../c-runtime-library/reference/aligned-msize.md)|힙에 할당된 메모리 블록의 크기를 반환합니다.|
|[_aligned_msize_dbg](../c-runtime-library/reference/aligned-msize-dbg.md)|힙에 할당된 메모리 블록의 크기를 반환합니다(디버그 버전에만 해당).|
|[_aligned_offset_malloc](../c-runtime-library/reference/aligned-offset-malloc.md)|지정된 맞춤 경계에 메모리를 할당합니다.|
|[_aligned_offset_malloc_dbg](../c-runtime-library/reference/aligned-offset-malloc-dbg.md)|지정된 맞춤 경계에 메모리를 할당합니다(디버그 버전에만 해당).|
|[_aligned_offset_realloc](../c-runtime-library/reference/aligned-offset-realloc.md)|[_aligned_malloc](../c-runtime-library/reference/aligned-malloc.md) 또는 [_aligned_offset_malloc](../c-runtime-library/reference/aligned-offset-malloc.md)를 사용하여 할당된 메모리 블록의 크기를 변경합니다.|
|[_aligned_offset_realloc_dbg](../c-runtime-library/reference/aligned-offset-realloc-dbg.md)|[_aligned_malloc](../c-runtime-library/reference/aligned-malloc.md) 또는 [_aligned_offset_malloc](../c-runtime-library/reference/aligned-offset-malloc.md)를 사용하여 할당된 메모리 블록의 크기를 변경합니다(디버그 버전에만 해당).|
|[_aligned_offset_recalloc](../c-runtime-library/reference/aligned-offset-recalloc.md)|[_aligned_malloc](../c-runtime-library/reference/aligned-malloc.md) 또는 [_aligned_offset_malloc](../c-runtime-library/reference/aligned-offset-malloc.md)를 사용하여 할당된 메모리 블록의 크기를 변경하고 메모리를 0으로 초기화합니다.|
|[_aligned_offset_recalloc_dbg](../c-runtime-library/reference/aligned-offset-recalloc-dbg.md)|[_aligned_malloc](../c-runtime-library/reference/aligned-malloc.md) 또는 [_aligned_offset_malloc](../c-runtime-library/reference/aligned-offset-malloc.md)를 사용하여 할당된 메모리 블록의 크기를 변경하고 메모리를 0으로 초기화합니다(디버그 버전에만 해당).|
|[_aligned_realloc](../c-runtime-library/reference/aligned-realloc.md)|[_aligned_malloc](../c-runtime-library/reference/aligned-malloc.md) 또는 [_aligned_offset_malloc](../c-runtime-library/reference/aligned-offset-malloc.md)를 사용하여 할당된 메모리 블록의 크기를 변경합니다.|
|[_aligned_realloc_dbg](../c-runtime-library/reference/aligned-realloc-dbg.md)|[_aligned_malloc](../c-runtime-library/reference/aligned-malloc.md) 또는 [_aligned_offset_malloc](../c-runtime-library/reference/aligned-offset-malloc.md)를 사용하여 할당된 메모리 블록의 크기를 변경합니다(디버그 버전에만 해당).|
|[_aligned_recalloc](../c-runtime-library/reference/aligned-recalloc.md)|[_aligned_malloc](../c-runtime-library/reference/aligned-malloc.md) 또는 [_aligned_offset_malloc](../c-runtime-library/reference/aligned-offset-malloc.md)를 사용하여 할당된 메모리 블록의 크기를 변경하고 메모리를 0으로 초기화합니다.|
|[_aligned_recalloc_dbg](../c-runtime-library/reference/aligned-recalloc-dbg.md)|[_aligned_malloc](../c-runtime-library/reference/aligned-malloc.md) 또는 [_aligned_offset_malloc](../c-runtime-library/reference/aligned-offset-malloc.md)를 사용하여 할당된 메모리 블록의 크기를 변경하고 메모리를 0으로 초기화합니다(디버그 버전에만 해당).|

## <a name="see-also"></a>참고 항목

[범주별 유버니설 C 런타임 루틴](../c-runtime-library/run-time-routines-by-category.md)<br/>