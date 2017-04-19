---
title: "strcpy, wcscpy, _mbscpy | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
apiname: 
  - "strcpy"
  - "wcscpy"
  - "_mbscpy"
apilocation: 
  - "msvcrt.dll"
  - "msvcr80.dll"
  - "msvcr90.dll"
  - "msvcr100.dll"
  - "msvcr100_clr0400.dll"
  - "msvcr110.dll"
  - "msvcr110_clr0400.dll"
  - "msvcr120.dll"
  - "msvcr120_clr0400.dll"
  - "ucrtbase.dll"
  - "api-ms-win-crt-multibyte-l1-1-0.dll"
  - "api-ms-win-crt-string-l1-1-0.dll"
apitype: "DLLExport"
f1_keywords: 
  - "_mbscpy"
  - "_ftcscpy"
  - "wcscpy"
  - "_tcscpy"
  - "strcpy"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "_ftcscpy 함수"
  - "_mbscpy 함수"
  - "_tcscpy 함수"
  - "문자열 복사"
  - "ftcscpy 함수"
  - "mbscpy 함수"
  - "strcpy 함수"
  - "문자열[C++], 복사"
  - "tcscpy 함수"
  - "wcscpy 함수"
ms.assetid: f97a4f81-e9ee-4f15-888a-0fa5d7094c5a
caps.latest.revision: 31
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 31
---
# strcpy, wcscpy, _mbscpy
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

문자열을 복사합니다.  이러한 함수의 더 안전한 버전을 사용할 수 있습니다. [strcpy\_s, wcscpy\_s, \_mbscpy\_s](../../c-runtime-library/reference/strcpy-s-wcscpy-s-mbscpy-s.md)를 참조하세요.  
  
> [!IMPORTANT]
>  `_mbscpy`는 [!INCLUDE[wrt](../../atl/reference/includes/wrt_md.md)]에서 실행되는 응용 프로그램에서 사용할 수 없습니다.  자세한 내용은 [CRT 함수는 \/ZW 옵션을 지원하지 않음](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx)을 참조하세요.  
  
## 구문  
  
```  
char *strcpy(  
   char *strDestination,  
   const char *strSource   
);  
wchar_t *wcscpy(  
   wchar_t *strDestination,  
   const wchar_t *strSource   
);  
unsigned char *_mbscpy(  
   unsigned char *strDestination,  
   const unsigned char *strSource   
);  
template <size_t size>  
char *strcpy(  
   char (&strDestination)[size],  
   const char *strSource   
); // C++ only  
template <size_t size>  
wchar_t *wcscpy(  
   wchar_t (&strDestination)[size],  
   const wchar_t *strSource   
); // C++ only  
template <size_t size>  
unsigned char *_mbscpy(  
   unsigned char (&strDestination)[size],  
   const unsigned char *strSource   
); // C++ only  
```  
  
#### 매개 변수  
 `strDestination`  
 대상 문자열입니다.  
  
 `strSource`  
 Null 종료 소스 문자열입니다.  
  
## 반환 값  
 이러한 각 함수는 대상 문자열을 반환합니다.  반환 값 없음은 오류를 나타내는 데 예약되어 있습니다.  
  
## 설명  
 `strcpy` 함수는 null 종료 문자를 포함하여 `strSource`를 `strDestination`에 지정된 위치로 복사합니다.  소스 문자열과 대상 문자열이 겹치는 경우 `strcpy`의 동작이 정의되지 않습니다.  
  
> [!IMPORTANT]
>  `strcpy`는 `strSource`를 복사하기 전에 `strDestination`의 공간이 충분한지 확인하지 않으므로 버퍼 오버런의 잠재적 원인이 될 수 있습니다.  따라서 [strcpy\_s](../../c-runtime-library/reference/strcpy-s-wcscpy-s-mbscpy-s.md)를 대신 사용하는 것이 좋습니다.  
  
 `wcscpy` 및 `_mbscpy`는 각각 `strcpy`의 와이드 문자 및 멀티바이트 문자 버전입니다.  `wcscpy`의 인수 및 반환 값은 와이드 문자열이며 `_mbscpy`의 인수와 반환 값은 멀티바이트 문자열입니다.  그렇지 않으면 이들 세 함수는 동일하게 작동합니다.  
  
 C\+\+에서 이러한 함수는 보다 최신의 보안 대응 함수를 호출하는 템플릿 오버로드를 갖고 있습니다.  자세한 내용은 [안전한 템플릿 오버로드](../../c-runtime-library/secure-template-overloads.md)를 참조하세요.  
  
### 제네릭 텍스트 라우팅 매핑  
  
|TCHAR.H 루틴|\_UNICODE 및 \_MBCS 정의되지 않음|\_MBCS 정의됨|\_UNICODE 정의됨|  
|----------------|--------------------------------|----------------|-------------------|  
|`_tcscpy`|`strcpy`|`_mbscpy`|`wcscpy`|  
  
## 요구 사항  
  
|루틴|필수 헤더|  
|--------|-----------|  
|`strcpy`|\<string.h\>|  
|`wcscpy`|\<string.h\> 또는 \<wchar.h\>|  
|`_mbscpy`|\<mbstring.h\>|  
  
 호환성에 대한 자세한 내용은 [호환성](../../c-runtime-library/compatibility.md)을 참조하세요.  
  
## 예제  
  
```  
// crt_strcpy.c  
// compile with: /W3  
// This program uses strcpy  
// and strcat to build a phrase.  
  
#include <string.h>  
#include <stdio.h>  
  
int main( void )  
{  
   char string[80];  
  
   // If you change the previous line to  
   //   char string[20];  
   // strcpy and strcat will happily overrun the string  
   // buffer.  See the examples for strncpy and strncat  
   // for safer string handling.  
  
   strcpy( string, "Hello world from " ); // C4996  
   // Note: strcpy is deprecated; use strcpy_s instead  
   strcat( string, "strcpy " );           // C4996  
   // Note: strcat is deprecated; use strcat_s instead  
   strcat( string, "and " );              // C4996  
   strcat( string, "strcat!" );           // C4996  
   printf( "String = %s\n", string );  
}  
```  
  
  **String \= Hello world from strcpy and strcat\!**   
## 해당 .NET Framework 항목  
 [System::String::Copy](https://msdn.microsoft.com/en-us/library/system.string.copy.aspx)  
  
## 참고 항목  
 [문자열 조작](../../c-runtime-library/string-manipulation-crt.md)   
 [strcat, wcscat, \_mbscat](../../c-runtime-library/reference/strcat-wcscat-mbscat.md)   
 [strcmp, wcscmp, \_mbscmp](../../c-runtime-library/reference/strcmp-wcscmp-mbscmp.md)   
 [strncat, \_strncat\_l, wcsncat, \_wcsncat\_l, \_mbsncat, \_mbsncat\_l](../../c-runtime-library/reference/strncat-strncat-l-wcsncat-wcsncat-l-mbsncat-mbsncat-l.md)   
 [strncmp, wcsncmp, \_mbsncmp, \_mbsncmp\_l](../../c-runtime-library/reference/strncmp-wcsncmp-mbsncmp-mbsncmp-l.md)   
 [strncpy, \_strncpy\_l, wcsncpy, \_wcsncpy\_l, \_mbsncpy, \_mbsncpy\_l](../../c-runtime-library/reference/strncpy-strncpy-l-wcsncpy-wcsncpy-l-mbsncpy-mbsncpy-l.md)   
 [\_strnicmp, \_wcsnicmp, \_mbsnicmp, \_strnicmp\_l, \_wcsnicmp\_l, \_mbsnicmp\_l](../../c-runtime-library/reference/strnicmp-wcsnicmp-mbsnicmp-strnicmp-l-wcsnicmp-l-mbsnicmp-l.md)   
 [strrchr, wcsrchr, \_mbsrchr, \_mbsrchr\_l](../../c-runtime-library/reference/strrchr-wcsrchr-mbsrchr-mbsrchr-l.md)   
 [strspn, wcsspn, \_mbsspn, \_mbsspn\_l](../../c-runtime-library/reference/strspn-wcsspn-mbsspn-mbsspn-l.md)