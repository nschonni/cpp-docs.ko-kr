---
title: "int_3 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- amp_short_vectors/Concurrency::graphics::int_3::get_x
- amp_short_vectors/Concurrency::graphics::int_3::operator-=
- amp_short_vectors/Concurrency::graphics::int_3::get_y
- amp_short_vectors/Concurrency::graphics::int_3::operator=
- amp_short_vectors/Concurrency::graphics::int_3::operator++
- amp_short_vectors/Concurrency::graphics::int_3::zyx
- amp_short_vectors/Concurrency::graphics::int_3::get_z
- amp_short_vectors/Concurrency::graphics::int_3::operator*=
- amp_short_vectors/Concurrency::graphics::int_3::grb
- amp_short_vectors/Concurrency::graphics::int_3::get_xz
- amp_short_vectors/Concurrency::graphics::int_3::br
- amp_short_vectors/Concurrency::graphics::int_3::operator--
- amp_short_vectors/Concurrency::graphics::int_3
- amp_short_vectors/Concurrency::graphics::int_3::set_yx
- amp_short_vectors/Concurrency::graphics::int_3::x
- amp_short_vectors/Concurrency::graphics::int_3::yxz
- amp_short_vectors/Concurrency::graphics::int_3::set_y
- amp_short_vectors/Concurrency::graphics::int_3::zy
- amp_short_vectors/Concurrency::graphics::int_3::z
- amp_short_vectors/Concurrency::graphics::int_3::get_zx
- amp_short_vectors/Concurrency::graphics::int_3::rb
- amp_short_vectors/Concurrency::graphics::int_3::yzx
- amp_short_vectors/Concurrency::graphics::int_3::gb
- amp_short_vectors/Concurrency::graphics::int_3::set_zxy
- amp_short_vectors/Concurrency::graphics::int_3::xy
- amp_short_vectors/Concurrency::graphics::int_3::set_zx
- amp_short_vectors/Concurrency::graphics::int_3::g
- amp_short_vectors/Concurrency::graphics::int_3::operator/=
- amp_short_vectors/Concurrency::graphics::int_3::get_zy
- amp_short_vectors/Concurrency::graphics::int_3::yx
- amp_short_vectors/Concurrency::graphics::int_3::xzy
- amp_short_vectors/Concurrency::graphics::int_3::set_x
- amp_short_vectors/Concurrency::graphics::int_3::set_xz
- amp_short_vectors/Concurrency::graphics::int_3::get_yzx
- amp_short_vectors/Concurrency::graphics::int_3::b
- amp_short_vectors/Concurrency::graphics::int_3::gbr
- amp_short_vectors/Concurrency::graphics::int_3::operator+=
- amp_short_vectors/Concurrency::graphics::int_3::gr
- amp_short_vectors/Concurrency::graphics::int_3::brg
- amp_short_vectors/Concurrency::graphics::int_3::bg
- amp_short_vectors/Concurrency::graphics::int_3::zx
- amp_short_vectors/Concurrency::graphics::int_3::get_xyz
- amp_short_vectors/Concurrency::graphics::int_3::set_zyx
- amp_short_vectors/Concurrency::graphics::int_3::set_yzx
- amp_short_vectors/Concurrency::graphics::int_3::y
- amp_short_vectors/Concurrency::graphics::int_3::set_z
- amp_short_vectors/Concurrency::graphics::int_3::r
- amp_short_vectors/Concurrency::graphics::int_3::set_xzy
- amp_short_vectors/Concurrency::graphics::int_3::rg
- amp_short_vectors/Concurrency::graphics::int_3::xyz
- amp_short_vectors/Concurrency::graphics::int_3::get_yz
- amp_short_vectors/Concurrency::graphics::int_3::operator-
- amp_short_vectors/Concurrency::graphics::int_3::set_xy
- amp_short_vectors/Concurrency::graphics::int_3::zxy
- amp_short_vectors/Concurrency::graphics::int_3::yz
- amp_short_vectors/Concurrency::graphics::int_3::set_zy
- amp_short_vectors/Concurrency::graphics::int_3::bgr
- amp_short_vectors/Concurrency::graphics::int_3::get_xzy
- amp_short_vectors/Concurrency::graphics::int_3::get_yx
- amp_short_vectors/Concurrency::graphics::int_3::rbg
- amp_short_vectors/Concurrency::graphics::int_3::get_zxy
- amp_short_vectors/Concurrency::graphics::int_3::set_yxz
- amp_short_vectors/Concurrency::graphics::int_3::rgb
- amp_short_vectors/Concurrency::graphics::int_3::get_xy
- amp_short_vectors/Concurrency::graphics::int_3::set_xyz
- amp_short_vectors/Concurrency::graphics::int_3::get_yxz
- amp_short_vectors/Concurrency::graphics::int_3::get_zyx
- amp_short_vectors/Concurrency::graphics::int_3::xz
- amp_short_vectors/Concurrency::graphics::int_3::set_yz
dev_langs:
- C++
ms.assetid: d4af182f-30f1-455c-b16d-aa99cd314038
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
ms.openlocfilehash: d9a9b8eed7fcf46dee258c55471e79420666e043
ms.lasthandoff: 03/17/2017

---
# <a name="int3-class"></a>int_3 클래스
세 개의 정수 짧은 벡터를 나타냅니다.  
  
## <a name="syntax"></a>구문  
  
```  
class int_3;  
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-typedefs"></a>공용 Typedefs  
  
|이름|설명|  
|----------|-----------------|  
|`value_type`||  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[int_3 생성자](#ctor)|오버로드됨. 기본 생성자를 0부터 모든 요소를 초기화 합니다.|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|int_3::get_x||  
|int_3::get_xy||  
|int_3::get_xyz||  
|int_3::get_xz||  
|int_3::get_xzy||  
|int_3::get_y||  
|int_3::get_yx||  
|int_3::get_yxz||  
|int_3::get_yz||  
|int_3::get_yzx||  
|int_3::get_z||  
|int_3::get_zx||  
|int_3::get_zxy||  
|int_3::get_zy||  
|int_3::get_zyx||  
|int_3::ref_b||  
|int_3::ref_g||  
|int_3::ref_r||  
|int_3::ref_x||  
|int_3::ref_y||  
|int_3::ref_z||  
|int_3::set_x||  
|int_3::set_xy||  
|int_3::set_xyz||  
|int_3::set_xz||  
|int_3::set_xzy||  
|int_3::set_y||  
|int_3::set_yx||  
|int_3::set_yxz||  
|int_3::set_yz||  
|int_3::set_yzx||  
|int_3::set_z||  
|int_3::set_zx||  
|int_3::set_zxy||  
|int_3::set_zy||  
|int_3::set_zyx||  
  
### <a name="public-operators"></a>Public 연산자  
  
|이름|설명|  
|----------|-----------------|  
|int_3::operator-||  
|int_3::operator-||  
|int_3::operator % =||  
|int_3::operator = / /||  
|int_3::operator * =||  
|int_3::operator / =||  
|int_3::operator ^ =||  
|int_3::operator | =||  
|int_3::operator ~||  
|int_3::operator + +||  
|int_3::operator + =||  
|int_3::operator\<=||  
|int_3::operator =||  
|-= int_3::operator||  
|int_3::operator >> =||  
  
### <a name="public-constants"></a>공용 상수  
  
|이름|설명|  
|----------|-----------------|  
|[상수 크기](#size)||  
  
### <a name="public-data-members"></a>공용 데이터 멤버  
  
|이름|설명|  
|----------|-----------------|  
|int_3::b||  
|int_3::bg||  
|int_3::bgr||  
|int_3::br||  
|int_3::brg||  
|int_3::g||  
|int_3::gb||  
|int_3::gbr||  
|int_3::gr||  
|int_3::grb||  
|int_3::r||  
|int_3::rb||  
|int_3::rbg||  
|int_3::rg||  
|int_3::rgb||  
|int_3::x||  
|int_3::xy||  
|int_3::xyz||  
|int_3::xz||  
|int_3::xzy||  
|int_3::y||  
|int_3::yx||  
|int_3::yxz||  
|int_3::yz||  
|int_3::yzx||  
|int_3::z||  
|int_3::zx||  
|int_3::zxy||  
|int_3::zy||  
|int_3::zyx||  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 `int_3`  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** amp_short_vectors.h  
  
 **Namespace:** concurrency:: graphics  

## <a name="ctor"></a>int_3 

기본 생성자를 0부터 모든 요소를 초기화 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
int_3() restrict(amp,cpu);  
int_3(  
   int _V0,  
   int _V1,  
   int _V2  
) restrict(amp,cpu);  
int_3(  
   int _V  
) restrict(amp,cpu);  
int_3(  
   const int_3& _Other  
) restrict(amp,cpu);  
explicit inline int_3(  
   const uint_3& _Other  
) restrict(amp,cpu);  
explicit inline int_3(  
   const float_3& _Other  
) restrict(amp,cpu);  
explicit inline int_3(  
   const unorm_3& _Other  
) restrict(amp,cpu);  
explicit inline int_3(  
   const norm_3& _Other  
) restrict(amp,cpu);  
explicit inline int_3(  
   const double_3& _Other  
) restrict(amp,cpu);  
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
  
## <a name="size"></a>크기 

## <a name="syntax"></a>구문  
  
```  
static const int size = 3;  
```  
  
## <a name="see-also"></a>참고 항목  
 [Concurrency::graphics 네임스페이스](concurrency-graphics-namespace.md)
