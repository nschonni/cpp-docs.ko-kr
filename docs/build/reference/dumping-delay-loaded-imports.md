---
title: 지연 로드 된 가져오기 덤프 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- delay-loaded imports, dumping
- imports (delay-loaded)
- delay-loaded imports
ms.assetid: f766acf4-9df8-4b85-8cf6-0be3ffc4c124
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 29f2faecb29da93729b0be0f40c00c18b82f6344
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45720878"
---
# <a name="dumping-delay-loaded-imports"></a>지연 로드된 가져오기 덤프

사용 하 여 지연 로드 가져오기를 덤프할 수 있습니다 [/imports dumpbin](../../build/reference/imports-dumpbin.md) 표준 가져오기와 조금씩 다른 정보를 사용 하 여 표시 합니다. 이러한 덤프 /imports 고유한 섹션으로 분리 되 고는 명시적으로 지연 로드 가져오기로 레이블이 지정 합니다. 가 언로드 정보가 이미지에는 표시 됩니다. 바인드 정보가 있으면 대상 DLL의 날짜/시간 스탬프 가져오기 바인딩된 주소와 함께 표시 됩니다.

## <a name="see-also"></a>참고 항목

[링커의 지연 로드된 DLL 지원](../../build/reference/linker-support-for-delay-loaded-dlls.md)