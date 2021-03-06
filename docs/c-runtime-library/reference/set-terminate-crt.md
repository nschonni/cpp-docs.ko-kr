---
title: set_terminate(CRT) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
apiname:
- set_terminate
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
- api-ms-win-crt-runtime-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- set_terminate
dev_langs:
- C++
helpviewer_keywords:
- set_terminate function
- terminate function
- exception handling, termination
ms.assetid: 3ff1456a-7898-44bc-9266-a328a80b6006
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7e62dc1e4f99a1d2707c6e7b86c79e0ffc8aa027
ms.sourcegitcommit: 6e3cf8df676d59119ce88bf5321d063cf479108c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/22/2018
ms.locfileid: "34450978"
---
# <a name="setterminate-crt"></a>set_terminate(CRT)

사용자 고유의 종료 루틴의 호출을 설치 **종료**합니다.

## <a name="syntax"></a>구문

```cpp
terminate_function set_terminate( terminate_function termFunction );
```

### <a name="parameters"></a>매개 변수

*termFunction*<br/>
작성하는 terminate 함수에 대한 포인터입니다.

## <a name="return-value"></a>반환 값

이전 함수에 의해 등록에 대 한 포인터를 반환 **set_terminate** 이전 함수는 나중에 복원할 수 있도록 합니다. 기본 동작을 복원할 반환 값을 사용할 수 없는 이전 함수에 설정한 경우 이 값이 경우도 **NULL**합니다.

## <a name="remarks"></a>설명

**set_terminate** 설치 함수 *termFunction* 호출한 함수로 **종료**합니다. **set_terminate** c + + 예외 처리와 함께 사용 되 고 예외가 발생 하기 전에 프로그램에서 언제 든 지 호출할 수 있습니다. **종료** 호출 [중단](abort.md) 기본적으로 합니다. 자체 종료 함수를 작성 하 고 호출 하 여이 기본값을 변경할 수 있습니다 **set_terminate** 의 인수로 서 함수 이름으로 합니다. **종료** 에 대 한 인수로 주어진 마지막 함수를 호출 **set_terminate**합니다. 정리 작업을 원하는 수행 후 *termFunction* 프로그램을 종료 해야 합니다. 경우 (호출자에 게 반환) 하는 경우 종료 되지 않으면, [중단](abort.md) 호출 됩니다.

다중 스레드 환경에서 terminate 함수는 각 스레드에 대해 개별적으로 유지 관리됩니다. 각 새 스레드는 자체 terminate 함수를 설치해야 합니다. 따라서 각 스레드는 자체 종료 처리를 담당합니다.

**terminate_function** 형식이 EH에 정의 되어 있습니다. 사용자 지정 종료 함수에 대 한 포인터로 H *termFunction* 반환 하는 **void**합니다. 사용자 지정 함수 *termFunction* 없는 인수를 사용할 수 및 해당 호출자에 게 반환 해서는 안 됩니다. 그렇지 않으면 [중단](abort.md) 호출 됩니다. 내에서 예외를 throw 될 수 있습니다 *termFunction*합니다.

```cpp
typedef void ( *terminate_function )( );
```

> [!NOTE]
> **set_terminate** 함수에만 디버거 외부에서 작동 합니다.

단일 **set_terminate** 처리기에 대 한 모든 동적으로 연결 된 Dll 또는 Exe; 호출 하는 경우에 **set_terminate** 처리기에 의해 다른 대체 될 수 있습니다 또는 다른 설정한 처리기를 바꿀 수 있습니다 DLL 또는 EXE 합니다.

## <a name="requirements"></a>요구 사항

|루틴|필수 헤더|
|-------------|---------------------|
|**set_terminate**|\<eh.h>|

호환성에 대한 자세한 내용은 [호환성](../../c-runtime-library/compatibility.md)을 참조하세요.

## <a name="example"></a>예제

[terminate](terminate-crt.md)의 예제를 참조하세요.

## <a name="see-also"></a>참고자료

[예외 처리 루틴](../../c-runtime-library/exception-handling-routines.md)<br/>
[abort](abort.md)<br/>
[_get_terminate](get-terminate.md)<br/>
[set_unexpected](set-unexpected-crt.md)<br/>
[terminate](terminate-crt.md)<br/>
[unexpected](unexpected-crt.md)<br/>
