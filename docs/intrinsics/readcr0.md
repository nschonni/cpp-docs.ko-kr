---
title: __readcr0 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __readcr0
dev_langs:
- C++
helpviewer_keywords:
- __readcr0 intrinsic
ms.assetid: 25bdb093-d83c-48d7-9c0f-224de8e2c61c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f989c7bd6cc74a688e8694ed59899c59c50cb0d4
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46430659"
---
# <a name="readcr0"></a>__readcr0

**Microsoft 전용**

CR0 레지스터를 읽고 해당 값을 반환합니다.

## <a name="syntax"></a>구문

```
unsigned long __readcr0(void);  /* X86 */
unsigned __int64 __readcr0(void);  /* X64 */

```

## <a name="return-value"></a>반환 값

CR0 레지스터의 값입니다.

## <a name="requirements"></a>요구 사항

|내장 함수|아키텍처|
|---------------|------------------|
|`__readcr0`|x86, x64|

**헤더 파일** \<intrin.h >

## <a name="remarks"></a>설명

이 내장 함수는 커널 모드에서만 사용할 수 있으며 루틴은 내장 함수로만 사용할 수 있습니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고 항목

[컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)