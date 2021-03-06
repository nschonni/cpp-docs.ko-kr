---
title: fputc, fputwc | Microsoft 문서
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
apiname:
- fputc
- fputwc
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
- api-ms-win-crt-stdio-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- fputc
- fputwc
- _fputtc
dev_langs:
- C++
helpviewer_keywords:
- streams, writing characters to
- fputtc function
- _fputtc function
- fputwc function
- fputc function
ms.assetid: 5a0a593d-43f4-4fa2-a401-ec4e23de4d2f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: af93e0c42002dc557f691daadd2fc003dced0247
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32401422"
---
# <a name="fputc-fputwc"></a>fputc, fputwc

스트림에 문자를 씁니다.

## <a name="syntax"></a>구문

```C
int fputc(
   int c,
   FILE *stream
);
wint_t fputwc(
   wchar_t c,
   FILE *stream
);
```

### <a name="parameters"></a>매개 변수

*c*<br/>
쓸 문자입니다.

*스트림*<br/>
**FILE** 구조체에 대한 포인터입니다.

## <a name="return-value"></a>반환 값

이러한 각 함수는 기록된 문자를 반환합니다. 에 대 한 **fputc**, 반환 값이 **EOF** 은 오류를 나타냅니다. 에 대 한 **fputwc**, 반환 값이 **WEOF** 은 오류를 나타냅니다. 경우 *스트림* 은 **NULL**에 설명 된 대로 잘못 된 매개 변수 처리기를 호출 하는이 함수를 이러한 [매개 변수 유효성 검사](../../c-runtime-library/parameter-validation.md)합니다. 실행을 계속 허용 된 경우 반환 **EOF** 설정 **errno** 를 **EINVAL**합니다.

이러한 오류 코드 및 기타 오류 코드에 대한 자세한 내용은 [_doserrno, errno, _sys_errlist 및 _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md)를 참조하세요.

## <a name="remarks"></a>설명

이러한 각 함수는 단일 문자를 씁니다 *c* 위치에 파일을 나타내는 연결 된 파일 위치 표시기 (정의 된 경우)를 적절 하 게 표시기를 앞으로 이동 합니다. 경우 **fputc** 및 **fputwc**, 파일 연결 된 *스트림*합니다. 파일이 위치 지정 요청을 지원할 수 없거나 추가 모드에서 열린 경우에는 문자가 스트림의 끝에 추가됩니다.

스트림이 ANSI 모드에서 열리는 경우 두 함수는 동일하게 작동합니다. **fputc** 현재 UNICODE 스트림에 출력을 지원 하지 않습니다.

**_nolock** 접미사가 있는 버전은 다른 스레드에 의한 간섭에서 보호되지 않는 점을 제외하면 동일합니다. 자세한 내용은 [_fputc_nolock, _fputwc_nolock](fputc-nolock-fputwc-nolock.md)를 참조하세요.

이어서 루틴별 설명이 제공됩니다.

|루틴|설명|
|-------------|-------------|
|**fputc**|에 해당 **putc**, 하지만 아닌 함수 및 매크로 함수로 구현 합니다.|
|**fputwc**|와이드 문자 버전의 **fputc**합니다. 기록 *c* 멀티 바이트 문자 또는 와이드 문자 열리는지에 따라 *스트림* 텍스트 모드 또는 이진 모드에서 열립니다.|

### <a name="generic-text-routine-mappings"></a>제네릭 텍스트 라우팅 매핑

|TCHAR.H 루틴|_UNICODE 및 _MBCS 정의되지 않음|_MBCS 정의됨|_UNICODE 정의됨|
|---------------------|------------------------------------|--------------------|-----------------------|
|**_fputtc**|**fputc**|**fputc**|**fputwc**|

## <a name="requirements"></a>요구 사항

|함수|필수 헤더|
|--------------|---------------------|
|**fputc**|\<stdio.h>|
|**fputwc**|\<stdio.h> 또는 \<wchar.h>|

콘솔 유니버설 Windows 플랫폼 (UWP) 응용 프로그램에서 지원 되지 않습니다. 콘솔에 연결된 된 표준 스트림 핸들-**stdin**, **stdout**, 및 **stderr**-C 런타임 함수 UWP 앱에서 사용할 수 있는 전에 리디렉션되어야 . 호환성에 대한 자세한 내용은 [호환성](../../c-runtime-library/compatibility.md)을 참조하세요.

## <a name="example"></a>예제

```C
// crt_fputc.c
// This program uses fputc
// to send a character array to stdout.

#include <stdio.h>

int main( void )
{
   char strptr1[] = "This is a test of fputc!!\n";
   char *p;

   // Print line to stream using fputc.
   p = strptr1;
   while( (*p != '\0') && fputc( *(p++), stdout ) != EOF ) ;

}
```

```Output
This is a test of fputc!!
```

## <a name="see-also"></a>참고자료

[스트림 I/O](../../c-runtime-library/stream-i-o.md)<br/>
[fgetc, fgetwc](fgetc-fgetwc.md)<br/>
[putc, putwc](putc-putwc.md)<br/>
