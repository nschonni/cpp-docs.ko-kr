---
title: Null 및 정의 되지 않은 매크로 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- NMAKE program, undefined macros
- Null macros in NMAKE
- macros, null and undefined
- undefined macros and NMAKE
- NMAKE program, null macros
ms.assetid: 1db4611a-1755-4328-b00f-d35365af8b6c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: eee6e713715e4709af990878224261a41f5470e3
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45702639"
---
# <a name="null-and-undefined-macros"></a>null 및 정의되지 않은 매크로

Null 문자열을 null 및 정의 되지 않은 매크로 확장 하지만 null 문자열로 정의 된 매크로 전처리 식에 정의 된 것으로 간주 됩니다. Null 문자열로 매크로 정의 하려면 문자가 공백이 나 탭을 제외 하 고 명령줄 또는 명령 파일에서 등호 (=) 뒤 및 null 문자열 또는 정의 큰따옴표로 묶습니다 지정 (""). 매크로 정의 하지 않으려면 **! UNDEF 합니다.** 자세한 내용은 [메이크파일 전처리 지시문](../build/makefile-preprocessing-directives.md)합니다.

## <a name="see-also"></a>참고 항목

[NMake 매크로 정의](../build/defining-an-nmake-macro.md)