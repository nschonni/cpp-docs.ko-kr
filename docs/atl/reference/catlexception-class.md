---
title: "CAtlException 클래스 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CAtlException
- ATLEXCEPT/ATL::CAtlException
- ATLEXCEPT/ATL::CAtlException::CAtlException
- ATLEXCEPT/ATL::CAtlException::m_hr
dev_langs:
- C++
helpviewer_keywords:
- CAtlException class
ms.assetid: 3fd7b041-f70d-4292-b947-0d70781d95a8
caps.latest.revision: 19
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
ms.sourcegitcommit: d2d39abf526a58b8442107b5ee816f316ae841f5
ms.openlocfilehash: 471ba42f25a4e237db03f2516288a7b33a0efd63
ms.lasthandoff: 03/31/2017

---
# <a name="catlexception-class"></a>CAtlException 클래스
이 클래스는 ATL 예외를 정의합니다.  
  
## <a name="syntax"></a>구문  
  
```
class CAtlException
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[CAtlException::CAtlException](#catlexception)|생성자입니다.|  
  
### <a name="public-operators"></a>Public 연산자  
  
|이름|설명|  
|----------|-----------------|  
|[CAtlException::operator HRESULT](#operator_hresult)|현재 개체를 HRESULT 값을 캐스팅합니다.|  
  
### <a name="public-data-members"></a>공용 데이터 멤버  
  
|이름|설명|  
|----------|-----------------|  
|[CAtlException::m_hr](#m_hr)|형식의 변수 HRESULT 개체에 의해 생성 및 오류 조건을 저장 하는 데 사용 합니다.|  
  
## <a name="remarks"></a>주의  
 A `CAtlException` 개체 ATL 작업과 관련 된 예외 상태를 나타냅니다. `CAtlException` 클래스는 예외 및 예외를 HRESULT 값이 있는 것 처럼 처리할 수 있도록 하는 캐스트 연산자에 대 한 이유를 나타내는 상태 코드를 저장 하는 공용 데이터 멤버를 포함 합니다.  
  
 일반적으로 호출 합니다 `AtlThrow` 만드는 대신 한 `CAtlException` 개체를 직접 합니다.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** atlexcept.h  
  
##  <a name="catlexception"></a>CAtlException::CAtlException  
 생성자입니다.  
  
```
CAtlException(HRESULT hr) throw();
CAtlException() throw();
```  
  
### <a name="parameters"></a>매개 변수  
 `hr`  
 `HRESULT` 오류 코드입니다.  
  
##  <a name="operator_hresult"></a>CAtlException::operator HRESULT 
 현재 개체를 HRESULT 값을 캐스팅합니다.  
  
```  
operator HRESULT() const throw ();
```  
  
##  <a name="m_hr"></a>CAtlException::m_hr  
 `HRESULT` 데이터 멤버입니다.  
  
```
HRESULT m_hr;
```  
  
### <a name="remarks"></a>주의  
 오류 조건이 저장 된 데이터 멤버입니다. HRESULT 값이 생성자에 의해 설정 [CAtlException::CAtlException](#catlexception)합니다.  
  
## <a name="see-also"></a>참고 항목  
 [Atlthrow 변형이](debugging-and-error-reporting-global-functions.md#atlthrow)   
 [클래스 개요](../../atl/atl-class-overview.md)
