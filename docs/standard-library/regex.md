---
title: '&lt;regex&gt; | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- <regex>
dev_langs:
- C++
helpviewer_keywords:
- regex header
ms.assetid: 5dd4ef74-6063-4dbc-b692-1960bb736f0b
caps.latest.revision: 23
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
translationtype: Machine Translation
ms.sourcegitcommit: 248e9ba676b906af62f6804f4939e04158a8e2ef
ms.openlocfilehash: 4e172f8bf72fd528027c333cf411a307aa97d786
ms.lasthandoff: 02/24/2017

---
# <a name="ltregexgt"></a>&lt;regex&gt;
[정규식(C++)](../standard-library/regular-expressions-cpp.md)을 구문 분석하는 템플릿 클래스와 텍스트에서 정규식 개체와 일치하는 항목을 검색하는 여러 템플릿 클래스 및 함수를 정의합니다.  
  
## <a name="syntax"></a>구문  
  
```  
#include <regex>  
```  
  
## <a name="remarks"></a>설명  
 정규식 개체를 만들려면 템플릿 클래스 [basic_regex 클래스](../standard-library/basic-regex-class.md) 또는 해당 특수화 [regex](../standard-library/regex-typedefs.md#regex_typedef) 및 [wregex](../standard-library/regex-typedefs.md#wregex_typedef) 중 하나를 [regex_constants::syntax_option_type](../standard-library/regex-constants-class.md#regex_constants__syntax_option_type) 형식의 구문 플래그와 함께 사용합니다.  
  
 텍스트에서 정규식 개체와 일치하는 항목을 검색하려면 템플릿 함수 [regex_match 함수](../standard-library/regex-functions.md#regex_match_function) 및 [regex_search 함수](../standard-library/regex-functions.md#regex_search_function)를 [regex_constants::match_flag_type](../standard-library/regex-constants-class.md#regex_constants__match_flag_type) 형식의 일치 플래그와 함께 사용합니다. 이러한 함수는 템플릿 클래스 [match_results 클래스](../standard-library/match-results-class.md)와 해당 특수화 [cmatch](../standard-library/regex-typedefs.md#cmatch_typedef), [wcmatch](../standard-library/regex-typedefs.md#wcmatch_typedef), [smatch](../standard-library/regex-typedefs.md#smatch_typedef) 및 [wsmatch](../standard-library/regex-typedefs.md#wsmatch_typedef)를 템플릿 클래스 [sub_match 클래스](../standard-library/sub-match-class.md)와 해당 특수화 [csub_match](../standard-library/regex-typedefs.md#csub_match_typedef), [wcsub_match](../standard-library/regex-typedefs.md#wcsub_match_typedef), [ssub_match](../standard-library/regex-typedefs.md#ssub_match_typedef) 및 [wssub_match](../standard-library/regex-typedefs.md#wssub_match_typedef)와 함께 사용하여 결과를 반환합니다.  
  
 정규식 개체와 일치하는 텍스트를 바꾸려면 템플릿 함수 [regex_replace 함수](../standard-library/regex-functions.md#regex_replace_function)를 [regex_constants::match_flag_type](../standard-library/regex-constants-class.md#regex_constants__match_flag_type) 형식의 일치 플래그와 함께 사용합니다.  
  
 정규식 개체의 여러 일치 항목을 반복하려면 템플릿 클래스 [regex_iterator 클래스](../standard-library/regex-iterator-class.md) 및 [regex_token_iterator 클래스](../standard-library/regex-token-iterator-class.md) 또는 해당 특수화 [cregex_iterator](../standard-library/regex-typedefs.md#cregex_iterator_typedef), [sregex_iterator](../standard-library/regex-typedefs.md#sregex_iterator_typedef), [wcregex_iterator](../standard-library/regex-typedefs.md#wcregex_iterator_typedef), [wsregex_iterator](../standard-library/regex-typedefs.md#wsregex_iterator_typedef), [cregex_token_iterator](../standard-library/regex-typedefs.md#cregex_token_iterator_typedef), [sregex_token_iterator](../standard-library/regex-typedefs.md#sregex_token_iterator_typedef), [wcregex_token_iterator](../standard-library/regex-typedefs.md#wcregex_token_iterator_typedef), 또는 [wsregex_token_iterator](../standard-library/regex-typedefs.md#wsregex_token_iterator_typedef) 중 하나를 [regex_constants::match_flag_type](../standard-library/regex-constants-class.md#regex_constants__match_flag_type) 형식의 일치 플래그와 함께 사용합니다.  
  
 정규식의 문법에 대한 세부 정보를 수정하려면 정규식 특성을 구현하는 클래스를 작성합니다.  
  
### <a name="classes"></a>클래스  
  
|||  
|-|-|  
|[basic_regex](../standard-library/basic-regex-class.md)|정규식을 래핑합니다.|  
|[match_results](../standard-library/match-results-class.md)|부분 일치 시퀀스를 보유합니다.|  
|[regex_constants](../standard-library/regex-constants-class.md)|분류된 상수를 보유합니다.|  
|[regex_error](../standard-library/regex-error-class.md)|잘못된 정규식을 보고합니다.|  
|[regex_iterator](../standard-library/regex-iterator-class.md)|일치 결과를 반복합니다.|  
|[regex_traits](../standard-library/regex-traits-class.md)|일치를 위해 요소의 특징을 설명합니다.|  
|[regex_traits\<char>](../standard-library/regex-traits-char-class.md)|일치를 위해 `char`의 특징을 설명합니다.|  
|[regex_traits<wchar_t>](../standard-library/regex-traits-wchar-t-class.md)|일치를 위해 `wchar_t`의 특징을 설명합니다.|  
|[regex_token_iterator](../standard-library/regex-token-iterator-class.md)|부분 일치를 반복합니다.|  
|[sub_match](../standard-library/sub-match-class.md)|부분 일치를 설명합니다.|  
  
### <a name="type-definitions"></a>형식 정의  
  
|||  
|-|-|  
|[cmatch](../standard-library/regex-typedefs.md#cmatch_typedef)|`char``match_results`에 대한 형식 정의입니다.|  
|[cregex_iterator](../standard-library/regex-typedefs.md#cregex_iterator_typedef)|`char``regex_iterator`에 대한 형식 정의입니다.|  
|[cregex_token_iterator](../standard-library/regex-typedefs.md#cregex_token_iterator_typedef)|`char``regex_token_iterator`에 대한 형식 정의입니다.|  
|[csub_match](../standard-library/regex-typedefs.md#csub_match_typedef)|`char``sub_match`에 대한 형식 정의입니다.|  
|[regex](../standard-library/regex-typedefs.md#regex_typedef)|`char``basic_regex`에 대한 형식 정의입니다.|  
|[smatch](../standard-library/regex-typedefs.md#smatch_typedef)|`string``match_results`에 대한 형식 정의입니다.|  
|[sregex_iterator](../standard-library/regex-typedefs.md#sregex_iterator_typedef)|`string``regex_iterator`에 대한 형식 정의입니다.|  
|[sregex_token_iterator](../standard-library/regex-typedefs.md#sregex_token_iterator_typedef)|`string``regex_token_iterator`에 대한 형식 정의입니다.|  
|[ssub_match](../standard-library/regex-typedefs.md#ssub_match_typedef)|`string``sub_match`에 대한 형식 정의입니다.|  
|[wcmatch](../standard-library/regex-typedefs.md#wcmatch_typedef)|`wchar_t``match_results`에 대한 형식 정의입니다.|  
|[wcregex_iterator](../standard-library/regex-typedefs.md#wcregex_iterator_typedef)|`wchar_t``regex_iterator`에 대한 형식 정의입니다.|  
|[wcregex_token_iterator](../standard-library/regex-typedefs.md#wcregex_token_iterator_typedef)|`wchar_t``regex_token_iterator`에 대한 형식 정의입니다.|  
|[wcsub_match](../standard-library/regex-typedefs.md#wcsub_match_typedef)|`wchar_t``sub_match`에 대한 형식 정의입니다.|  
|[wregex](../standard-library/regex-typedefs.md#wregex_typedef)|`wchar_t``basic_regex`에 대한 형식 정의입니다.|  
|[wsmatch](../standard-library/regex-typedefs.md#wsmatch_typedef)|`wstring``match_results`에 대한 형식 정의입니다.|  
|[wsregex_iterator](../standard-library/regex-typedefs.md#wsregex_iterator_typedef)|`wstring``regex_iterator`에 대한 형식 정의입니다.|  
|[wsregex_token_iterator](../standard-library/regex-typedefs.md#wsregex_token_iterator_typedef)|`wstring``regex_token_iterator`에 대한 형식 정의입니다.|  
|[wssub_match](../standard-library/regex-typedefs.md#wssub_match_typedef)|`wstring``sub_match`에 대한 형식 정의입니다.|  
  
### <a name="functions"></a>함수  
  
|||  
|-|-|  
|[regex_match](../standard-library/regex-functions.md#regex_match_function)|정규식과 정확히 일치합니다.|  
|[regex_replace](../standard-library/regex-functions.md#regex_replace_function)|일치하는 정규식을 바꿉니다.|  
|[regex_search](../standard-library/regex-functions.md#regex_search_function)|정규식 일치 항목을 검색합니다.|  
|[swap](../standard-library/regex-functions.md#swap_function)|`basic_regex` 또는 `match_results` 개체를 교환합니다.|  
  
### <a name="operators"></a>연산자  
  
|||  
|-|-|  
|[operator==](../standard-library/regex-operators.md#operator_eq_eq)|다양한 개체가 같은지 비교합니다.|  
|[operator!=](../standard-library/regex-operators.md#operator_neq)|다양한 개체가 같지 않은지 비교합니다.|  
|[operator<](../standard-library/regex-operators.md#operator_lt_)|다양한 개체가 보다 작은지 비교합니다.|  
|[operator\<=](../standard-library/regex-operators.md#operator_lt__eq)|다양한 개체가 보다 작거나 같은지 비교합니다.|  
|[operator>](../standard-library/regex-operators.md#operator_gt_)|다양한 개체가 보다 큰지 비교합니다.|  
|[operator>=](../standard-library/regex-operators.md#operator_gt__eq)|다양한 개체가 보다 크거나 같은지 비교합니다.|  
|[operator<<](../standard-library/regex-operators.md#operator_lt__lt_)|스트림에 `sub_match`를 삽입합니다.|  
  
## <a name="see-also"></a>참고 항목  
[정규식(C++)](../standard-library/regular-expressions-cpp.md)  
[regex_constants 클래스](../standard-library/regex-constants-class.md)  
[regex_error 클래스](../standard-library/regex-error-class.md)  
[\<regex> 함수](../standard-library/regex-functions.md)  
[regex_iterator 클래스](../standard-library/regex-iterator-class.md)  
[\<regex> 연산자](../standard-library/regex-operators.md)  
[regex_token_iterator 클래스](../standard-library/regex-token-iterator-class.md)  
[regex_traits 클래스](../standard-library/regex-traits-class.md)  
[\<regex> 형식 정의](../standard-library/regex-typedefs.md)  



