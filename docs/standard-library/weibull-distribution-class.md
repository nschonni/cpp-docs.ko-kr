---
title: "weibull_distribution 클래스 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- weibull_distribution
- std::weibull_distribution
- random/std::weibull_distribution
- std::weibull_distribution::reset
- random/std::weibull_distribution::reset
- std::weibull_distribution::a
- random/std::weibull_distribution::a
- std::weibull_distribution::b
- random/std::weibull_distribution::b
- std::weibull_distribution::param
- random/std::weibull_distribution::param
- std::weibull_distribution::min
- random/std::weibull_distribution::min
- std::weibull_distribution::max
- random/std::weibull_distribution::max
- std::weibull_distribution::operator()
- random/std::weibull_distribution::operator()
- std::weibull_distribution::param_type
- random/std::weibull_distribution::param_type
- std::weibull_distribution::param_type::a
- random/std::weibull_distribution::param_type::a
- std::weibull_distribution::param_type::b
- random/std::weibull_distribution::param_type::b
- std::weibull_distribution::param_type::operator==
- random/std::weibull_distribution::param_type::operator==
- std::weibull_distribution::param_type::operator!=
- random/std::weibull_distribution::param_type::operator!=
dev_langs:
- C++
helpviewer_keywords:
- weibull_distribution class
ms.assetid: f20b49d3-1b9a-41af-8db4-baf800eaa02b
caps.latest.revision: 15
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
ms.sourcegitcommit: 491992306060125ab91d64560113f7f8a3b740b1
ms.openlocfilehash: 265754b7593a9654eab6f377d34d95268f1b9454
ms.lasthandoff: 02/24/2017

---
# <a name="weibulldistribution-class"></a>weibull_distribution 클래스
와이불 분포를 생성합니다.  
  
## <a name="syntax"></a>구문  
```  
class weibull_distribution  
   {  
   public: 
    // types  
   typedef RealType result_type;  
   struct param_type; 

    // constructor and reset functions  
   explicit weibull_distribution(result_type a = 1.0, result_type b = 1.0);
   explicit weibull_distribution(const param_type& parm);
   void reset();

   // generating functions  
   template <class URNG>  
      result_type operator()(URNG& gen);
   template <class URNG>  
      result_type operator()(URNG& gen, const param_type& parm);
   
   // property functions  
   result_type a() const;
   result_type b() const;
   param_type param() const;
   void param(const param_type& parm);
   result_type min() const;
   result_type max() const;
   };  
```   
#### <a name="parameters"></a>매개 변수  
*RealType*  
부동 소수점 결과 형식으로, 기본적으로 `double`로 지정되어 있습니다. 가능한 형식은 [\<random>](../standard-library/random.md)을 참조하세요.  
  
## <a name="remarks"></a>설명  
와이블 분포에 따라 분포된 경우 템플릿 클래스는 사용자 지정 부동 소수점 형식 또는 아무것도 제공되지 않았다면 `double` 형식의 값을 생성하는 분포를 설명합니다. 다음 테이블은 개별 멤버에 대한 문서와 연결되어 있습니다.  
  
||||  
|-|-|-|  
|[weibull_distribution::weibull_distribution](#weibull_distribution__weibull_distribution)|`weibull_distribution::a`|`weibull_distribution::param`|  
|`weibull_distribution::operator()`|`weibull_distribution::b`|[weibull_distribution::param_type](#weibull_distribution__param_type)|  
  
속성 함수 `a()` 및 `b()`는 저장된 분포 매개 변수인 *a* 및 *b* 각각에 대한 값을 반환합니다.  
  
속성 구성원 `param()`은 `param_type`으로 저장된 분포 매개 변수 패키지를 설정하거나 반환합니다.  

`min()` 및 `max()` 구성원 함수는 각각 가능한 가장 작은 결과 및 가능한 가장 큰 결과를 반환합니다.  
  
`reset()` 구성원 함수는 캐시된 모든 값을 버립니다. 따라서 `operator()`에 대한 다음 호출의 결과는 호출 전 엔진에서 얻은 어떠한 값의 영향도 받지 않습니다.  
  
`operator()` 구성원 함수는 현재 매개 변수 패키지 또는 지정된 매개 변수 패키지에서 URNG 엔진을 기반으로 하여 다음에 생성된 값을 반환합니다.
  
분포 클래스 및 이러한 클래스의 구성원에 대한 자세한 내용은 [\<random>](../standard-library/random.md)을 참조하세요.  
  
와이블 분포에 대한 자세한 내용은 Wolfram MathWorld 문서 [와이블 분포](http://go.microsoft.com/fwlink/LinkId=401115)를 참조하세요.  
  
## <a name="example"></a>예제  
  
```cpp  
// compile with: /EHsc /W4  
#include <random>   
#include <iostream>  
#include <iomanip>  
#include <string>  
#include <map>  
  
void test(const double a, const double b, const int s) {  
  
    // uncomment to use a non-deterministic generator  
    //    std::random_device gen;  
    std::mt19937 gen(1701);  
  
    std::weibull_distribution<> distr(a, b);  
  
    std::cout << std::endl;  
    std::cout << "min() == " << distr.min() << std::endl;  
    std::cout << "max() == " << distr.max() << std::endl;  
    std::cout << "a() == " << std::fixed << std::setw(11) << std::setprecision(10) << distr.a() << std::endl;  
    std::cout << "b() == " << std::fixed << std::setw(11) << std::setprecision(10) << distr.b() << std::endl;  
  
    // generate the distribution as a histogram  
    std::map<double, int> histogram;  
    for (int i = 0; i < s; ++i) {  
        ++histogram[distr(gen)];  
    }  
  
    // print results  
    std::cout << "Distribution for " << s << " samples:" << std::endl;  
    int counter = 0;  
    for (const auto& elem : histogram) {  
        std::cout << std::fixed << std::setw(11) << ++counter << ": "  
            << std::setw(14) << std::setprecision(10) << elem.first << std::endl;  
    }  
    std::cout << std::endl;  
}  
  
int main()  
{  
    double a_dist = 0.0;  
    double b_dist = 1;  
  
    int samples = 10;  
  
    std::cout << "Use CTRL-Z to bypass data entry and run using default values." << std::endl;  
    std::cout << "Enter a floating point value for the 'a' distribution parameter (must be greater than zero): ";  
    std::cin >> a_dist;  
    std::cout << "Enter a floating point value for the 'b' distribution parameter (must be greater than zero): ";  
    std::cin >> b_dist;  
    std::cout << "Enter an integer value for the sample count: ";  
    std::cin >> samples;  
  
    test(a_dist, b_dist, samples);  
}  
  
```  
  
## <a name="output"></a>출력  
 첫 번째 실행:  
  
```Output  
Use CTRL-Z to bypass data entry and run using default values.  
Enter a floating point value for the 'a' distribution parameter (must be greater than zero): 1  
Enter a floating point value for the 'b' distribution parameter (must be greater than zero): 1  
Enter an integer value for the sample count: 10  
 
min() == 0  
max() == 1.79769e+308  
a() == 1.0000000000  
b() == 1.0000000000  
Distribution for 10 samples:  
    1: 0.0936880533  
    2: 0.1225944894  
    3: 0.6443593183  
    4: 0.6551171649  
    5: 0.7313457551  
    6: 0.7313557977  
    7: 0.7590097389  
    8: 1.4466885214  
    9: 1.6434088411  
    10: 2.1201210996  
```  
  
 두 번째 실행:  
  
```Output  
Use CTRL-Z to bypass data entry and run using default values.  
Enter a floating point value for the 'a' distribution parameter (must be greater than zero): .5  
Enter a floating point value for the 'b' distribution parameter (must be greater than zero): 5.5  
Enter an integer value for the sample count: 10  
 
min() == 0  
max() == 1.79769e+308  
a() == 0.5000000000  
b() == 5.5000000000  
Distribution for 10 samples:  
    1: 0.0482759823  
    2: 0.0826617486  
    3: 2.2835941207  
    4: 2.3604817485  
    5: 2.9417663742  
    6: 2.9418471657  
    7: 3.1685268104  
    8: 11.5109922290  
    9: 14.8543594043  
    10: 24.7220241239  
```  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<random>  
  
 **네임스페이스:** std  
  
##  <a name="a-nameweibulldistributionweibulldistributiona--weibulldistributionweibulldistribution"></a><a name="weibull_distribution__weibull_distribution"></a>  weibull_distribution::weibull_distribution  
  
```  
explicit weibull_distribution(result_type a = 1.0, result_type b = 1.0);
explicit weibull_distribution(const param_type& parm);
```  
  
### <a name="parameters"></a>매개 변수  
*a*  
`a` 분포 매개 변수입니다.  
  
*b*  
`b` 분포 매개 변수입니다.  
  
*parm*  
분포를 생성하는 데 사용되는 `param_type` 구조체입니다.  
  
### <a name="remarks"></a>설명  
 **사전 조건:** `0.0 < a` 및 `0.0 < b`  
  
 첫 번째 생성자는 저장된 `a` 값이 *a* 값을 포함하며 저장된 `b` 값이 *b* 값을 포함하는 개체를 생성합니다.  
  
 두 번째 생성자는 저장된 매개 변수가 *parm*에서 초기화되는 개체를 생성합니다. `param()` 멤버 함수를 호출하여 기존 분포의 현재 매개 변수를 가져와 설정할 수 있습니다.  
  
##  <a name="a-nameweibulldistributionparamtypea--weibulldistributionparamtype"></a><a name="weibull_distribution__param_type"></a>  weibull_distribution::param_type  
 분포의 매개 변수를 저장합니다.  
```  
struct param_type {  
   typedef weibull_distribution<result_type> distribution_type;  
   param_type(result_type a = 1.0, result_type b = 1.0);
   result_type a() const;
   result_type b() const;

   bool operator==(const param_type& right) const;
   bool operator!=(const param_type& right) const;
   };  
```
### <a name="parameters"></a>매개 변수  
*a*  
`a` 분포 매개 변수입니다.  
  
*b*  
`b` 분포 매개 변수입니다.  
  
*right*  
이 매개 변수와 비교할 `param_type` 개체입니다.  
  
### <a name="remarks"></a>설명  
**사전 조건:** `0.0 < a` 및 `0.0 < b`  
  
이 구조를 인스턴스화 시에는 분포의 클래스 생성자로, 기존 분포의 저장된 매개 변수를 설정하기 위해서는 `param()` 멤버 함수로, 저장된 매개 변수 대신 사용하기 위해서는 `operator()`로 전달할 수 있습니다.  
  
## <a name="see-also"></a>참고 항목  
 [\<random>](../standard-library/random.md)



