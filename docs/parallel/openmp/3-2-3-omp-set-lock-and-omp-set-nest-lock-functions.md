---
title: 3.2.3 omp_set_lock and omp_set_nest_lock 함수 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: b5323879-f72e-418e-953f-3979fdda17a2
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 792b95baef2821bb693d9a90fc228d2b0c508e1f
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46420363"
---
# <a name="323-ompsetlock-and-ompsetnestlock-functions"></a>3.2.3 omp_set_lock and omp_set_nest_lock 함수

이러한 각 함수는 지정 된 잠금을 사용할 수 있고 잠금이 설정 될 때까지 함수를 실행 하는 스레드를 차단 합니다. 간단한 잠금은 잠금이 해제 될 경우 사용할 수 있습니다. 잠긴 경우 또는 함수를 실행 하는 스레드가 이미 소유 된 경우 중첩 가능 잠금 수입니다. 형식은 다음과 같습니다.

```
#include <omp.h>
void omp_set_lock(omp_lock_t *lock);
void omp_set_nest_lock(omp_nest_lock_t *lock);
```

간단한 잠금에 대 한 인수에 대 한는 `omp_set_lock` 함수 초기화 잠금 변수를 가리켜야 합니다. 함수를 실행 하는 스레드 잠금 소유권 부여 됩니다.

인수에서 중첩 가능 잠금는 `omp_set_nest_lock` 함수 초기화 잠금 변수를 가리켜야 합니다. 중첩 수 증가 하 고 스레드 부여 또는 잠금 소유권을 보유 합니다.