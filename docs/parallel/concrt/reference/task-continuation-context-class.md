---
title: "task_continuation_context 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- task_continuation_context
- PPLTASKS/concurrency::task_continuation_context
- PPLTASKS/concurrency::task_continuation_context::get_current_winrt_context
- PPLTASKS/concurrency::task_continuation_context::use_arbitrary
- PPLTASKS/concurrency::task_continuation_context::use_current
- PPLTASKS/concurrency::task_continuation_context::use_default
- PPLTASKS/concurrency::task_continuation_context::use_synchronous_execution
dev_langs:
- C++
helpviewer_keywords:
- task_continuation_context class
ms.assetid: 1fb5a76a-3682-45c2-a615-8b6b527741f0
caps.latest.revision: 15
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
ms.openlocfilehash: 8afd599e5ee489500d7f8c498d03c91ace6b99ed
ms.lasthandoff: 03/17/2017

---
# <a name="taskcontinuationcontext-class"></a>task_continuation_context 클래스
`task_continuation_context` 클래스를 사용하면 연속 실행 위치를 지정할 수 있습니다. 이 클래스는 Windows 스토어 앱에서 사용할 때만 유용합니다. 그 외의 앱에서는 작업 연속 실행 컨텍스트가 런타임에 의해 결정되며 구성할 수 없습니다.  
  
## <a name="syntax"></a>구문  
  
```
class task_continuation_context : public details::_ContextCallback;
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[get_current_winrt_context](#get_current_winrt_context)|현재 winrt 스레드 컨텍스트를 나타내는 작업 연속 컨텍스트 개체를 반환 합니다.|  
|[use_arbitrary](#use_arbitrary)|런타임이 연속에 대한 실행 컨텍스트를 선택할 수 있는 작업 연속 컨텍스트를 만듭니다.|  
|[use_current](#use_current)|현재 실행 컨텍스트를 나타내는 작업 연속 컨텍스트 개체를 반환합니다.|  
|[use_default](#use_default)|기본 작업 연속 컨텍스트를 만듭니다.|  
|[use_synchronous_execution](#use_synchronous_execution)|동기 실행 컨텍스트를 나타내는 작업 연속 컨텍스트 개체를 반환 합니다.|  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 `_ContextCallback`  
  
 `task_continuation_context`  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** ppltasks.h  
  
 **네임스페이스:** 동시성  

## <a name="get_current_winrt_context"></a>get_current_winrt_context
 현재 WinRT 스레드 컨텍스트를 나타내는 작업 연속 컨텍스트 개체를 반환 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
static task_continuation_context get_current_winrt_context();  
```  
  
## <a name="return-value"></a>반환 값  
 현재 Windows 런타임 스레드 컨텍스트입니다. 비-Windows Runtime 컨텍스트에서 호출 하는 경우에 빈 task_continuation_context를 반환 합니다.  
  
## <a name="remarks"></a>설명  
 `get_current_winrt_context` 메서드는 호출자의 Windows 런타임 스레드 컨텍스트를 캡처합니다. 비-Windows Runtime 호출자에 게는 빈 컨텍스트를 반환합니다.  
  
 반환한 값 `get_current_winrt_context` 선행 작업 아파트 인식 인지에 관계 없이 캡처된 컨텍스트 (STA vs MTA)의 아파트 모델에서 연속 작업을 실행 해야 런타임에 나타내는 데 사용할 수 있습니다. 작업이 Windows 런타임의 래핑을 해제 하는 작업이 인식 아파트 `IAsyncInfo` 인터페이스 또는 그러한 작업의 하위 작업입니다.  
  
 이 메서드는는 `use_current` 메서드를 만들었지만 역시 사용할 수 있는 네이티브 c + + 코드 없이 C + + /cli CX 확장 지원 합니다. 위함입니다 사용 하 여 고급 사용자가 쓰기 C + + 네이티브와 Windows 런타임 호출자에 대 한 알 수 없는 CX 라이브러리 코드입니다. 이 기능이 필요 하지 않은 한 것이 좋습니다는 `use_current` 메서드를만 사용할 수 있는 C + + CX 클라이언트입니다.  
  
  
##  <a name="use_arbitrary"></a>use_arbitrary 

 런타임이 연속에 대한 실행 컨텍스트를 선택할 수 있는 작업 연속 컨텍스트를 만듭니다.  
  
```
static task_continuation_context use_arbitrary();
```  
  
### <a name="return-value"></a>반환 값  
 임의의 위치를 나타내는 작업 연속 컨텍스트.  
  
### <a name="remarks"></a>주의  
 이 연속 컨텍스트를 사용 하는 경우 연속 작업이 선행 작업은 아파트를 인식 하는 경우에 런타임에 선택 된 컨텍스트에서 실행 됩니다.  
  
 `use_arbitrary`sta로 바뀝니다.에 만든 아파트 인식 작업에는 연속 작업에 대 한 기본 동작을 해제 하는 데 될 수 있습니다.  
  
 이 메서드는 Windows 스토어 응용 프로그램에 사용할 수만 있습니다.  
  
##  <a name="use_current"></a>use_current 

 현재 실행 컨텍스트를 나타내는 작업 연속 컨텍스트 개체를 반환합니다.  
  
```
static task_continuation_context use_current();
```  
  
### <a name="return-value"></a>반환 값  
 현재 실행 컨텍스트입니다.  
  
### <a name="remarks"></a>주의  
 이 메서드는 연속 오른쪽 아파트에서 실행 될 수 있도록 호출자의 Windows 런타임 컨텍스트를 캡처합니다.  
  
 반환한 값 `use_current` 캡처된 컨텍스트에서 STA vs (MTA)는 선행 작업의 아파트를 인식 되는지 여부에 관계 없이 연속이 실행 되어야 런타임에 나타내는 데 사용할 수 있습니다. 작업이 Windows 런타임의 래핑을 해제 하는 작업이 인식 아파트 `IAsyncInfo` 인터페이스 또는 그러한 작업의 하위 작업입니다.  
  
 이 메서드는 Windows 스토어 응용 프로그램에 사용할 수만 있습니다.  
  
##  <a name="use_default"></a>use_default 

 기본 작업 연속 컨텍스트를 만듭니다.  
  
```
static task_continuation_context use_default();
```  
  
### <a name="return-value"></a>반환 값  
 기본 연속 컨텍스트입니다.  
  
### <a name="remarks"></a>주의  
 기본 컨텍스트가 지정 하지 않으면 연속 컨텍스트를 호출할 때 사용 되는 `then` 메서드. Windows 응용 프로그램에 대 한 Windows 7과 아래와 같은 데스크톱 응용 프로그램에서 Windows 8 이상, 런타임에 작업 연속을 실행할 위치 결정 합니다. 그러나 Windows 스토어 앱의 경우 아파트 인식 작업에는 연속 작업에 대 한 기본 연속 컨텍스트는 아파트 여기서 `then` 호출 됩니다.  
  
 작업이 Windows 런타임의 래핑을 해제 하는 작업이 인식 아파트 `IAsyncInfo` 인터페이스 또는 그러한 작업의 하위 작업입니다. 따라서 Windows 런타임 STA에서 아파트 인식 작업에서 연속 작업을 예약 하는 경우 연속 작업에서에서 실행될지 해당 sta로 바뀝니다.  
  
 비 아파트 인식 작업에는 연속 작업은 런타임이 선택할 컨텍스트에서 실행 됩니다.  

## <a name="use_synchronous_execution"></a>task_continuation_context::use_synchronous_execution  
동기 실행 컨텍스트를 나타내는 작업 연속 컨텍스트 개체를 반환 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
static task_continuation_context use_synchronous_execution();  
```  
  
## <a name="return-value"></a>반환 값  
 동기 실행 컨텍스트입니다.  
  
## <a name="remarks"></a>설명  
 `use_synchronous_execution` 메서드를 사용 하면 연속 작업이 선행 작업의 완료를 일으키는 컨텍스트에서만 동기적으로 실행 하도록 합니다.  
  
 선행 작업이 이미 완료 되어 연속 작업은 연결 된 경우 연속 작업이 연속 작업을 연결 하는 컨텍스트에 동기적으로 실행 됩니다.  
  
 
## <a name="see-also"></a>참고 항목  
 [concurrency 네임스페이스](concurrency-namespace.md)
