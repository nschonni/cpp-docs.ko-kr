---
title: NMAKE 실행 | Microsoft Docs
ms.custom: ''
ms.date: 09/05/2018
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- targets, building
- response files, NMAKE
- targets
- command files
- NMAKE program, targets
- NMAKE program, running
- command files, NMAKE
ms.assetid: 0421104d-8b7b-4bf3-86c1-928d9b7c1a8c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: bdc9d89dbc0e77a8002cc34e5d010ee49d761da4
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45706695"
---
# <a name="running-nmake"></a>NMAKE 실행

## <a name="syntax"></a>구문

> **NMAKE** [*옵션* ...] [*매크로* ...] [*대상* ...] [**\@**<em>commandfile</em> ...]

## <a name="remarks"></a>설명

NMAKE 빌드만 지정할 *대상* 또는 지정 되지 않은 경우 첫 번째 메이크파일의 대상으로 합니다. 첫 번째 메이크파일 대상 수를 [의사 대상](../build/pseudotargets.md) 다른 목표를 작성 하는 합니다. NMAKE /F;를 사용 하 여 지정 된 메이크파일을 사용합니다 /F 지정 하지 않으면 현재 디렉터리의 메이크파일 파일을 사용 합니다. 유추 규칙 사용 하 여 명령줄 빌드를 지정 된 메이크파일이 없는 경우 *대상*합니다.

합니다 *commandfile* 명령줄 입력을 포함 텍스트 파일 (또는 응답 파일). 다른 입력 앞 또는 뒤에 \@ *commandfile*합니다. 경로 허용 됩니다. *commandfile*, 줄 바꿈 공백으로 처리 됩니다. 공백이 포함 된 매크로 정의를 따옴표로 묶습니다.

## <a name="what-do-you-want-to-know-more-about"></a>추가 정보

[NMAKE 옵션](../build/nmake-options.md)

[Tools.ini 및 NMake](../build/tools-ini-and-nmake.md)

[NMAKE의 종료 코드](../build/exit-codes-from-nmake.md)

## <a name="see-also"></a>참고 항목

[NMAKE 참조](../build/nmake-reference.md)