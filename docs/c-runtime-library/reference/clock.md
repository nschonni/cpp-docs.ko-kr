---
title: clock | Microsoft 문서
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
apiname:
- clock
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
- api-ms-win-crt-time-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- clock
dev_langs:
- C++
helpviewer_keywords:
- processor time used, calculating
- time, calculating processor
- clock function
- processor time used
- calculating processor time used
ms.assetid: 3e1853dd-498f-49ba-b06a-f2315f20904e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: fd4b399900802d110ff5746a0ccb2424ba40e6b5
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43209868"
---
# <a name="clock"></a>clock

호출 프로세스에서 사용하는 벽시계 시간을 계산합니다.

## <a name="syntax"></a>구문

```C
clock_t clock( void );
```

## <a name="return-value"></a>반환 값

프로세스의 시작 시 CRT 초기화 이후 경과 된 시간 단위의 **CLOCKS_PER_SEC** 초당 단위입니다. 경과 된 시간을 사용할 수 없거나으로 기록 될 수 있는 최대 양수 시간을 초과 하는 경우는 **clock_t** 형식 함수 값을 반환 합니다. `(clock_t)(-1)`합니다.

## <a name="remarks"></a>설명

합니다 **클록** 함수에서 프로세스 시작 중 CRT 초기화 이후 이후 경과 된 벽 시계 시간을 알려 줍니다. 이 함수는 ISO C를 엄격하게 준수하지는 않으며, 순 CPU 시간을 반환 값으로 지정합니다. CPU 시간을 가져오려면 Win32 [GetProcessTimes](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesstimes) 함수를 사용합니다. 경과 된 시간 (초)을 확인 하려면 반환 하는 값을 나누는 합니다 **클록** 매크로 의해 함수 **CLOCKS_PER_SEC**합니다.

충분 한 시간을 지정 된 값을 반환한 **클록** 의 최대 양수 값을 초과할 수 있습니다 **clock_t**합니다. 경우 프로세스가 더 길게 실행에서 반환 된 값 **클록** 항상 `(clock_t)(-1)`ISO C99 표준 (7.23.2.1) 및 ISO C11 표준 (7.27.2.1)에 지정 된 대로 합니다. Microsoft 구현 **clock_t** 으로 **긴**, 부호 있는 32 비트 정수를 하며 **CLOCKS_PER_SEC** 매크로가 1000으로 정의 됩니다. 이렇게 하면 최대 **클록** 함수 이렇게 하면 2147483.647 초 또는 약 24.8 일 반환 값입니다. 반환 된 값에 의존 하지 마십시오 **클록** 이 기간 보다 오랫동안 실행 된 프로세스에 있습니다. 64 비트를 사용할 수 있습니다 [시간](time-time32-time64.md) 함수나는 Windows [QueryPerformanceCounter](https://msdn.microsoft.com/library/windows/desktop/ms644904) 함수 수년간의 레코드 프로세스 경과 시간입니다.

## <a name="requirements"></a>요구 사항

|루틴에서 반환된 값|필수 헤더|
|-------------|---------------------|
|**clock**|\<time.h>|

호환성에 대한 자세한 내용은 [호환성](../../c-runtime-library/compatibility.md)을 참조하세요.

## <a name="example"></a>예제

```C
// crt_clock.c
// This sample uses clock() to 'sleep' for three
// seconds, then determines how long it takes
// to execute an empty loop 600000000 times.

#include <stdio.h>
#include <stdlib.h>
#include <time.h>

// Pauses for a specified number of milliseconds.
void do_sleep( clock_t wait )
{
   clock_t goal;
   goal = wait + clock();
   while( goal > clock() )
      ;
}

const long num_loops = 600000000L;

int main( void )
{
   long    i = num_loops;
   clock_t start, finish;
   double  duration;

   // Delay for a specified time.
   printf( "Delay for three seconds\n" );
   do_sleep( (clock_t)3 * CLOCKS_PER_SEC );
   printf( "Done!\n" );

   // Measure the duration of an event.
   start = clock();
   while( i-- )
      ;
   finish = clock();
   duration = (double)(finish - start) / CLOCKS_PER_SEC;
   printf( "Time to do %ld empty loops is ", num_loops );
   printf( "%2.3f seconds\n", duration );
}
```

```Output
Delay for three seconds
Done!
Time to do 600000000 empty loops is 1.354 seconds
```

## <a name="see-also"></a>참고자료

[시간 관리](../../c-runtime-library/time-management.md)<br/>
[difftime, _difftime32, _difftime64](difftime-difftime32-difftime64.md)<br/>
[time, _time32, _time64](time-time32-time64.md)<br/>
