---
title: 이전 코드 (Visual c + +)를 위한 부동 소수점 지원 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: a2a26b96-7bc2-418a-981a-51aa1a0294a2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7285325bf1a934afcef337da318d019ec6fe375c
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45706812"
---
# <a name="floating-point-support-for-older-code-visual-c"></a>이전 코드를 위한 부동 소수점 지원(Visual C++)

MMX와 부동 소수점 스택 레지스터 (MM0-MM7/ST0-ST7) 컨텍스트 스위치 간에 유지 됩니다.  이러한 레지스터에 대 한 명시적 호출 규칙이 없는 경우  이러한 레지스터를 사용 하 여 커널 모드 코드에서 엄격 하 게 사용할 수 없습니다.

## <a name="see-also"></a>참고 항목

[호출 규칙](../build/calling-convention.md)