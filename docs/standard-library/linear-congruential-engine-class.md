---
title: "linear_congruential_engine 클래스 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "std.tr1.linear_congruential_engine"
  - "random/std::tr1::linear_congruential_engine"
  - "linear_congruential_engine"
  - "std::tr1::linear_congruential_engine"
  - "tr1.linear_congruential_engine"
  - "tr1::linear_congruential_engine"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "linear_congruential_engine 클래스"
ms.assetid: 30e00ca6-1933-4701-9561-54f3e810a5a1
caps.latest.revision: 21
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 21
---
# linear_congruential_engine 클래스
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

선형 합동 알고리즘에 따라 임의 시퀀스를 생성합니다.  
  
## 구문  
  
```  
template<class UIntType, UIntType A, UIntType C, UIntType M>  
class linear_congruential_engine{  
public:  
    // types  
    typedef UIntType result_type;  
  
    // engine characteristics  
    static constexpr result_type multiplier = a;  
    static constexpr result_type increment = c;  
    static constexpr result_type modulus = m;  
    static constexpr result_type min() { return c == 0u ? 1u: 0u; }  
    static constexpr result_type max() { return m - 1u; }  
    static constexpr result_type default_seed = 1u;  
  
    // constructors and seeding functions  
    explicit linear_congruential_engine(result_type s = default_seed);  
    template<class Sseq> explicit linear_congruential_engine(Sseq& q);  
    void seed(result_type s = default_seed);  
    template<class Sseq> void seed(Sseq& q);  
  
    // generating functions  
    result_type operator()();  
    void discard(unsigned long long z);  
};  
```  
  
#### 매개 변수  
 `UIntType`  
 부호가 없는 정수 결과 형식입니다. 가능한 형식에 대 한 참조 [\<random\>](../standard-library/random.md)합니다.  
  
 `A`  
 **승수**입니다.**사전 조건**: 설명 섹션을 참조하세요.  
  
 `C`  
 **증분**입니다.**사전 조건**: 설명 섹션을 참조하세요.  
  
 `M`  
 **모듈러스**입니다.**사전 조건**: 설명을 참조하세요.  
  
## 멤버  
  
||||  
|-|-|-|  
|`linear_congruential_engine::linear_congruential_engine`|`linear_congruential_engine::min`|`linear_congruential_engine::discard`|  
|`linear_congruential_engine::operator()`|`linear_congruential_engine::max`|`linear_congruential_engine::seed`|  
  
 `default_seed`는 `1u`로 정의된 멤버 상수로, `linear_congruential_engine::seed` 및 단일 값 생성자의 기본 매개 변수 값으로 사용됩니다.  
  
 엔진 멤버에 대 한 자세한 내용은 참조 [\<random\>](../standard-library/random.md)합니다.  
  
## 설명  
 `linear_congruential_engine` 템플릿 클래스는 가장 단순한 생성기 엔진이지만 가장 빠르거나 품질이 가장 뛰어나지는 않습니다. 이 엔진을 개선한 것이 [substract\_with\_carry\_engine](../standard-library/subtract-with-carry-engine-class.md)입니다. 이러한 엔진 둘 다 [mersenne\_twister\_engine](../standard-library/mersenne-twister-engine-class.md)만큼 빠르거나 품질 결과가 뛰어나지는 않습니다.  
  
 이 엔진은 되풀이 관계\(*기간*\)를 사용하여 사용자가 지정한 부호가 없는 정수 형식을 생성합니다. `x(i) = (A * x(i-1) + C) mod M`  
  
 `M`이 0이면 이 모듈러스 연산에 사용되는 값은 `numeric_limits<result_type>::max() + 1`입니다. 엔진의 상태는 반환되는 마지막 값이거나 `operator()`를 호출하지 않은 경우에는 시드 값입니다.  
  
 `M`이 0이 아니면 템플릿 인수 `A`와 `C`의 값이 `M`보다 작아야 합니다.  
  
 이 엔진 생성기에서 직접 생성할 수 있지만 이러한 미리 정의 된 typedef 중 하나 에서도 사용할 수 있습니다.  
  
 `minstd_rand0`: 1988 최소 표준 엔진입니다 \(Lewis, Goodman 및 Miller, 1969\).  
  
```  
typedef linear_congruential_engine<unsigned int, 16807, 0, 2147483647> minstd_rand0;  
```  
  
 `minstd_rand`: 업데이트 된 최소 표준 엔진 `minstd_rand0` \(Park, Miller 및 Stockmeyer, 1993\).  
  
```  
typedef linear_congruential_engine<unsigned int, 48271, 0, 2147483647> minstd_rand;  
```  
  
 선형 합동 엔진 알고리즘에 대 한 자세한 내용은 Wikipedia 문서를 참조 하십시오. [선형 합동 발생기](http://go.microsoft.com/fwlink/?LinkId=402446)합니다.  
  
## 요구 사항  
 **헤더:** \<random\>  
  
 **네임스페이스:** std  
  
## 참고 항목  
 [\<random\>](../standard-library/random.md)