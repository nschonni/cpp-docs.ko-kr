---
title: "binomial_distribution 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- binomial_distribution
- std::binomial_distribution
- random/std::binomial_distribution
- std::binomial_distribution::reset
- random/std::binomial_distribution::reset
- std::binomial_distribution::p
- random/std::binomial_distribution::p
- std::binomial_distribution::t
- random/std::binomial_distribution::t
- std::binomial_distribution::param
- random/std::binomial_distribution::param
- std::binomial_distribution::min
- random/std::binomial_distribution::min
- std::binomial_distribution::max
- random/std::binomial_distribution::max
- std::binomial_distribution::operator()
- random/std::binomial_distribution::operator()
- std::binomial_distribution::param_type
- random/std::binomial_distribution::param_type
- std::binomial_distribution::param_type::p
- random/std::binomial_distribution::param_type::p
- std::binomial_distribution::param_type::t
- random/std::binomial_distribution::param_type::t
- std::binomial_distribution::param_type::operator==
- random/std::binomial_distribution::param_type::operator==
- std::binomial_distribution::param_type::operator!=
- random/std::binomial_distribution::param_type::operator!=
dev_langs:
- C++
helpviewer_keywords:
- binomial_distribution class
ms.assetid: b7c8a26a-da8c-45a5-a3a8-208f7a3609ce
caps.latest.revision: 22
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
ms.sourcegitcommit: a937c9d083a7e4331af63323a19fb207142604a0
ms.openlocfilehash: 8b334da1953b67965c95c8c61e9426d9020132ed
ms.lasthandoff: 02/24/2017

---
# <a name="binomialdistribution-class"></a>binomial_distribution 클래스
이항 분포를 생성합니다.  
  
## <a name="syntax"></a>구문  
  
```  
template<class IntType = int>
class binomial_distribution  
   {  
public:  
   // types  
   typedef IntType result_type;  
   struct param_type;  
   
   // constructors and reset functions  
   explicit binomial_distribution(result_type t = 1, double p = 0.5);
   explicit binomial_distribution(const param_type& parm);
   void reset();
   
   // generating functions  
   template <class URNG>  
   result_type operator()(URNG& gen);
   template <class URNG>  
   result_type operator()(URNG& gen, const param_type& parm);
   
   // property functions  
   result_type t() const;
   double p() const;
   param_type param() const;
   void param(const param_type& parm);
   result_type min() const;
   result_type max() const;
   };  
```  
#### <a name="parameters"></a>매개 변수  
*IntType*  
정수 결과 형식으로, 기본적으로 `int`로 지정되어 있습니다. 가능한 형식은 [\<random>](../standard-library/random.md)를 참조하세요.  
  
*URNG* 균일 난수 생성기 엔진입니다. 가능한 형식은 [\<random>](../standard-library/random.md)를 참조하세요.  

## <a name="remarks"></a>설명  
이항 분포 이산 확률 함수에 따라 분포된 경우 템플릿 클래스는 사용자 지정 정수 형식 또는 아무 것도 제공되지 않았다면 `int` 형식의 값을 생성하는 분포를 설명합니다. 다음 테이블은 개별 멤버에 대한 문서와 연결되어 있습니다.  
  
||||  
|-|-|-|  
|[binomial_distribution::binomial_distribution](#binomial_distribution__binomial_distribution)|`binomial_distribution::t`|`binomial_distribution::param`|  
|`binomial_distribution::operator()`|`binomial_distribution::p`|[binomial_distribution::param_type](#binomial_distribution__param_type)|  
  
속성 멤버 `t()` 및 `p()`는 각각 현재 저장된 분포 매개 변수 값 `t` 및 `p`를 반환합니다.  
  
속성 멤버 `param()`은 `param_type`으로 저장된 분포 매개 변수 패키지를 설정하거나 반환합니다.  

`min()` 및 `max()` 구성원 함수는 각각 가능한 가장 작은 결과 및 가능한 가장 큰 결과를 반환합니다.  
  
`reset()` 구성원 함수는 캐시된 모든 값을 버립니다. 따라서 `operator()`에 대한 다음 호출의 결과는 호출 전 엔진에서 얻은 어떠한 값의 영향도 받지 않습니다.  
  
`operator()` 구성원 함수는 현재 매개 변수 패키지 또는 지정된 매개 변수 패키지에서 URNG 엔진을 기반으로 하여 다음에 생성된 값을 반환합니다.
  
분포 클래스 및 이러한 클래스의 멤버에 대한 자세한 내용은 [\<random>](../standard-library/random.md)을 참조하세요.  
  
이항 분포 이산 확률 함수에 대한 자세한 내용은 Wolfram MathWorld 문서 [이항 분포](http://go.microsoft.com/fwlink/LinkId=398469)를 참조하세요.  
  
## <a name="example"></a>예제  
  
```cpp  
// compile with: /EHsc /W4  
#include <random>   
#include <iostream>  
#include <iomanip>  
#include <string>  
#include <map>  
  
void test(const int t, const double p, const int& s) {  
  
    // uncomment to use a non-deterministic seed  
    //    std::random_device rd;  
    //    std::mt19937 gen(rd());  
    std::mt19937 gen(1729);  
  
    std::binomial_distribution<> distr(t, p);  
  
    std::cout << std::endl;  
    std::cout << "p == " << distr.p() << std::endl;  
    std::cout << "t == " << distr.t() << std::endl;  
  
    // generate the distribution as a histogram  
    std::map<int, int> histogram;  
    for (int i = 0; i < s; ++i) {  
        ++histogram[distr(gen)];  
    }  
  
    // print results  
    std::cout << "Histogram for " << s << " samples:" << std::endl;  
    for (const auto& elem : histogram) {  
        std::cout << std::setw(5) << elem.first << ' ' << std::string(elem.second, ':') << std::endl;  
    }  
    std::cout << std::endl;  
}  
  
int main()  
{  
    int    t_dist = 1;  
    double p_dist = 0.5;  
    int    samples = 100;  
  
    std::cout << "Use CTRL-Z to bypass data entry and run using default values." << std::endl;  
    std::cout << "Enter an integer value for t distribution (where 0 <= t): ";  
    std::cin >> t_dist;  
    std::cout << "Enter a double value for p distribution (where 0.0 <= p <= 1.0): ";  
    std::cin >> p_dist;  
    std::cout << "Enter an integer value for a sample count: ";  
    std::cin >> samples;  
  
    test(t_dist, p_dist, samples);  
}  
```  
  
첫 번째 실행:  
  
```Output  
Use CTRL-Z to bypass data entry and run using default values.  
Enter an integer value for t distribution (where 0 <= t): 22  
Enter a double value for p distribution (where 0.0 <= p <= 1.0): .25  
Enter an integer value for a sample count: 100  
 
p == 0.25  
t == 22  
Histogram for 100 samples:  
    1 :  
    2 ::  
    3 :::::::::::::  
    4 ::::::::::::::  
    5 :::::::::::::::::::::::::  
    6 ::::::::::::::::::  
    7 :::::::::::::  
    8 ::::::  
    9 ::::::  
    11 :  
    12 :  
```  
  
두 번째 실행:  
  
```Output  
Use CTRL-Z to bypass data entry and run using default values.  
Enter an integer value for t distribution (where 0 <= t): 22  
Enter a double value for p distribution (where 0.0 <= p <= 1.0): .5  
Enter an integer value for a sample count: 100  
 
p == 0.5  
t == 22  
Histogram for 100 samples:  
    6 :  
    7 ::  
    8 :::::::::  
    9 ::::::::::  
    10 ::::::::::::::::  
    11 :::::::::::::::::::  
    12 :::::::::::  
    13 :::::::::::::  
    14 :::::::::::::::  
    15 ::  
    16 ::  
```  
  
세 번째 실행:  
  
```Output  
Use CTRL-Z to bypass data entry and run using default values.  
Enter an integer value for t distribution (where 0 <= t): 22  
Enter a double value for p distribution (where 0.0 <= p <= 1.0): .75  
Enter an integer value for a sample count: 100  
 
p == 0.75  
t == 22  
Histogram for 100 samples:  
    13 ::::  
    14 :::::::::::  
    15 :::::::::::::::  
    16 :::::::::::::::::::::  
    17 ::::::::::::::  
    18 :::::::::::::::::  
    19 :::::::::::  
    20 ::::::  
    21 :  
```  
  
## <a name="requirements"></a>요구 사항  
**헤더:** \<random>  
  
**네임스페이스:** std  
  
##  <a name="a-namebinomialdistributionbinomialdistributiona--binomialdistributionbinomialdistribution"></a><a name="binomial_distribution__binomial_distribution"></a>  binomial_distribution::binomial_distribution  
분포를 생성합니다.  
  
```  
explicit binomial_distribution(result_type t = 1, double p = 0.5);
explicit binomial_distribution(const param_type& parm);
```  
  
### <a name="parameters"></a>매개 변수  
*t*  
`t` 분포 매개 변수입니다.  
  
*p*  
`p` 분포 매개 변수입니다.  
  
*parm*  
분포를 생성하는 데 사용되는 `param_type` 구조체입니다.  
  
### <a name="remarks"></a>설명  
**사전 조건:** `0 ≤ t` 및 `0.0 ≤ p ≤ 1.0`  
  
첫 번째 생성자는 저장된 `p` 값이 *p* 값을 보유하고 저장된 `t` 값이 *t* 값을 보유하고 있는 개체를 생성합니다.  
  
두 번째 생성자는 저장된 매개 변수가 *parm*에서 초기화되는 개체를 생성합니다. `param()` 멤버 함수를 호출하여 기존 분포의 현재 매개 변수를 가져와 설정할 수 있습니다.  
  
##  <a name="a-namebinomialdistributionparamtypea--binomialdistributionparamtype"></a><a name="binomial_distribution__param_type"></a>  binomial_distribution::param_type  
분포의 모든 매개 변수를 저장합니다.  
  
```cpp  
struct param_type {  
   typedef binomial_distribution<result_type> distribution_type;  
   param_type(result_type t = 1, double p = 0.5);
   result_type t() const;
   double p() const;
   .....  
   bool operator==(const param_type& right) const;
   bool operator!=(const param_type& right) const;
   };  
```  
  
### <a name="parameters"></a>매개 변수  
*t*  
`t` 분포 매개 변수입니다.  
  
*p*  
`p` 분포 매개 변수입니다.  
  
*right*  
 이 매개 변수와 비교할 `param_type` 개체입니다.  
  
### <a name="remarks"></a>설명  
**사전 조건:** `0 ≤ t` 및 `0.0 ≤ p ≤ 1.0`  
  
이 구조를 인스턴스화 시에는 분포의 클래스 생성자로, 기존 분포의 저장된 매개 변수를 설정하기 위해서는 `param()` 멤버 함수로, 저장된 매개 변수 대신 사용하기 위해서는 `operator()`로 전달할 수 있습니다.  
  
## <a name="see-also"></a>참고 항목  
 [\<random>](../standard-library/random.md)



