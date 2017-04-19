---
title: "CAccelerateDecelerateTransition Class1 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CAccelerateDecelerateTransition
- afxanimationcontroller/CAccelerateDecelerateTransition
dev_langs:
- C++
helpviewer_keywords:
- CAccelerateDecelerateTransition class
ms.assetid: b1f31ee8-bb11-4ccc-b124-365fb02b025c
caps.latest.revision: 16
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
ms.sourcegitcommit: 5a0c6a1062330f952bb8fa52bc934f6754465513
ms.openlocfilehash: f11dc96b48695b998fb17c33735e8f56bce517b7
ms.lasthandoff: 02/24/2017

---
# <a name="cacceleratedeceleratetransition-class"></a>CAccelerateDecelerateTransition 클래스
가속-감속 전환을 구현합니다.  
  
## <a name="syntax"></a>구문  
  
```  
class CAccelerateDecelerateTransition : public CBaseTransition;  
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[CAccelerateDecelerateTransition::CAccelerateDecelerateTransition](#cacceleratedeceleratetransition)|전환 개체를 생성 합니다.|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[CAccelerateDecelerateTransition::Create](#create)|캡슐화 된 전환 COM 개체를 만드는 전환 라이브러리를 호출 합니다. (재정의 [CBaseTransition::Create](../../mfc/reference/cbasetransition-class.md#create).)|  
  
### <a name="public-data-members"></a>공용 데이터 멤버  
  
|이름|설명|  
|----------|-----------------|  
|[CAccelerateDecelerateTransition::m_accelerationRatio](#m_accelerationratio)|기간을 가속화 하는 데 걸린 시간의 비율입니다.|  
|[CAccelerateDecelerateTransition::m_decelerationRatio](#m_decelerationratio)|기간으로 감속 데 걸린 시간의 비율입니다.|  
|[CAccelerateDecelerateTransition::m_duration](#m_duration)|전환의 기간입니다.|  
|[CAccelerateDecelerateTransition::m_finalValue](#m_finalvalue)|전환의 끝에 있는 애니메이션 변수의 값입니다.|  
  
## <a name="remarks"></a>주의  
 동안 가속-감속 전환을, 애니메이션 변수 속도 지정된 된 값에는 전환 기간 동안 다음 속도가 느려집니다. 변수 가속화 하 고 다른 가속 및 감속을 지정 하 여 독립적으로 감속 얼마나 신속 하 게 제어할 수 있습니다. 초기 속도&0;이 되 면 가속 비율은 변수 문제를 신속 하 고, 작업에 소요 되는 기간을의 소수 부분 감속 비율와 마찬가지로입니다. 초기 속도&0;이 아닌 경우,&0; 및 전환의 끝에 도달 하는 속도 간격의 비율 및 됩니다. 가속 비율 및 감속 비율 1.0의 최대 합계를 계산 해야 합니다. 전환 되는 모든 자동으로 지워집니다 것이 좋습니다 하에 할당 된 새 연산자를 사용 하 여 합니다. 캡슐화 IUIAnimationTransition COM 개체는 NULL이 될 때까지 CAnimationController::AnimateGroup를 하 여 생성 됩니다. 이 COM 개체의 생성에 영향을 주지 않습니다 후 멤버 변수를 변경 합니다.  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CBaseTransition](../../mfc/reference/cbasetransition-class.md)  
  
 `CAccelerateDecelerateTransition`   
  
## <a name="requirements"></a>요구 사항  
 **헤더:** afxanimationcontroller.h  
  
##  <a name="a-namecacceleratedeceleratetransitiona--cacceleratedeceleratetransitioncacceleratedeceleratetransition"></a><a name="cacceleratedeceleratetransition"></a>CAccelerateDecelerateTransition::CAccelerateDecelerateTransition  
 전환 개체를 생성 합니다.  
  
```  
CAccelerateDecelerateTransition(
    UI_ANIMATION_SECONDS duration,  
    DOUBLE finalValue,  
    DOUBLE accelerationRatio = 0.3,  
    DOUBLE decelerationRatio = 0.3);
```  
  
### <a name="parameters"></a>매개 변수  
 `duration`  
 전환의 기간입니다.  
  
 `finalValue`  
 전환의 끝에 있는 애니메이션 변수의 값입니다.  
  
 `accelerationRatio`  
 기간을 가속화 하는 데 걸린 시간의 비율입니다.  
  
 `decelerationRatio`  
 기간으로 감속 데 걸린 시간의 비율입니다.  
  
##  <a name="a-namecreatea--cacceleratedeceleratetransitioncreate"></a><a name="create"></a>CAccelerateDecelerateTransition::Create  
 캡슐화 된 전환 COM 개체를 만드는 전환 라이브러리를 호출 합니다.  
  
```  
virtual BOOL Create(
    IUIAnimationTransitionLibrary* pLibrary,  
    IUIAnimationTransitionFactory* *\not used*\);
```  
  
### <a name="parameters"></a>매개 변수  
`pLibrary`  
 에 대 한 포인터는 [IUIAnimationTransitionLibrary 인터페이스](https://msdn.microsoft.com/library/windows/desktop/dd371897), 표준 전환의 라이브러리를 정의 하는 합니다.  
  
### <a name="return-value"></a>반환 값  
 TRUE 이면 전환을 만들었습니다. 그렇지 않으면 FALSE입니다.  
  
##  <a name="a-namemaccelerationratioa--cacceleratedeceleratetransitionmaccelerationratio"></a><a name="m_accelerationratio"></a>CAccelerateDecelerateTransition::m_accelerationRatio  
 기간을 가속화 하는 데 걸린 시간의 비율입니다.  
  
```  
DOUBLE m_accelerationRatio;  
```  
  
##  <a name="a-namemdecelerationratioa--cacceleratedeceleratetransitionmdecelerationratio"></a><a name="m_decelerationratio"></a>CAccelerateDecelerateTransition::m_decelerationRatio  
 기간으로 감속 데 걸린 시간의 비율입니다.  
  
```  
DOUBLE m_decelerationRatio;  
```  
  
##  <a name="a-namemdurationa--cacceleratedeceleratetransitionmduration"></a><a name="m_duration"></a>CAccelerateDecelerateTransition::m_duration  
 전환의 기간입니다.  
  
```  
UI_ANIMATION_SECONDS m_duration;  
```  
  
##  <a name="a-namemfinalvaluea--cacceleratedeceleratetransitionmfinalvalue"></a><a name="m_finalvalue"></a>CAccelerateDecelerateTransition::m_finalValue  
 전환의 끝에 있는 애니메이션 변수의 값입니다.  
  
```  
DOUBLE m_finalValue;  
```  
  
## <a name="see-also"></a>참고 항목  
 [클래스](../../mfc/reference/mfc-classes.md)
