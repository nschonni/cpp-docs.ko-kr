---
title: 파일 이름 매크로 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- macros, NMAKE
- filename macros in NMAKE
- NMAKE program, filename macros
ms.assetid: 20afd6b3-5b6c-4e33-9d01-309ce98ef9db
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: bc231dfb156460a2a0cc383b6d038a98c6e2015b
ms.sourcegitcommit: d10a2382832373b900b1780e1190ab104175397f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43894410"
---
# <a name="filename-macros"></a>파일 이름 매크로

파일 이름 매크로 종속성 (디스크의 하지 전체 파일 이름 사양이)에 지정 된 파일 이름으로 미리 정의 됩니다. 이러한 매크로; 호출 될 때 괄호로 묶이 필요가 없습니다. 표시 된 것 처럼 $만을 지정 합니다.

|매크로|의미|
|-----------|-------------|
|**$\@**|현재 지정 된 현재 대상의 전체 이름 (경로, 기본 이름, 확장)입니다.|
|**$$\@**|현재 지정 된 현재 대상의 전체 이름 (경로, 기본 이름, 확장)입니다. 종속성의 종속 으로만 사용할 수 있습니다.|
|**$&#42;**|파일 확장명을 제외한 현재 대상의 경로 및 기본 이름입니다.|
|**$&#42;&#42;**|현재 대상의 모든 종속 항목입니다.|
|**$?**|현재 대상 보다 나중 타임 스탬프를 사용 하 여 모든 종속 항목입니다.|
|**$<**|현재 대상 보다 나중 타임 스탬프를 사용 하 여 종속 파일입니다. 유추 규칙의 명령에만 유효 합니다.|

미리 정의 된 파일 이름 매크로의 일부를 지정 하려면 매크로 한정자를 추가 하 고 수정된 된 매크로 괄호로 묶습니다.

|한정자|결과 파일 이름 부분|
|--------------|-----------------------------|
|**D**|드라이브와 디렉터리|
|**B**|기본 이름|
|**F**|기본 이름 및 확장|
|**R**|드라이브와 디렉터리, 기본 이름|

## <a name="see-also"></a>참고 항목

[특수 NMake 매크로](../build/special-nmake-macros.md)
