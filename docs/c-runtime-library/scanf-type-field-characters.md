---
title: "scanf 형식 필드 문자 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
apilocation:
- msvcr90.dll
- msvcr80.dll
- msvcr100.dll
- msvcr110_clr0400.dll
- msvcr110.dll
- msvcr120.dll
apitype: DLLExport
f1_keywords:
- scanf
dev_langs:
- C++
helpviewer_keywords:
- scanf function, type field characters
ms.assetid: 5d546a84-715b-44ca-b1c5-bbe997f9ff62
caps.latest.revision: 21
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
translationtype: Human Translation
ms.sourcegitcommit: aadbf7d2c6fece48ab29c1b818995464a790c38b
ms.openlocfilehash: 7a9d13924a14b51ed78256825dee6d9a59475c51
ms.lasthandoff: 03/07/2017

---
# <a name="scanf-type-field-characters"></a>scanf 형식 필드 문자
다음 정보는 `scanf` 와 같은 보안 버전을 비롯하여 함수의 모든 `scanf_s`패밀리에 적용됩니다.  
  
 `type` 문자는 요구되는 유일한 서식 지정 필드이며 선택적 서식 필드 뒤에 표시됩니다. `type` 문자는 관련된 인수가 문자, 문자열 또는 숫자로 해석되는지 여부를 결정합니다.  
  
### <a name="type-characters-for-scanf-functions"></a>Scanf 함수의 형식 문자  
  
|문자|필요한 입력 형식|인수의 형식|보안 버전의 크기 인수?|  
|---------------|----------------------------|----------------------|--------------------------------------|  
|`c`|문자. `scanf` 함수와 함께 사용될 때 단일 바이트 문자를 지정하고 `wscanf` 함수와 함께 사용될 때 와이드 문자를 지정합니다. `c` 가 지정되어 있으면 일반적으로 건너뛰는 공백 문자를 읽습니다. 공백이 아닌 싱글바이트 문자를 읽으려면 `%1s`를 사용하고 공백이 아닌 와이드 문자를 읽으려면 `%1ws`를 사용합니다.|`char` 함수와 함께 사용되는 경우 `scanf` 에 대한 포인터이고 `wchar_t` 함수와 함께 사용되는 경우 `wscanf` 에 대한 포인터입니다.|필수 요소. 크기에는 null 종결자를 위한 공간이 포함되어 있지 않습니다.|  
|`C`|반대 크기 문자. `scanf` 함수와 함께 사용될 때 와이드 문자를 지정하고, `wscanf` 함수와 함께 사용될 때 단일 바이트 문자를 지정합니다. `C` 가 지정되어 있으면 일반적으로 건너뛰는 공백 문자를 읽습니다. 공백이 아닌 싱글바이트 문자를 읽으려면 `%1s`를 사용하고 공백이 아닌 와이드 문자를 읽으려면 `%1ws`를 사용합니다.|`wchar_t` 함수와 함께 사용되는 경우 `scanf` 에 대한 포인터이고 `char` 함수와 함께 사용되는 경우 `wscanf` 에 대한 포인터입니다.|필수 요소. 크기 인수에는 null 종결자를 위한 공간이 포함되어 있지 않습니다.|  
|`d`|10진수 정수.|`int`에 대한 포인터입니다.|아니요.|  
|`i`|정수입니다. 입력 문자열이 "0x" 또는 "0X"로 시작하는 경우&16;진수이고 "0"으로 시작하는 경우&8;진수이며 그렇지 않은 경우에는&10;진수입니다.|`int`에 대한 포인터입니다.|아니요.|  
|`o`|8진수 정수.|`int`에 대한 포인터입니다.|아니요.|  
|`p`|16진수의 포인터 주소입니다. 읽을 최대 자릿수는 컴퓨터 아키텍처에 따라 달라지는 포인터의 크기(32비트 또는 64비트)에 따라 달라집니다. "0x" 또는 "0X"는 접두사로 허용됩니다.|`void*`에 대한 포인터입니다.|아니요.|  
|`u`|부호 없는&10;진수 정수.|`unsigned``int`에 대한 포인터입니다.|아니요.|  
|`x`|16진수 정수.|`int`에 대한 포인터입니다.|아니요.|  
|`e`, `E`, `f`, `F`, `g`, `G`|부동 소수점 값은 선택적 부호(+ 또는 -), 하나 이상의 일련의&10;진수(소수점 포함) 및 선택적으로 부호가 붙은 정수 값이 뒤에 오는 선택적 지수("e" 또는 "E")로 구성됩니다.|`float`에 대한 포인터입니다.|아니요.|  
|`a`, `A`|선택적인 소수점을 포함하는 일련의 하나 이상의&16;진수로 구성되는 부동 소수점 값과 뒤에&10;진수 값이 표시되는 지수("p" 또는 "P")입니다.|`float`에 대한 포인터입니다.|아니요.|  
|`n`|스트림 또는 버퍼에서 읽은 입력이 아닙니다.|`int`에 대한 포인터로, 여기에는 `scanf` 함수 또는 `wscanf` 함수에 대한 현재 호출에서 해당 시점까지 스트림 또는 버퍼에서 성공적으로 읽은 문자 수가 저장됩니다.|아니요.|  
|`s`|첫 번째 공백 문자(공백, 탭 또는 줄바꿈)까지의 문자열. 공백 문자로 구분되지 않는 문자열을 읽으려면 [scanf 너비 지정](../c-runtime-library/scanf-width-specification.md)에서 설명하는 것처럼 대괄호(`[ ]`)를 사용합니다.|`scanf` 함수와 함께 사용되는 경우 싱글바이트 문자 배열을 나타내고 `wscanf` 함수와 함께 사용되는 경우 와이드 문자 배열을 나타냅니다. 어떤 경우든 문자 배열은 입력 필드와 자동으로 추가되는 null 종결 문자가 포함될 수 있도록 충분히 커야 합니다.|필수 요소. 크기에는 null 종결자를 위한 공간이 포함되어 있습니다.|  
|`S`|첫 번째 공백 문자(공백, 탭 또는 줄바꿈)까지의 반대 크기 문자열. 공백 문자로 구분되지 않는 문자열을 읽으려면 [scanf 너비 지정](../c-runtime-library/scanf-width-specification.md)에서 설명하는 것처럼 대괄호(`[ ]`)를 사용합니다.|`scanf` 함수와 함께 사용되는 경우 와이드 문자 배열을 나타내고 `wscanf` 함수와 함께 사용되는 경우 싱글바이트 문자 배열을 나타냅니다. 어떤 경우든 문자 배열은 입력 필드와 자동으로 추가되는 null 종결 문자가 포함될 수 있도록 충분히 커야 합니다.|필수 요소. 크기에는 null 종결자를 위한 공간이 포함되어 있습니다.|  
  
  
 필요한 경우 크기 인수는 자신이 적용되는 인수 바로 뒤에 따라오는 매개 변수 목록에서 전달되어야 합니다. 예를 들어, 다음 코드는  
  
```  
char string1[11], string2[9];  
scanf_s("%10s %8s", string1, 11, string2, 9);  
```  
  
 최대 길이가 10인 문자열을 `string1`로 읽고 최대 길이가 8인 문자열을 `string2`로 읽습니다. 공백은 null 종결자를 위해 예약되어 있어야 하므로 버퍼 크기는 너비 지정보다 하나 이상 커야 합니다.  
  
 형식 문자열은 함수의 싱글바이트 문자 또는 와이드 문자 버전 사용 여부에 관계없이 싱글바이트 또는 와이드 문자 입력을 처리할 수 있습니다. 따라서 `scanf` 함수 및 `wscanf` 함수와 함께 싱글바이트 또는 와이드 문자를 읽으려면 다음과 같이 형식 지정자를 사용합니다.  
  
|문자를 읽을 형식|이 함수 사용|함께 사용할 형식 지정자|  
|--------------------------|-----------------------|----------------------------------|  
|싱글바이트|`scanf` 함수|`c`, `hc` 또는 `hC`|  
|싱글바이트|`wscanf` 함수|`C`, `hc` 또는 `hC`|  
|와이드|`wscanf` 함수|`c`, `lc` 또는 `lC`|  
|와이드|`scanf` 함수|`C`, `lc` 또는 `lC`|  
  
 `scanf` 함수 및 `wscanf` 함수를 사용하여 문자열을 검색하려면 `s` 및 `S` 대신 `c` 및 `C`형식 유형 지정자와 함께 위 테이블을 사용합니다.  
  
## <a name="see-also"></a>참고 항목  
 [scanf, _scanf_l, wscanf, _wscanf_l](../c-runtime-library/reference/scanf-scanf-l-wscanf-wscanf-l.md)