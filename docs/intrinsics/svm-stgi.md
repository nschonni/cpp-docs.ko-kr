---
title: __svm_stgi | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __svm_stgi
dev_langs:
- C++
helpviewer_keywords:
- __svm_stgi intrinsic
- STGI instruction
ms.assetid: 96488da4-5587-4e99-8674-627a9e51be84
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: fd4d2593621c7c2cc36f84580a757e98f5e48c92
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46431257"
---
# <a name="svmstgi"></a>__svm_stgi

**Microsoft 전용**

전역 인터럽트 플래그를 설정합니다.

## <a name="syntax"></a>구문

```
void __svm_stgi(void);
```

## <a name="remarks"></a>설명

합니다 `__svm_stgi` 함수는 동일 합니다 `STGI` 컴퓨터 명령입니다. 전역는 인터럽트 플래그를 여부를 결정 마이크로프로세서 무시, 연기, I/O 완료, 하드웨어 온도 경고를 또는 디버그 예외와 같은 이벤트로 인해 인터럽트를 처리 합니다.

이 함수는 게스트 운영 체제 및 해당 응용 프로그램과 호스트 가상 머신 모니터의 상호 작용을 지원합니다. 자세한 내용은 문서를 검색 "AMD64 아키텍처 프로그래머 수동 볼륨 2: 시스템 프로그래밍"에서 24593, 3.11, 수정 버전 번호를 문서화 합니다 [AMD corporation](https://developer.amd.com/resources/developer-guides-manuals/) 사이트입니다.

## <a name="requirements"></a>요구 사항

|내장 함수|아키텍처|
|---------------|------------------|
|`__svm_stgi`|x86, x64|

**헤더 파일** \<intrin.h >

**Microsoft 전용 종료**

## <a name="see-also"></a>참고 항목

[컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)<br/>
[__svm_clgi](../intrinsics/svm-clgi.md)