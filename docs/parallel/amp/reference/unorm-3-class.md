---
title: "unorm_3 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- amp_short_vectors/Concurrency::graphics::unorm_3::set_zy
- amp_short_vectors/Concurrency::graphics::unorm_3::zxy
- amp_short_vectors/Concurrency::graphics::unorm_3::set_zyx
- amp_short_vectors/Concurrency::graphics::unorm_3::operator-=
- amp_short_vectors/Concurrency::graphics::unorm_3::xzy
- amp_short_vectors/Concurrency::graphics::unorm_3::get_xzy
- amp_short_vectors/Concurrency::graphics::unorm_3::zyx
- amp_short_vectors/Concurrency::graphics::unorm_3::rgb
- amp_short_vectors/Concurrency::graphics::unorm_3::set_xz
- amp_short_vectors/Concurrency::graphics::unorm_3::set_yxz
- amp_short_vectors/Concurrency::graphics::unorm_3::set_yx
- amp_short_vectors/Concurrency::graphics::unorm_3::br
- amp_short_vectors/Concurrency::graphics::unorm_3::get_zy
- amp_short_vectors/Concurrency::graphics::unorm_3::set_zx
- amp_short_vectors/Concurrency::graphics::unorm_3::get_xyz
- amp_short_vectors/Concurrency::graphics::unorm_3::b
- amp_short_vectors/Concurrency::graphics::unorm_3::set_xyz
- amp_short_vectors/Concurrency::graphics::unorm_3
- amp_short_vectors/Concurrency::graphics::unorm_3::set_z
- amp_short_vectors/Concurrency::graphics::unorm_3::set_xy
- amp_short_vectors/Concurrency::graphics::unorm_3::get_zyx
- amp_short_vectors/Concurrency::graphics::unorm_3::get_xy
- amp_short_vectors/Concurrency::graphics::unorm_3::x
- amp_short_vectors/Concurrency::graphics::unorm_3::get_zxy
- amp_short_vectors/Concurrency::graphics::unorm_3::z
- amp_short_vectors/Concurrency::graphics::unorm_3::get_x
- amp_short_vectors/Concurrency::graphics::unorm_3::operator=
- amp_short_vectors/Concurrency::graphics::unorm_3::yxz
- amp_short_vectors/Concurrency::graphics::unorm_3::get_yx
- amp_short_vectors/Concurrency::graphics::unorm_3::gbr
- amp_short_vectors/Concurrency::graphics::unorm_3::get_yxz
- amp_short_vectors/Concurrency::graphics::unorm_3::operator--
- amp_short_vectors/Concurrency::graphics::unorm_3::operator/=
- amp_short_vectors/Concurrency::graphics::unorm_3::brg
- amp_short_vectors/Concurrency::graphics::unorm_3::gb
- amp_short_vectors/Concurrency::graphics::unorm_3::zy
- amp_short_vectors/Concurrency::graphics::unorm_3::set_xzy
- amp_short_vectors/Concurrency::graphics::unorm_3::get_yzx
- amp_short_vectors/Concurrency::graphics::unorm_3::rb
- amp_short_vectors/Concurrency::graphics::unorm_3::gr
- amp_short_vectors/Concurrency::graphics::unorm_3::zx
- amp_short_vectors/Concurrency::graphics::unorm_3::r
- amp_short_vectors/Concurrency::graphics::unorm_3::xyz
- amp_short_vectors/Concurrency::graphics::unorm_3::grb
- amp_short_vectors/Concurrency::graphics::unorm_3::bg
- amp_short_vectors/Concurrency::graphics::unorm_3::get_y
- amp_short_vectors/Concurrency::graphics::unorm_3::g
- amp_short_vectors/Concurrency::graphics::unorm_3::yz
- amp_short_vectors/Concurrency::graphics::unorm_3::yx
- amp_short_vectors/Concurrency::graphics::unorm_3::get_xz
- amp_short_vectors/Concurrency::graphics::unorm_3::set_zxy
- amp_short_vectors/Concurrency::graphics::unorm_3::get_z
- amp_short_vectors/Concurrency::graphics::unorm_3::bgr
- amp_short_vectors/Concurrency::graphics::unorm_3::set_x
- amp_short_vectors/Concurrency::graphics::unorm_3::operator-
- amp_short_vectors/Concurrency::graphics::unorm_3::y
- amp_short_vectors/Concurrency::graphics::unorm_3::set_yzx
- amp_short_vectors/Concurrency::graphics::unorm_3::get_zx
- amp_short_vectors/Concurrency::graphics::unorm_3::yzx
- amp_short_vectors/Concurrency::graphics::unorm_3::operator++
- amp_short_vectors/Concurrency::graphics::unorm_3::set_yz
- amp_short_vectors/Concurrency::graphics::unorm_3::operator+=
- amp_short_vectors/Concurrency::graphics::unorm_3::xz
- amp_short_vectors/Concurrency::graphics::unorm_3::rg
- amp_short_vectors/Concurrency::graphics::unorm_3::xy
- amp_short_vectors/Concurrency::graphics::unorm_3::operator*=
- amp_short_vectors/Concurrency::graphics::unorm_3::set_y
- amp_short_vectors/Concurrency::graphics::unorm_3::get_yz
- amp_short_vectors/Concurrency::graphics::unorm_3::rbg
dev_langs:
- C++
ms.assetid: ea4e7a17-5256-464c-af28-8b01962564c0
caps.latest.revision: 10
author: mikeblome
ms.author: mblome
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
ms.sourcegitcommit: 5faef5bd1be6cc02d6614a6f6193c74167a8ff23
ms.openlocfilehash: 14c85a46b8026878c3b5502931f937e2cf6196cd
ms.lasthandoff: 03/17/2017

---
# <a name="unorm3-class"></a>unorm_3 클래스
3 가지 서명 되지 않은 일반 숫자의 short 벡터를 나타냅니다.  
  
## <a name="syntax"></a>구문  
  
```  
class unorm_3;  
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-typedefs"></a>공용 Typedefs  
  
|이름|설명|  
|----------|-----------------|  
|`value_type`||  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[unorm_3 생성자](#ctor)|오버로드됨. 기본 생성자를 0부터 모든 요소를 초기화 합니다.|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|unorm_3::get_x||  
|unorm_3::get_xy||  
|unorm_3::get_xyz||  
|unorm_3::get_xz||  
|unorm_3::get_xzy||  
|unorm_3::get_y||  
|unorm_3::get_yx||  
|unorm_3::get_yxz||  
|unorm_3::get_yz||  
|unorm_3::get_yzx||  
|unorm_3::get_z||  
|unorm_3::get_zx||  
|unorm_3::get_zxy||  
|unorm_3::get_zy||  
|unorm_3::get_zyx||  
|Unorm_3::ref_b||  
|Unorm_3::ref_g||  
|Unorm_3::ref_r||  
|Unorm_3::ref_x||  
|Unorm_3::ref_y||  
|Unorm_3::ref_z||  
|unorm_3::set_x||  
|unorm_3::set_xy||  
|unorm_3::set_xyz||  
|unorm_3::set_xz||  
|unorm_3::set_xzy||  
|unorm_3::set_y||  
|unorm_3::set_yx||  
|unorm_3::set_yxz||  
|unorm_3::set_yz||  
|unorm_3::set_yzx||  
|unorm_3::set_z||  
|unorm_3::set_zx||  
|unorm_3::set_zxy||  
|unorm_3::set_zy||  
|unorm_3::set_zyx||  
  
### <a name="public-operators"></a>Public 연산자  
  
|이름|설명|  
|----------|-----------------|  
|unorm_3::operator-||  
|unorm_3::operator * =||  
|unorm_3::operator / =||  
|unorm_3::operator + +||  
|unorm_3::operator + =||  
|unorm_3::operator =||  
|-= unorm_3::operator||  
  
### <a name="public-constants"></a>공용 상수  
  
|이름|설명|  
|----------|-----------------|  
|[상수 크기](#unorm_3__size)||  
  
### <a name="public-data-members"></a>공용 데이터 멤버  
  
|이름|설명|  
|----------|-----------------|  
|unorm_3::b||  
|unorm_3::bg||  
|unorm_3::bgr||  
|unorm_3::br||  
|unorm_3::brg||  
|unorm_3::g||  
|unorm_3::gb||  
|unorm_3::gbr||  
|unorm_3::gr||  
|unorm_3::grb||  
|unorm_3::r||  
|unorm_3::rb||  
|unorm_3::rbg||  
|unorm_3::rg||  
|unorm_3::rgb||  
|unorm_3::x||  
|unorm_3::xy||  
|unorm_3::xyz||  
|unorm_3::xz||  
|unorm_3::xzy||  
|unorm_3::y||  
|unorm_3::yx||  
|unorm_3::yxz||  
|unorm_3::yz||  
|unorm_3::yzx||  
|unorm_3::z||  
|unorm_3::zx||  
|unorm_3::zxy||  
|unorm_3::zy||  
|unorm_3::zyx||  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 `unorm_3`  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** amp_short_vectors.h  
  
 **Namespace:** concurrency:: graphics  
  
##  <a name="ctor"></a>unorm_3 

 기본 생성자를 0부터 모든 요소를 초기화 합니다.  
  
```  
unorm_3() restrict(amp,
    cpu);

 
unorm_3(
    unorm _V0,  
    unorm _V1,  
    unorm _V2) restrict(amp,
    cpu);

 
unorm_3(
    float _V0,  
    float _V1,  
    float _V2) restrict(amp,
    cpu);

 
unorm_3(
    unorm _V) restrict(amp,
    cpu);

 
explicit unorm_3(
    float _V) restrict(amp,
    cpu);

 
unorm_3(
    const unorm_3& _Other) restrict(amp,
    cpu);

 
explicit inline unorm_3(
    const uint_3& _Other) restrict(amp,
    cpu);

 
explicit inline unorm_3(
    const int_3& _Other) restrict(amp,
    cpu);

 
explicit inline unorm_3(
    const float_3& _Other) restrict(amp,
    cpu);

 
explicit inline unorm_3(
    const norm_3& _Other) restrict(amp,
    cpu);

 
explicit inline unorm_3(
    const double_3& _Other) restrict(amp,
    cpu);
```  
  
### <a name="parameters"></a>매개 변수  
 `_V0`  
 0 요소를 초기화할 값입니다.  
  
 `_V1`  
 1 요소를 초기화할 값입니다.  
  
 `_V2`  
 2 요소를 초기화할 값입니다.  
  
 `_V`  
 초기화에 대 한 값입니다.  
  
 `_Other`  
 초기화 하는 데 사용 되는 개체입니다.  
  
##  <a name="unorm_3__size"></a>크기 

```  
static const int size = 3;  
```  
  
## <a name="see-also"></a>참고 항목  
 [Concurrency::graphics 네임스페이스](concurrency-graphics-namespace.md)
