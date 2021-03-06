---
title: _amsg_exit | Microsoft 문서
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
apiname:
- _amsg_exit
apilocation:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
apitype: DLLExport
f1_keywords:
- _amsg_exit
dev_langs:
- C++
helpviewer_keywords:
- _amsg_exit
ms.assetid: 146d4faf-d763-43a4-b264-12711196456b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: dbb7f46bb4f3c942fd1c9e1a1d45c1ccf48739f7
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32392798"
---
# <a name="amsgexit"></a>_amsg_exit

지정된 런타임 오류 메시지를 내보낸 다음 오류 코드 255와 함께 응용 프로그램을 종료합니다.

## <a name="syntax"></a>구문

```cpp
void _amsg_exit ( int rterrnum );
```

### <a name="parameters"></a>매개 변수

*rterrnum*<br/>
시스템 정의 런타임 오류 메시지의 ID 번호입니다.

## <a name="remarks"></a>설명

이 함수는 콘솔 응용 프로그램에 대한 런타임 오류 메시지를 **stderr**로 내보내거나 Windows 응용 프로그램에 대한 메시지를 메시지 상자에 표시합니다. 디버그 모드에서 종료하기 전에 디버거를 호출하도록 선택할 수 있습니다.

## <a name="requirements"></a>요구 사항

|루틴|필수 헤더|
|-------------|---------------------|
|_amsg_exit|internal.h|