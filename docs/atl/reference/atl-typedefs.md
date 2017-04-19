---
title: "ATL Typedef | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: 'index-page '
dev_langs:
- C++
helpviewer_keywords:
- typedefs, ATL
- typedefs
- ATL, typedefs
ms.assetid: 7dd05baa-3efb-4e3b-af23-793c610f4560
caps.latest.revision: 20
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
ms.sourcegitcommit: 347e7bf7cd9173fb2815f44fc052ec23ab4055a6
ms.openlocfilehash: aa57212b602538e4e8d2854c6075562e72472796
ms.lasthandoff: 02/24/2017

---
# <a name="atl-typedefs"></a>ATL 형식 정의
액티브 템플릿 라이브러리는 다음 형식 정의 포함합니다.  
  
|||  
|-|-|  
|[_ATL_BASE_MODULE](#_atl_base_module)|형식 정의 기반으로 정의 된 [_ATL_BASE_MODULE70](../../atl/reference/atl-base-module70-structure.md)합니다.|  
|[_ATL_COM_MODULE](#_atl_com_module)|형식 정의 기반으로 정의 된 [_ATL_COM_MODULE70](../../atl/reference/atl-com-module70-structure.md)합니다.|  
|[_ATL_MODULE](#_atl_module)|형식 정의 기반으로 정의 된 [_ATL_MODULE70](../../atl/reference/atl-module70-structure.md)합니다.|  
|[_ATL_WIN_MODULE](#_atl_win_module)|형식 정의 기반으로 정의 된 [_ATL_WIN_MODULE70](../../atl/reference/atl-win-module70-structure.md)|  
|[ATL_URL_PORT](#atl_url_port)|사용 되는 형식을 [CUrl](../../atl/reference/curl-class.md) 포트 번호를 지정 하는 데 있습니다.|  
|[CComDispatchDriver](#ccomdispatchdriver)|이 클래스는 COM 인터페이스 포인터를 관리합니다.|  
|[CComGlobalsThreadModel](#ccomglobalsthreadmodel)|적절 한 스레드 사용 되는 스레딩 모델에 관계 없이 모델 메서드를 호출 합니다.|  
|[CComObjectThreadModel](#ccomobjectthreadmodel)|적절 한 스레드 사용 되는 스레딩 모델에 관계 없이 모델 메서드를 호출 합니다.|  
|[CContainedWindow](#ccontainedwindow)|이 클래스의 특수화는 **CContainedWindowT 합니다.**|  
|[CPath](#cpath)|특수화 [CPathT](../../atl/reference/cpatht-class.md) 를 사용 하 여 `CString`합니다.|  
|[CPathA](#cpatha)|특수화 [CPathT](../../atl/reference/cpatht-class.md) 를 사용 하 여 `CStringA`합니다.|  
|[CPathW](#cpathw)|특수화 [CPathT](../../atl/reference/cpatht-class.md) 를 사용 하 여 `CStringW`합니다.|  
|[CSimpleValArray](#csimplevalarray)|단순 형식을 저장 하기 위해 배열을 나타냅니다.|  
|[DefaultThreadTraits](#defaultthreadtraits)|기본 스레드 특성 클래스입니다.|  
|[LPCURL](#lpcurl)|상수에 대 한 포인터 [CUrl](../../atl/reference/curl-class.md) 개체입니다.|  
|[LPURL](#lpurl)|에 대 한 포인터는 [CUrl](../../atl/reference/curl-class.md) 개체입니다.|  
  
##  <a name="a-nameatlbasemodulea--atlbasemodule"></a><a name="_atl_base_module"></a>_ATL_BASE_MODULE  
 Typedef _ATL_BASE_MODULE70을 기반으로 정의 됩니다.  
  
```   
typedef ATL::_ATL_BASE_MODULE70 _ATL_BASE_MODULE;   
```  
  
### <a name="remarks"></a>주의  
 모든 ATL 프로젝트에서 사용 합니다. 에 따라 [_ATL_BASE_MODULE70](../../atl/reference/atl-base-module70-structure.md)합니다.  
  
 ATL 7.0 모듈 클래스의 일부인 클래스 _ATL_BASE_MODULE 구조에서 파생 됩니다.  ATL 모듈 클래스에 대 한 자세한 내용은 참조 [COM 모듈 클래스](../../atl/com-modules-classes.md)합니다.  
  
##  <a name="a-nameatlcommodulea--atlcommodule"></a><a name="_atl_com_module"></a>_ATL_COM_MODULE  
 Typedef _ATL_COM_MODULE70을 기반으로 정의 됩니다.  
  
```   
typedef ATL::_ATL_COM_MODULE70 _ATL_COM_MODULE;   
```  
  
### <a name="remarks"></a>주의  
 ATL 프로젝트 COM 기능을 사용 하 여 사용 합니다. 에 따라 [_ATL_COM_MODULE70](../../atl/reference/atl-com-module70-structure.md)합니다.  
  
##  <a name="a-nameatlmodulea--atlmodule"></a><a name="_atl_module"></a>_ATL_MODULE  
 Typedef _ATL_MODULE70을 기반으로 정의 됩니다.  
  
```   
typedef ATL::_ATL_MODULE70 _ATL_MODULE;   
```  
  
### <a name="remarks"></a>주의  
 에 따라 [_ATL_MODULE70](../../atl/reference/atl-module70-structure.md)합니다.  
  
##  <a name="a-nameatlwinmodulea--atlwinmodule"></a><a name="_atl_win_module"></a>_ATL_WIN_MODULE  
 Typedef _ATL_WIN_MODULE70을 기반으로 정의 됩니다.  
  
```   
typedef ATL::_ATL_WIN_MODULE70 _ATL_WIN_MODULE; 
 
```  
  
### <a name="remarks"></a>주의  
 기간 이동 기능을 사용 하는 모든 ATL 프로젝트에서 사용 합니다. 에 따라 [_ATL_WIN_MODULE70](../../atl/reference/atl-win-module70-structure.md)합니다.  
  
##  <a name="a-nameatlurlporta--atlurlport"></a><a name="atl_url_port"></a>ATL_URL_PORT 
  사용 되는 형식을 [CUrl](curl-class.md) 포트 번호를 지정 하는 데 있습니다.
```  
typedef WORD ATL_URL_PORT;
```  

##  <a name="a-nameccomdispatchdrivera--ccomdispatchdriver"></a><a name="ccomdispatchdriver"></a>CComDispatchDriver  
 이 클래스는 COM 인터페이스 포인터를 관리합니다.  
  
```   
typedef CComQIPtr<IDispatch, &__uuidof(IDispatch)> CComDispatchDriver;   
```  
  
##  <a name="a-nameccomglobalsthreadmodela--ccomglobalsthreadmodel"></a><a name="ccomglobalsthreadmodel"></a>CComGlobalsThreadModel  
 적절 한 스레드 사용 되는 스레딩 모델에 관계 없이 모델 메서드를 호출 합니다.  
  
```   
#if defined(_ATL_SINGLE_THREADED)  
typedef CComSingleThreadModel CComGlobalsThreadModel;  
#elif defined(_ATL_APARTMENT_THREADED)  
typedef CComMultiThreadModel CComGlobalsThreadModel;  
#elif defined(_ATL_FREE_THREADED)  
typedef CComMultiThreadModel CComGlobalsThreadModel;  
#else  
#pragma message ("No global threading model defined")  
#endif   
```  
  
### <a name="remarks"></a>주의  
 응용 프로그램에서 사용 되는 스레딩 모델에 따라는 `typedef` 이름 `CComGlobalsThreadModel` 참조 하거나 [CComSingleThreadModel](../../atl/reference/ccomsinglethreadmodel-class.md) 또는 [CComMultiThreadModel](../../atl/reference/ccommultithreadmodel-class.md)합니다. 이러한 클래스는 추가 제공 `typedef` 임계 클래스를 참조 하는 이름입니다.  
  
> [!NOTE]
> `CComGlobalsThreadModel`클래스를 참조 하지 않는 [CComMultiThreadModelNoCS](../../atl/reference/ccommultithreadmodelnocs-class.md)합니다.  
  
 사용 하 여 `CComGlobalsThreadModel` 문화권에서 특정 스레딩 모델 클래스를 지정 합니다. 사용 되는 스레딩 모델에 관계 없이 적절 한 메서드 호출 됩니다.  
  
 외에 `CComGlobalsThreadModel`, ATL은 제공 된 `typedef` 이름 [CComObjectThreadModel](#ccomobjectthreadmodel)합니다. 각각 사용 하 여 참조 하는 클래스 `typedef` 는 다음 표에 나와 있는 것 처럼 사용 하 고 스레딩 모델에 따라 달라 집니다.  
  
|형식 정의|단일 스레딩|아파트 스레딩|자유 스레딩|  
|-------------|----------------------|-------------------------|--------------------|  
|`CComObjectThreadModel`|S|S|M|  
|`CComGlobalsThreadModel`|S|M|M|  
  
 S= `CComSingleThreadModel`; M =`CComMultiThreadModel`  
  
 사용 하 여 `CComObjectThreadModel` 단일 개체 클래스 내에서. 사용 하 여 `CComGlobalsThreadModel` 프로그램에 전역적으로 사용할 수 없거나 여러 스레드에서 모듈 리소스를 보호 하려는 경우 개체에 있습니다.  
  
##  <a name="a-nameccomobjectthreadmodela--ccomobjectthreadmodel"></a><a name="ccomobjectthreadmodel"></a>CComObjectThreadModel  
 적절 한 스레드 사용 되는 스레딩 모델에 관계 없이 모델 메서드를 호출 합니다.  
  
```   
#if defined(_ATL_SINGLE_THREADED)  
typedef CComSingleThreadModel CComObjectThreadModel;  
#elif defined(_ATL_APARTMENT_THREADED)  
typedef CComSingleThreadModel CComObjectThreadModel;  
#elif defined(_ATL_FREE_THREADED)  
typedef CComMultiThreadModel CComObjectThreadModel;  
#else  
#pragma message ("No global threading model defined")  
#endif   
```  
  
### <a name="remarks"></a>주의  
 응용 프로그램에서 사용 되는 스레딩 모델에 따라는 `typedef` 이름 `CComObjectThreadModel` 참조 하거나 [CComSingleThreadModel](../../atl/reference/ccomsinglethreadmodel-class.md) 또는 [CComMultiThreadModel](../../atl/reference/ccommultithreadmodel-class.md)합니다. 이러한 클래스는 추가 제공 `typedef` 임계 클래스를 참조 하는 이름입니다.  
  
> [!NOTE]
> `CComObjectThreadModel`클래스를 참조 하지 않는 [CComMultiThreadModelNoCS](../../atl/reference/ccommultithreadmodelnocs-class.md)합니다.  
  
 사용 하 여 `CComObjectThreadModel` 문화권에서 특정 스레딩 모델 클래스를 지정 합니다. 사용 되는 스레딩 모델에 관계 없이 적절 한 메서드 호출 됩니다.  
  
 외에 `CComObjectThreadModel`, ATL은 제공 된 `typedef` 이름 [CComGlobalsThreadModel](#ccomglobalsthreadmodel)합니다. 각각 사용 하 여 참조 하는 클래스 `typedef` 는 다음 표에 나와 있는 것 처럼 사용 하 고 스레딩 모델에 따라 달라 집니다.  
  
|형식 정의|단일 스레딩|아파트 스레딩|자유 스레딩|  
|-------------|----------------------|-------------------------|--------------------|  
|`CComObjectThreadModel`|S|S|M|  
|`CComGlobalsThreadModel`|S|M|M|  
  
 S= `CComSingleThreadModel`; M =`CComMultiThreadModel`  
  
 사용 하 여 `CComObjectThreadModel` 단일 개체 클래스 내에서. 사용 하 여 `CComGlobalsThreadModel` 중 하나는 개체의 여러 스레드에서 모듈 리소스를 보호 하려는 경우 또는 프로그램에 전역적으로 사용할 수 있습니다.  
  
##  <a name="a-nameccontainedwindowa--ccontainedwindow"></a><a name="ccontainedwindow"></a>CContainedWindow  
 이 클래스의 특수화는 **CContainedWindowT 합니다.**  
  
```   
typedef CContainedWindowT<CWindow> CContainedWindow;   
```  
  
### <a name="remarks"></a>주의  
 `CContainedWindow`특수화 [CContainedWindowT](../../atl/reference/ccontainedwindowt-class.md)합니다. 기본 클래스 또는 특성을 변경 하려는 경우 사용 하 여 `CContainedWindowT` 직접.  
  
##  <a name="a-namecpatha--cpath"></a><a name="cpath"></a>CPath  
 특수화 [CPathT](../../atl/reference/cpatht-class.md) 를 사용 하 여 `CString`합니다.  
  
```   
typedef CPathT<CString> CPath;   
```  
  
##  <a name="a-namecpathaa--cpatha"></a><a name="cpatha"></a>CPathA  
 특수화 [CPathT](../../atl/reference/cpatht-class.md) 를 사용 하 여 `CStringA`합니다.  
  
```   
typedef CPathT<CStringA> CPathA;   
```  
  
##  <a name="a-namecpathwa--cpathw"></a><a name="cpathw"></a>CPathW  
 특수화 [CPathT](../../atl/reference/cpatht-class.md) 를 사용 하 여 `CStringW`합니다.  
  
```   
typedef ATL::CPathT<CStringW> CPathW;   
```  
  
##  <a name="a-namecsimplevalarraya--csimplevalarray"></a><a name="csimplevalarray"></a>CSimpleValArray  
 단순 형식을 저장 하기 위해 배열을 나타냅니다.  
  
```   
#define CSimpleValArray CSimpleArray   
```  
  
### <a name="remarks"></a>주의  
 `CSimpleValArray`만들기 및 관리 단순 데이터 형식이 포함 된 배열에 제공 됩니다. 단순 #define의 [CSimpleArray](../../atl/reference/csimplearray-class.md)합니다.  
  
##  <a name="a-namelpcurla--lpcurl"></a><a name="lpcurl"></a>LPCURL  
 상수에 대 한 포인터 [CUrl](../../atl/reference/curl-class.md) 개체입니다.  
  
```   
typedef const CUrl* LPCURL;   
```  

##  <a name="a-namedefaultthreadtraitsa--defaultthreadtraits"></a><a name="defaultthreadtraits"></a>DefaultThreadTraits
기본 스레드 특성 클래스입니다.

### <a name="syntax"></a>구문
```  
      #if defined(_MT)  
   typedef CRTThreadTraits DefaultThreadTraits;  
#else  
   typedef Win32ThreadTraits DefaultThreadTraits;  
#endif  
```

## <a name="remarks"></a>주의
현재 프로젝트에서 다중 스레드 CRT를 사용 하는 경우 DefaultThreadTraits CRTThreadTraits로 정의 됩니다. 그렇지 않으면 Win32ThreadTraits 사용 됩니다.
  
##  <a name="a-namelpurla--lpurl"></a><a name="lpurl"></a>LPURL  
 에 대 한 포인터는 [CUrl](../../atl/reference/curl-class.md) 개체입니다.  
  
```   
typedef CUrl* LPURL;   
```  
  
## <a name="see-also"></a>참고 항목  
 [ATL COM 데스크톱 구성 요소](../../atl/atl-com-desktop-components.md)   
 [함수](../../atl/reference/atl-functions.md)   
 [전역 변수](../../atl/reference/atl-global-variables.md)   
 [구조](../../atl/reference/atl-structures.md)   
 [매크로](../../atl/reference/atl-macros.md)   
 [클래스](../../atl/reference/atl-classes.md)