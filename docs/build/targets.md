---
title: 대상 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- targets, specifying in NMAKE
ms.assetid: 826ee849-4278-4c6e-97c3-79a2b5fe6463
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: edb75258c548526c68ed33f7f8037656750f6855
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45713808"
---
# <a name="targets"></a>대상

종속 줄의 모든 유효한 파일 이름, 디렉터리 이름을 사용 하 여 하나 이상의 대상을 지정 하거나 [의사 대상](../build/pseudotargets.md)합니다. 하나 이상의 공백이 나 탭을 사용 하 여 여러 대상을 구분 합니다. 대상은 대/소문자 구분 하지 않습니다. 경로 파일 이름에 허용 됩니다. 대상에는 256 자를 초과할 수 없습니다. 콜론 앞의 대상이 단일 문자 구분 공간; 사용 그렇지 않으면 NMAKE 콜론 문자 조합을 드라이브 지정자로 해석합니다.

## <a name="what-do-you-want-to-know-more-about"></a>추가 정보

[의사 대상](../build/pseudotargets.md)

[여러 대상](../build/multiple-targets.md)

[누적 종속성](../build/cumulative-dependencies.md)

[여러 개의 설명 블록에는 대상](../build/targets-in-multiple-description-blocks.md)

[의도 하지 않은 종속성](../build/dependency-side-effects.md)

## <a name="see-also"></a>참고 항목

[설명 블록](../build/description-blocks.md)