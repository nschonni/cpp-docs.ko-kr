---
title: "strtoimax, _strtoimax_l, wcstoimax, _wcstoimax_l | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
apiname: 
  - "wcstoimax"
  - "_wcstoimax_l"
  - "_strtoimax_l"
  - "strtoimax"
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
  - "api-ms-win-crt-convert-l1-1-0.dll"
apitype: "DLLExport"
f1_keywords: 
  - "wcstoimax"
  - "_tcstoimax"
  - "strtoimax"
  - "_wcstoimax_l"
  - "_strtoimax_l"
  - "_tcstoimax_l"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "_strtoimax_l 함수"
  - "_wcstoimax_l 함수"
  - "변환 함수"
  - "strtoimax 함수"
  - "wcstoimax 함수"
ms.assetid: 4530d3dc-aaac-4a76-b7cf-29ae3c98d0ae
caps.latest.revision: 5
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 5
---
# strtoimax, _strtoimax_l, wcstoimax, _wcstoimax_l
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

문자열을 부호 있는 정수 형식의 최대 지원 정수 값으로 변환합니다.  
  
## 구문  
  
```  
intmax_t strtoimax(  
   const char *nptr,  
   char **endptr,  
   int base   
);  
intmax_t wcstoimax(  
   const wchar_t *nptr,  
   wchar_t **endptr,  
   int base   
);  
intmax_t _strtoimax_l(  
   const char *nptr,  
   char **endptr,  
   int base,  
   _locale_t locale  
);  
intmax_t _wcstoimax_l(  
   const wchar_t *nptr,  
   wchar_t **endptr,  
   int base,  
   _locale_t locale  
);  
```  
  
#### 매개 변수  
 `nptr`  
 변환할 Null 종료 문자열입니다.  
  
 `endptr`  
 검색을 중지하는 문자에 대한 포인터입니다.  
  
 `base`  
 사용할 번호 기준입니다.  
  
 `locale`  
 사용할 로캘입니다.  
  
## 반환 값  
 `strtoimax`는 오버플로가 발생되는 시기를 제외하고 `nptr` 문자열을 나타내는 값을 반환합니다. 이런 경우 `INTMAX_MAX` 또는 `INTMAX_MIN`, 및 `errno`는 `ERANGE`를 반환하도록 설정됩니다.  변환을 수행할 수 없는 경우 함수는 0을 반환합니다.  `wcstoimax`이 analogously 값을 `strtoimax`에 반환 합니다.  
  
 `INTMAX_MAX` 및 `INTMAX_MIN`은 stdint.h에 정의되어 있습니다.  
  
 `nptr`이 `NULL`이 되거나 `base`가 0이 아니고 2보다 작거나 36보다는 클 경우 `errno`는 `EINVAL`로 설정됩니다.  
  
 반환 코드에 대한 자세한 내용은 [errno, \_doserrno, \_sys\_errlist 및 \_sys\_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md)를 참조하십시오.  
  
## 설명  
 `strtoimax` 함수는 `nptr`을 `intmax_t`로 변환합니다.  `strtoimax`는 `wcstoimax`의 와이드 문자 버전이며, `nptr` 인수는 와이드 문자 문자열입니다.  그렇지 않으면 이러한 함수는 동일하게 작동합니다.  두 함수 모두 숫자 부분으로 인식할 수 없는 첫 번째 문자에서 문자열 `nptr`를 중단합니다.  이는 null 종결 문자일 수 있거나 `base` 보다 크거나 동일한 첫 번째 숫자일 수 있습니다.  
  
 로캘의 `LC_NUMERIC` 범주 설정은 `nptr`에서 기수 문자 인식 여부를 결정합니다. 자세한 내용은 [setlocale, \_wsetlocale](../../c-runtime-library/reference/setlocale-wsetlocale.md)을 참조하십시오.  `_l` 접미사가 없는 함수는 현재 로캘을 사용합니다. `_strtoimax_l`과 `_wcstoimax_l`은 전달되는 로캘을 대신 사용한다는 점을 제외하면 `_l` 접미사가 없는 해당 함수와 동일합니다.  자세한 내용은 [로캘](../../c-runtime-library/locale.md)을 참조하십시오.  
  
 `endptr`이 `NULL`이 아닌 경우 검색을 중지시키는 문자에 대한 포인터는 `endptr`가 가리키는 위치에 저장됩니다.  변환을 수행할 수 없는 경우\(유효 숫자를 찾을 수 없거나 잘못된 기준이 지정됨\) `nptr`의 값은 `endptr`가 가리키는 위치에 저장됩니다.  
  
### 제네릭 텍스트 라우팅 매핑  
  
|TCHAR.H 루틴|\_UNICODE 및 \_MBCS 정의되지 않음|\_MBCS 정의됨|\_UNICODE 정의됨|  
|----------------|--------------------------------|----------------|-------------------|  
|`_tcstoimax`|`strtoimax`|`strtoimax`|`wcstoimax`|  
|`_tcstoimax_l`|`strtoimax_l`|`_strtoimax_l`|`_wcstoimax_l`|  
  
 `strtoimax`에서는 다음 양식의 문자열을 가리키는 `nptr`를 예상합니다.  
  
 \[`whitespace`\] \[{`+` &#124; `–`}\] \[`0` \[{ `x` &#124; `X` }\]\] \[`digits` &#124; `letters`\]  
  
 `whitespace`는 무시되는 공백 및 탭 문자를 포함할 수 있으며 `digits`는 하나 이상의 10진수입니다. `letters`는 문자 'a' ~ 'z'\(또는 'A' ~ 'Z'\)입니다.  이 폼에 맞지 않는 첫 번째 문자는 검색을 중지합니다.  `base`가 2와 36 사이에 있으면 번호의 기준으로 사용됩니다.  `base`가 0이 되는 경우 `nptr`가 지시하는 문자열의 최초 문자가 베이스 결정에 사용됩니다.  첫 번째 문자가 '0'이고 두 번째 문자가 'x' 또는 'X'인 경우 문자열은 8진수 정수로 해석됩니다.  첫 번째 문자가 '0'이고 두 번째 문자가 'x' 또는 'X'인 경우 문자열은 16진수 정수로 해석됩니다.  첫 번째 문자가 '1'부터 '9'이면 문자열은 10진수로 해석됩니다.  문자 'a'부터 'z'\(또는 'A'부터 'Z'\)는 10\-35 값이 할당됩니다. 즉, 할당된 값이 `base` 보다 작은 문자만이 허용됩니다.  기준 범위를 벗어나는 첫 번째 문자는 검색을 중지합니다.  예를 들어 `base`가 0이 되어 검색된 첫 번째 문자가 '0'이 되는 경우 8진수 정수를 정하여 '8' 이나 '9' 로 검색이 중지될 수 있습니다.  
  
## 요구 사항  
  
|루틴|필수 헤더|  
|--------|-----------|  
|`strtoimax`, `_strtoimax_l`, `wcstoimax`, `_wcstoimax_l`|\<inttypes.h\>|  
  
 호환성에 대한 자세한 내용은 [호환성](../../c-runtime-library/compatibility.md)을 참조하십시오.  
  
## 참고 항목  
 [데이터 변환](../../c-runtime-library/data-conversion.md)   
 [로캘](../../c-runtime-library/locale.md)   
 [localeconv](../../c-runtime-library/reference/localeconv.md)   
 [setlocale, \_wsetlocale](../../c-runtime-library/reference/setlocale-wsetlocale.md)   
 [문자열을 숫자 값으로 변환하는 함수](../../c-runtime-library/string-to-numeric-value-functions.md)   
 [strtod, \_strtod\_l, wcstod, \_wcstod\_l](../../c-runtime-library/reference/strtod-strtod-l-wcstod-wcstod-l.md)   
 [strtol, wcstol, \_strtol\_l, \_wcstol\_l](../../c-runtime-library/reference/strtol-wcstol-strtol-l-wcstol-l.md)   
 [strtoul, \_strtoul\_l, wcstoul, \_wcstoul\_l](../../c-runtime-library/reference/strtoul-strtoul-l-wcstoul-wcstoul-l.md)   
 [strtoumax, \_strtoumax\_l, wcstoumax, \_wcstoumax\_l](../../c-runtime-library/reference/strtoumax-strtoumax-l-wcstoumax-wcstoumax-l.md)   
 [atof, \_atof\_l, \_wtof, \_wtof\_l](../../c-runtime-library/reference/atof-atof-l-wtof-wtof-l.md)