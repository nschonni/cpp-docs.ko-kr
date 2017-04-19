---
title: "CCustomTransition 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CCustomTransition
- AFXANIMATIONCONTROLLER/CCustomTransition
- AFXANIMATIONCONTROLLER/CCustomTransition::CCustomTransition
- AFXANIMATIONCONTROLLER/CCustomTransition::Create
- AFXANIMATIONCONTROLLER/CCustomTransition::SetInitialValue
- AFXANIMATIONCONTROLLER/CCustomTransition::SetInitialVelocity
- AFXANIMATIONCONTROLLER/CCustomTransition::m_bInitialValueSpecified
- AFXANIMATIONCONTROLLER/CCustomTransition::m_bInitialVelocitySpecified
- AFXANIMATIONCONTROLLER/CCustomTransition::m_initialValue
- AFXANIMATIONCONTROLLER/CCustomTransition::m_initialVelocity
- AFXANIMATIONCONTROLLER/CCustomTransition::m_pInterpolator
dev_langs:
- C++
helpviewer_keywords:
- CCustomTransition class
ms.assetid: 5bd3f492-940f-4290-a38b-fa68eb8f8401
caps.latest.revision: 17
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
ms.sourcegitcommit: 73410ae17465880f455e5b15026f6cc010803c19
ms.openlocfilehash: 483fb2ab84d2c41fe4666a4ea333c0be8b07caee
ms.lasthandoff: 02/24/2017

---
# <a name="ccustomtransition-class"></a>CCustomTransition 클래스
사용자 지정 전환을 구현합니다.  
  
## <a name="syntax"></a>구문  
  
```  
class CCustomTransition : public CBaseTransition;  
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[CCustomTransition::CCustomTransition](#ccustomtransition)|사용자 지정 전환을 개체를 만듭니다.|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[CCustomTransition::Create](#create)|캡슐화 된 전환 COM 개체를 만드는 전환 라이브러리를 호출 합니다. (재정의 [CBaseTransition::Create](../../mfc/reference/cbasetransition-class.md#create).)|  
|[CCustomTransition::SetInitialValue](#setinitialvalue)|이 전환과 관련 된 애니메이션 변수에 적용 될 초기 값을 설정 합니다.|  
|[CCustomTransition::SetInitialVelocity](#setinitialvelocity)|이 전환과 관련 된 애니메이션 변수에 적용 될 초기 속도 설정 합니다.|  
  
### <a name="protected-data-members"></a>보호된 데이터 멤버  
  
|이름|설명|  
|----------|-----------------|  
|[CCustomTransition::m_bInitialValueSpecified](#m_binitialvaluespecified)|SetInitialValue와 초기 값을 지정 했는지 여부를 지정 합니다.|  
|[CCustomTransition::m_bInitialVelocitySpecified](#m_binitialvelocityspecified)|초기 속도 SetInitialVelocity로 지정 되었는지 여부를 지정 합니다.|  
|[CCustomTransition::m_initialValue](#m_initialvalue)|초기 값을 저장합니다.|  
|[CCustomTransition::m_initialVelocity](#m_initialvelocity)|초기 속도 저장합니다.|  
|[CCustomTransition::m_pInterpolator](#m_pinterpolator)|사용자 지정 보간 기에 대 한 포인터를 저장합니다.|  
  
## <a name="remarks"></a>주의  
 CCustomTransitions 클래스 사용자 지정 전환을 구현 하는 개발자를 수 있습니다. 만들고 표준 전환으로 사용 하지만 해당 생성자는 사용자 지정 보간 기에 대 한 포인터를 매개 변수로 허용 합니다. 사용자 지정 전환을 사용 하 여 다음 단계를 수행 합니다. 1. CCustomInterpolator에서 클래스를 파생 하 고 최소한 구현 InterpolateValue 메서드. 2. 사용자 지정 보간 기 개체의 수명이 되도록 애니메이션의 기간 보다 오래 사용 되는 위치를 확인 합니다. 3. (New 연산자 사용) CCustomTransition 개체를 인스턴스화하고 생성자에서 사용자 지정 보간 기에 대 한 포인터를 전달 합니다. 4. 이러한 매개 변수는 사용자 지정 보간에 필요한 경우 CCustomTransition::SetInitialValue 및 CCustomTransition::SetInitialVelocity를 호출 합니다. 5. 사용자 지정 알고리즘으로 애니메이션 값을 갖는 애니메이션 개체의 사용자 지정 AddTransition 메서드 전환에 포인터를 전달 합니다. 6. 애니메이션 개체의 값을 변경 해야 하는 경우 Windows 애니메이션 API에서 CCustomInterpolator InterpolateValue (및 기타 관련 메서드) 호출 합니다.  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CBaseTransition](../../mfc/reference/cbasetransition-class.md)  
  
 `CCustomTransition`  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** afxanimationcontroller.h  
  
##  <a name="ccustomtransition"></a>CCustomTransition::CCustomTransition  
 사용자 지정 전환을 개체를 만듭니다.  
  
```  
CCustomTransition(CCustomInterpolator* pInterpolator);
```  
  
### <a name="parameters"></a>매개 변수  
 `pInterpolator`  
 사용자 지정 보간 기에 대 한 포인터입니다.  
  
##  <a name="create"></a>CCustomTransition::Create  
 캡슐화 된 전환 COM 개체를 만드는 전환 라이브러리를 호출 합니다.  
  
```  
virtual BOOL Create(
    IUIAnimationTransitionLibrary* */,  
    IUIAnimationTransitionFactory* pFactory);
```  
  
### <a name="parameters"></a>매개 변수  
 `pFactory`  
 사용자 지정 전환 만드는 담당 하는 전환 팩토리에 대 한 포인터입니다.  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
 또한이 메서드 초기 값과 관련 된이 전환 애니메이션 변수에 적용할 초기 속도 설정할 수 있습니다. 이 목적을 위해 프레임 워크 (CAnimationController::AnimateGroup를 호출할 때 발생) 캡슐화 된 전환 COM 개체를 만들기 전에 SetInitialValue 및 SetInitialVelocity를 호출 해야 합니다.  
  
##  <a name="m_binitialvaluespecified"></a>CCustomTransition::m_bInitialValueSpecified  
 SetInitialValue와 초기 값을 지정 했는지 여부를 지정 합니다.  
  
```  
BOOL m_bInitialValueSpecified;  
```  
  
##  <a name="m_binitialvelocityspecified"></a>CCustomTransition::m_bInitialVelocitySpecified  
 초기 속도 SetInitialVelocity로 지정 되었는지 여부를 지정 합니다.  
  
```  
BOOL m_bInitialVelocitySpecified;  
```  
  
##  <a name="m_initialvalue"></a>CCustomTransition::m_initialValue  
 초기 값을 저장합니다.  
  
```  
DOUBLE m_initialValue;  
```  
  
##  <a name="m_initialvelocity"></a>CCustomTransition::m_initialVelocity  
 초기 속도 저장합니다.  
  
```  
DOUBLE m_initialVelocity;  
```  
  
##  <a name="m_pinterpolator"></a>CCustomTransition::m_pInterpolator  
 사용자 지정 보간 기에 대 한 포인터를 저장합니다.  
  
```  
CCustomInterpolator* m_pInterpolator;  
```  
  
##  <a name="setinitialvalue"></a>CCustomTransition::SetInitialValue  
 이 전환과 관련 된 애니메이션 변수에 적용 될 초기 값을 설정 합니다.  
  
```  
void SetInitialValue(DOUBLE initialValue);
```  
  
### <a name="parameters"></a>매개 변수  
 `initialValue`  
  
##  <a name="setinitialvelocity"></a>CCustomTransition::SetInitialVelocity  
 이 전환과 관련 된 애니메이션 변수에 적용 될 초기 속도 설정 합니다.  
  
```  
void SetInitialVelocity(DOUBLE initialVelocity);
```  
  
### <a name="parameters"></a>매개 변수  
 `initialVelocity`  
  
## <a name="see-also"></a>참고 항목  
 [클래스](../../mfc/reference/mfc-classes.md)
