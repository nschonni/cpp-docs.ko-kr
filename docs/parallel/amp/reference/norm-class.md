---
title: "norm 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- norm
- AMP_SHORT_VECTORS/norm
- AMP_SHORT_VECTORS/Concurrency::graphics::norm Constructor
dev_langs:
- C++
ms.assetid: 73002f3d-c25e-4119-bcd3-4c46c9b6abf1
caps.latest.revision: 8
author: mikeblome
ms.author: mblome
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
translationtype: Machine Translation
ms.sourcegitcommit: 5faef5bd1be6cc02d6614a6f6193c74167a8ff23
ms.openlocfilehash: 6f6477f37a94a0c2a093fd3a63fa8e87463a5a7b
ms.lasthandoff: 03/17/2017

---
# <a name="norm-class"></a>norm 클래스
Norm 수를 나타냅니다. 각 요소는 부동 소수점 숫자의 범위에 [-1.0 f, 1.0 f].  
  
## <a name="syntax"></a>구문  
  
```  
class norm;  
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[norm 생성자](#ctor)|오버로드됨. 기본 생성자입니다. 0.0f로 초기화합니다.|  
  
### <a name="public-operators"></a>Public 연산자  
  
|이름|설명|  
|----------|-----------------|  
|norm::operator-||  
|norm::operator-||  
|norm::operator float|변환 연산자입니다. Norm 번호 변환 부동 소수점 값입니다.|  
|norm::operator * =||  
|norm::operator / =||  
|norm::operator + +||  
|norm::operator + =||  
|norm::operator =||  
|-= norm::operator||  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 `norm`  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** amp_short_vectors.h  
  
 **Namespace:** concurrency:: graphics  
  
##  <a name="ctor"></a>norm 

 기본 생성자입니다. 0.0f로 초기화합니다.  
  
```  
norm(
    void) restrict(amp,
    cpu);

 
explicit norm(
    float _V) restrict(amp,
    cpu);

 
explicit norm(
    unsigned int _V) restrict(amp,
    cpu);

 
explicit norm(
    int _V) restrict(amp,
    cpu);

 
explicit norm(
    double _V) restrict(amp,
    cpu);

 
norm(
    const norm& _Other) restrict(amp,
    cpu);

 
norm(
    const unorm& _Other) restrict(amp,
    cpu);
```  
  
### <a name="parameters"></a>매개 변수  
 `_V`  
 초기화할 때 사용되는 값입니다.  
  
 `_Other`  
 초기화 하는 데 사용 되는 개체입니다.  
  
## <a name="see-also"></a>참고 항목  
 [Concurrency::graphics 네임스페이스](concurrency-graphics-namespace.md)
