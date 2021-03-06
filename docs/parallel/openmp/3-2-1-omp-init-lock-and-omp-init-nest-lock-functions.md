---
title: 3.2.1 omp_init_lock and omp_init_nest_lock 함수 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 098a2721-b16a-484f-bc83-4b8e281e382c
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 4303eb3ccfcb1c449022a4be32f94b9f91e6e80c
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46387005"
---
# <a name="321-ompinitlock-and-ompinitnestlock-functions"></a>3.2.1 omp_init_lock and omp_init_nest_lock 함수

이러한 함수에는 잠금을 초기화 하는 유일한 수단을 제공 합니다. 각 함수 초기화 매개 변수를 사용 하 여 연결 된 잠금을 *잠금* 후속 호출에서 사용 합니다. 형식은 다음과 같습니다.

```
#include <omp.h>
void omp_init_lock(omp_lock_t *lock);
void omp_init_nest_lock(omp_nest_lock_t *lock);
```

초기 상태를 잠긴 아닙니다 (즉, 스레드가 소유 하지 않는 잠금). 중첩 가능 잠금을 초기 중첩 개수는 0입니다. 비규격 이미 초기화 된 잠금 변수를 사용 하 여 이러한 루틴 중 하나를 호출 하는 것입니다.