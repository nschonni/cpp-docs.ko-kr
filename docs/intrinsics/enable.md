---
title: 사용 (_e) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- _enable
- _enable_cpp
dev_langs:
- C++
helpviewer_keywords:
- enable intrinsic
- _enable intrinsic
- ssm instruction
ms.assetid: 8bee669b-6bd8-4e25-9383-bb7d57295b4d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ce3b59bc6665c4622078285a0c3b4b5011bc7d9b
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46433382"
---
# <a name="enable"></a>_enable

**Microsoft 전용**

인터럽트를 사용하도록 설정합니다.

## <a name="syntax"></a>구문

```
void _enable(void);
```

## <a name="requirements"></a>요구 사항

|내장 함수|아키텍처|
|---------------|------------------|
|`_enable`|x86, ARM, x64|

**헤더 파일** \<intrin.h >

## <a name="remarks"></a>설명

`_enable`은 인터럽트 플래그를 설정하도록 프로세서에 명령합니다. x86 시스템에서 이 함수는 인터럽트 플래그 설정(`sti`) 명령을 생성합니다.

이 함수는 커널 모드에서만 사용할 수 있습니다. 사용자 모드에서 이 함수를 사용하면 권한 있는 명령 예외가 throw됩니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고 항목

[컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)