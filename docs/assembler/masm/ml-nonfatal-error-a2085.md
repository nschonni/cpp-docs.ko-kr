---
title: ML 심각 하지 않은 오류 A2085 | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: error-reference
f1_keywords:
- A2085
dev_langs:
- C++
helpviewer_keywords:
- A2085
ms.assetid: c2fef415-a32b-4249-896c-6d981fc6e327
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: dd5ec9f36a4f956b8eeb097b6a8f8eaed89ba2b2
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43681438"
---
# <a name="ml-nonfatal-error-a2085"></a>ML 심각하지 않은 오류 A2085

**명령 또는 현재 CPU 모드에서 허용 되지 않습니다 등록**

명령, 레지스터 또는 현재 프로세서 모드에 대 한 잘못 된 키워드를 사용 하려고 했습니다.

예를 들어 32 비트 레지스터 요구할 [.386](../../assembler/masm/dot-386.md) 이상. CR0 필요한 특권된 모드와 같은 컨트롤 레지스터가 [.386P](../../assembler/masm/dot-386p.md) 이상. 이 오류에 대 한도 생성 됩니다는 **NEAR32**, **FAR32**, 및 **플랫** 요구 하는 키워드입니다. **386** 이상.

## <a name="see-also"></a>참고자료

[ML 오류 메시지](../../assembler/masm/ml-error-messages.md)<br/>