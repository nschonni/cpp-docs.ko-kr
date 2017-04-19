---
title: '&lt;utility&gt; | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- <utility>
- utility/std::<utility>
- std.<utility>
- std::<utility>
dev_langs:
- C++
helpviewer_keywords:
- utility header
ms.assetid: c4491103-5da9-47a1-9c2b-ed8bc64b0599
caps.latest.revision: 18
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
ms.sourcegitcommit: 41b445ceeeb1f37ee9873cb55f62d30d480d8718
ms.openlocfilehash: 67792e92a4a8336c025249a5d1322d00360a62c5
ms.lasthandoff: 02/24/2017

---
# <a name="ltutilitygt"></a>&lt;utility&gt;
두 개체를 하나인 것처럼 처리해야 할 때 유용한 개체 쌍을 생성 및 관리하는 데 도움이 되는 C++ 표준 라이브러리 형식, 함수 및 연산자를 정의합니다.  
  
## <a name="syntax"></a>구문  
  
```  
#include <utility>  
  
```  
  
## <a name="remarks"></a>설명  
 쌍은 C++ 표준 라이브러리에서 널리 사용됩니다. 쌍은 다양한 함수에 대한 인수 및 반환 값으로 필요하며, [map class](../standard-library/map-class.md) 및 [multimap class](../standard-library/multimap-class.md) 등의 컨테이너에 대한 요소 형식으로도 필요합니다. \<utility> 헤더는 키/값 쌍 형식 요소 관리를 지원하기 위해 자동으로 \<map>에 포함됩니다.  
  
### <a name="classes"></a>클래스  
  
|||  
|-|-|  
|[tuple_element](../standard-library/tuple-element-class-tuple.md)|`pair` 요소의 형식을 래핑하는 클래스입니다.|  
|[tuple_size](../standard-library/tuple-size-class-tuple.md)|`pair` 요소 수를 래핑하는 클래스입니다.|  
  
### <a name="functions"></a>함수  
  
|||  
|-|-|  
|[forward](../standard-library/utility-functions.md#forward)|완벽한 전달에 의해 가려지지 않도록 인수의 참조 형식(`lvalue` 또는 `rvalue` 중 하나)을 유지합니다.|  
|[get](../standard-library/utility-functions.md#get)|`pair` 개체에서 요소를 가져오는 함수입니다.|  
|[make_pair](../standard-library/utility-functions.md#make_pair)|`pair` 형식의 개체를 생성하는 데 사용되는 템플릿 도우미 함수입니다. 여기서 구성 요소 형식은 매개 변수로 전달된 데이터 형식을 기반으로 합니다.|  
|[move](../standard-library/utility-functions.md#move)|전달된 인수를 `rvalue` 참조로 반환합니다.|  
|[swap](../standard-library/utility-functions.md#swap)|두 `pair` 개체의 요소를 교환합니다.|  
  
### <a name="operators"></a>연산자  
  
|||  
|-|-|  
|[operator!=](../standard-library/utility-operators.md#operator_neq)|연산자의 좌변에 있는 pair 개체가 우변에 있는 pair 개체와 같지 않은지 테스트합니다.|  
|[operator==](../standard-library/utility-operators.md#operator_eq_eq)|연산자의 좌변에 있는 pair 개체가 우변에 있는 pair 개체와 같은지 테스트합니다.|  
|[operator<](../standard-library/utility-operators.md#operator_lt_)|연산자의 좌변에 있는 pair 개체가 우변에 있는 pair 개체보다 작은지 테스트합니다.|  
|[operator\<=](../standard-library/utility-operators.md#operator_lt__eq)|연산자의 좌변에 있는 pair 개체가 우변에 있는 pair 개체보다 작은지 테스트합니다.|  
|[operator>](../standard-library/utility-operators.md#operator_gt_)|연산자의 좌변에 있는 pair 개체가 우변에 있는 pair 개체보다 큰지 테스트합니다.|  
|[operator>=](../standard-library/utility-operators.md#operator_gt__eq)|연산자의 좌변에 있는 pair 개체가 우변에 있는 pair 개체보다 크거나 같은지 테스트합니다.|  
  
### <a name="structs"></a>구조체  
  
|||  
|-|-|  
|[identity](../standard-library/identity-structure.md)||  
|[pair](../standard-library/pair-structure.md)|두 개체를 단일 개체로 처리하는 기능을 제공하는 형식입니다.|  
  
## <a name="see-also"></a>참고 항목  
 [헤더 파일 참조](../standard-library/cpp-standard-library-header-files.md)   
 [C++ 표준 라이브러리의 스레드 보안](../standard-library/thread-safety-in-the-cpp-standard-library.md)



