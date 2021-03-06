---
title: 가정 | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: reference
f1_keywords:
- ASSUME
dev_langs:
- C++
helpviewer_keywords:
- ASSUME directive
ms.assetid: cd162070-aee9-4c65-babc-005c6cc73d7c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6fbba50e56ae06dc3afb64582d4a131bba75a6c8
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50055855"
---
# <a name="assume"></a>ASSUME

오류 레지스터 값에 대 한 검사를 사용 합니다.

## <a name="syntax"></a>구문

> ASSUME *segregister*:*이름* [[를 *segregister*:*이름*]]...<br/>
> ASSUME *dataregister*:*유형* [[를 *dataregister*:*형식*]]...<br/>
> 가정 *등록할*: 오류 [[합니다 *등록*: 오류]]...<br/>
> 가정 [[*등록할*:]] NOTHING [[, *등록*: NOTHING]]...

## <a name="remarks"></a>설명

이후에 `ASSUME` 어셈블러 감시는 지정 된 레지스터의 값이 변경 효과에 배치 됩니다. **오류** 등록을 사용 하는 경우 오류가 발생 합니다. **NOTHING** 제거 오류 검사를 등록 합니다. 여러 가지 가정 하나의 문으로 결합할 수 있습니다.

## <a name="see-also"></a>참고자료

[지시문 참조](../../assembler/masm/directives-reference.md)<br/>