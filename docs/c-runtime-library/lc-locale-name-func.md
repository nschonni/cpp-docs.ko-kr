---
title: ___lc_locale_name_func | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: conceptual
apiname:
- ___lc_locale_name_func
apilocation:
- msvcrt.dll
- msvcr110.dll
- msvcr100.dll
- msvcr90.dll
- msvcr120.dll
- msvcr80.dll
- msvcr110_clr0400.dll
apitype: DLLExport
f1_keywords:
- ___lc_locale_name_func
dev_langs:
- C++
helpviewer_keywords:
- ___lc_locale_name_func
ms.assetid: ef858308-872e-43de-95e0-9b1b4084343e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: eb94b73bf3f32c61fae37f7d3c9b9c51d012bfb6
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46087918"
---
# <a name="lclocalenamefunc"></a>___lc_locale_name_func

내부 CRT 함수입니다. 스레드의 현재 로캘 이름을 검색합니다.

## <a name="syntax"></a>구문

```cpp
wchar_t** ___lc_locale_name_func(void);
```

## <a name="return-value"></a>반환 값

스레드의 현재 로캘 이름이 포함된 문자열에 대한 포인터입니다.

## <a name="remarks"></a>설명

`___lc_locale_name_func`는 다른 CRT 함수가 CRT 데이터의 스레드 로컬 저장소에서 현재 로캘 이름을 가져오기 위해 사용하는 내부 CRT 함수입니다. [_get_current_locale](../c-runtime-library/reference/get-current-locale.md) 함수 또는 [setlocale, _wsetlocale](../c-runtime-library/reference/setlocale-wsetlocale.md) 함수를 사용하면 이 정보를 사용할 수 있습니다.

내부 CRT 함수는 구현과 관련되어 있으며 각 릴리스 시 변경될 수 있습니다. 따라서 사용자 코드에는 사용하지 않는 것이 좋습니다.

## <a name="requirements"></a>요구 사항

|루틴에서 반환된 값|필수 헤더|
|-------------|---------------------|
|`___lc_locale_name_func`|crt\src\setlocal.h|

## <a name="see-also"></a>참고 항목

[_get_current_locale](../c-runtime-library/reference/get-current-locale.md)<br/>
[setlocale, _wsetlocale](../c-runtime-library/reference/setlocale-wsetlocale.md)<br/>
[_create_locale, _wcreate_locale](../c-runtime-library/reference/create-locale-wcreate-locale.md)<br/>
[_free_locale](../c-runtime-library/reference/free-locale.md)