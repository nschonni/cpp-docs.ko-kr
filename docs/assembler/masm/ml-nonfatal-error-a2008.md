---
title: ML 심각 하지 않은 오류 A2008 | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: error-reference
f1_keywords:
- A2008
dev_langs:
- C++
helpviewer_keywords:
- A2008
ms.assetid: ca24157f-c88a-4678-ae06-3bc3cd956001
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 774cf4c2a51bf084fb63e572cc99b0c8e3cba26f
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43679377"
---
# <a name="ml-nonfatal-error-a2008"></a>ML 심각하지 않은 오류 A2008

**구문 오류:**

현재 위치에서 토큰을 구문 오류가 발생 했습니다.

다음 중 하나를 발생할 수 있습니다.

- 점 접두사에 추가 되었거나 지시문에서 생략 됩니다.

- 예약어 (같은 **C** 하거나 **크기**) 식별자로 사용 되었습니다.

- 명령에는 현재 프로세서 또는 프로세서 선택 항목과 함께 사용할 수 없었던 사용 되었습니다.

- 런타임 비교 연산자 (같은 `==`)는 관계형 연산자 대신 조건부 어셈블리 문에서 사용 된 (같은 [EQ](../../assembler/masm/operator-eq.md)).

- 지침이 나 지시문에는 너무 적은 피연산자 제공 되었습니다.

- 사용 되지 않는 지시문을 사용 했습니다.

## <a name="see-also"></a>참고자료

[ML 오류 메시지](../../assembler/masm/ml-error-messages.md)<br/>