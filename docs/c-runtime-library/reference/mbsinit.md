---
title: mbsinit | Microsoft 문서
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
apiname:
- mbsinit
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
- mbsinit
dev_langs:
- C++
helpviewer_keywords:
- mbsinit function
ms.assetid: 4618555b-baaa-4d04-93fa-36abae411034
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 413592bcf3af01c898a72d0ca70239364ee432f9
ms.sourcegitcommit: 6e3cf8df676d59119ce88bf5321d063cf479108c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/22/2018
ms.locfileid: "34450452"
---
# <a name="mbsinit"></a>mbsinit

멀티 바이트 문자 변환의 상태를 추적합니다.

## <a name="syntax"></a>구문

```C
int mbsinit(
   const mbstate_t* ps
);
```

### <a name="parameters"></a>매개 변수

*ps*<br/>
[mbstate_t](../../c-runtime-library/standard-types.md) 변수에 대한 포인터입니다.

## <a name="return-value"></a>반환 값

0이 아닌 경우 *ps* 은 **NULL** 이거나 변환 과정이 아닌 합니다.

## <a name="remarks"></a>설명

사용 하는 ANSI 함수 중 하나를 사용 하는 경우는 **mbstate_t** 포인터의 주소를 전달 하면 **mbstate_t** 버퍼의 마지막 바이트 변환 하는지 여부에 대 한 정보를 반환 합니다.

멀티바이트 문자를 지원하려면 적절한 코드 페이지를 설치해야 합니다.

## <a name="example"></a>예제

```cpp
// crt_mbsinit.cpp
#include <stdio.h>
#include <mbctype.h>
#include <string.h>
#include <locale.h>
#include <cwchar>
#include <xlocinfo.h>

#define   BUF_SIZE   0x40

wchar_t      g_wcBuf[BUF_SIZE] = L"This a wc buffer that will be over written...";
char      g_mbBuf[BUF_SIZE] = "AaBbCc\x9A\x8B\xE0\xEF\xF0xXyYzZ";
int      g_nInit = strlen(g_mbBuf);

int MbsinitSample(char* szIn, wchar_t* wcOut, int nMax)
{
   mbstate_t   state = {0};
   size_t      nConvResult, nmbLen = 0, nwcLen = 0;
   wchar_t*   wcCur = wcOut;
   wchar_t*   wcEnd = wcCur + nMax;
   const char*   mbCur = szIn;
   const char*   mbEnd = mbCur + strlen(mbCur) + 1;
   char*      szLocal = setlocale(LC_ALL, "japanese");

   printf("Locale set to: \"%s\"\n", szLocal);

   if   (_setmbcp(_MB_CP_LOCALE) != -1)
   {
      while   ((mbCur < mbEnd) && (wcCur < wcEnd))
      {
         nConvResult = mbrtowc(wcCur, mbCur, 1, &state);

         switch   (nConvResult)
         {
            case 0:
            {   // done
               printf("Conversion succeeded!\nMB String: ");
               printf(szIn);
               printf("\nWC String: ");
               wprintf(wcOut);
               printf("\n");
               mbCur = mbEnd;
               break;
            }

            case -1:
            {   // encoding error
               printf("ERROR: The call to mbrtowc has detected an encoding error.\n");
               mbCur = mbEnd;
               break;
            }

            case -2:
            {   // incomplete character
               if   (!mbsinit(&state))
               {
                  printf("Currently in middle of mb conversion, state = %x\n", state);
                  // state will contain data regarding lead byte of mb character
               }

               ++nmbLen;
               ++mbCur;
               break;
            }

            default:
            {
               if   (nConvResult > 2)   // Microsoft mb should never be larger than 2
                  printf("ERROR: nConvResult = %d\n", nConvResult);

               ++nmbLen;
               ++nwcLen;
               ++wcCur;
               ++mbCur;
               break;
            }
         }
      }
   }
   else
      printf("ERROR: _setmbcp(932) failed!");

   return 0;
}

int main(int argc, char* argv[])
{
   return MbsinitSample(g_mbBuf, g_wcBuf, BUF_SIZE);
}
```

### <a name="sample-output"></a>샘플 출력

```Output
Locale set to: "Japanese_Japan.932"
Currently in middle of mb conversion, state = 9a
Currently in middle of mb conversion, state = e0
Currently in middle of mb conversion, state = f0
Conversion succeeded!
MB String: AaBbCcxXyYzZ
WC String: AaBbCcxXyYzZ
```

## <a name="see-also"></a>참고자료

[바이트 분류](../../c-runtime-library/byte-classification.md)<br/>
