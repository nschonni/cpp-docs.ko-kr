---
title: "동시성 네임 스페이스 열거형 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CONCRT/concurrency::Agents_EventType
- CONCRT/concurrency::Concrt_TraceFlags
- CONCRT/concurrency::CriticalRegionType
- CONCRT/concurrency::PolicyElementKey
- CONCRT/concurrency::SchedulerType
- CONCRT/concurrency::SwitchingProxyState
- CONCRT/concurrency::WinRTInitializationType
- CONCRT/concurrency::join_type
- CONCRT/concurrency::message_status Enumeration
dev_langs:
- C++
ms.assetid: a40e3b2d-ad21-4229-9880-2cfa84f7ab8f
caps.latest.revision: 7
author: mikeblome
ms.author: mblome
manager: ghogen
translationtype: Machine Translation
ms.sourcegitcommit: 5faef5bd1be6cc02d6614a6f6193c74167a8ff23
ms.openlocfilehash: 7589f0054e9393f938bf69d4e1751202cbc02456
ms.lasthandoff: 03/17/2017

---
# <a name="concurrency-namespace-enums"></a>동시성 네임 스페이스 열거형
||||  
|-|-|-|  
|[Agents_EventType](#agents_eventtype)|[ConcRT_EventType](#concrt_eventtype)|[Concrt_TraceFlags](#concrt_traceflags)|  
|[CriticalRegionType](#criticalregiontype)|[DynamicProgressFeedbackType](#dynamicprogressfeedbacktype)|[PolicyElementKey](#policyelementkey)|  
|[SchedulerType](#schedulertype)|[SchedulingProtocolType](#schedulingprotocoltype)|[SwitchingProxyState](#switchingproxystate)|  
|[WinRTInitializationType](#winrtinitializationtype)|[agent_status](#agent_status)|[조인 유형](#join_type)|  
|[message_status](#message_status)|[task_group_status](#task_group_status)|  
  
##  <a name="agent_status"></a>agent_status 열거형  
 `agent`에 유효한 상태입니다.  
  
```
enum agent_status;
```  
### <a name="values"></a>값  
  
|이름|설명|  
|----------|-----------------|  
|`agent_canceled`|`agent`을 취소했습니다.|  
|`agent_created`|`agent` 생성 되었지만 시작 되지 않았습니다.|  
|`agent_done`|`agent` 취소 되지 않고 완료 합니다.|  
|`agent_runnable`|`agent` 시작 되었지만 입력 되지 않은 해당 `run` 메서드.|  
|`agent_started`|`agent` 시작 했습니다.|  

### <a name="remarks"></a>설명  
 자세한 내용은 참조 [비동기 에이전트](../../../parallel/concrt/asynchronous-agents.md)합니다.  

### <a name="requirements"></a>요구 사항  
 **헤더:** concrt.h

##  <a name="agents_eventtype"></a>Agents_EventType 열거형  
 에이전트 라이브러리에서 제공하는 추적 기능을 사용하여 추적할 수 있는 이벤트 형식입니다.  
  
```
enum Agents_EventType;
```  

### <a name="values"></a>값  
  
|이름|설명|  
|----------|-----------------|  
|`AGENTS_EVENT_CREATE`|개체의 생성을 나타내는 이벤트 형식입니다.|  
|`AGENTS_EVENT_DESTROY`|개체의 제거를 나타내는 이벤트 형식입니다.|  
|`AGENTS_EVENT_END`|일부 처리의 종료를 나타내는 이벤트 형식입니다.|  
|`AGENTS_EVENT_LINK`|메시지 블록의 연결을 나타내는 이벤트 형식입니다.|  
|`AGENTS_EVENT_NAME`|개체의 이름을 나타내는 이벤트 형식입니다.|  
|`AGENTS_EVENT_SCHEDULE`|프로세스의 일정을 나타내는 이벤트 형식입니다.|  
|`AGENTS_EVENT_START`|일부 처리의 시작을 나타내는 이벤트 형식입니다.|  
|`AGENTS_EVENT_UNLINK`|메시지 블록의 연결 해제를 나타내는 이벤트 형식입니다.|  

### <a name="requirements"></a>요구 사항  
 **헤더:** concrt.h

##  <a name="concrt_eventtype"></a>ConcRT_EventType 열거형  
 동시성 런타임에서 제공하는 추적 기능을 사용하여 추적할 수 있는 이벤트 형식입니다.  
  
```
enum ConcRT_EventType;
```  
### <a name="values"></a>값  
  
|이름|설명|  
|----------|-----------------|  
|`CONCRT_EVENT_ATTACH`|스케줄러에 연결 하는 작업을 나타내는 이벤트 형식입니다.|  
|`CONCRT_EVENT_BLOCK`|컨텍스트를 차단 하는 작업을 나타내는 이벤트 형식입니다.|  
|`CONCRT_EVENT_DETACH`|스케줄러에서 분리 하는 작업을 나타내는 이벤트 형식입니다.|  
|`CONCRT_EVENT_END`|시작/종료 이벤트 쌍의 시작을 표시 하는 이벤트 유형입니다.|  
|`CONCRT_EVENT_GENERIC`|기타 이벤트에 사용 되는 이벤트 유형입니다.|  
|`CONCRT_EVENT_IDLE`|유휴 상태로 전환 하는 컨텍스트의 동작을 나타내는 이벤트 형식입니다.|  
|`CONCRT_EVENT_START`|시작/종료 이벤트 쌍의 시작을 표시 하는 이벤트 유형입니다.|  
|`CONCRT_EVENT_UNBLOCK`|컨텍스트의 차단을 해제 하는 작업을 나타내는 이벤트 형식입니다.|  
|`CONCRT_EVENT_YIELD`|컨텍스트 생성 하는 작업을 나타내는 이벤트 형식입니다.|  
  
### <a name="requirements"></a>요구 사항  
 **헤더:** concrt.h  **Namespace:** 동시성

##  <a name="concrt_traceflags"></a>Concrt_TraceFlags 열거형  
 이벤트 형식에 대한 추적 플래그입니다.  
  
```
enum Concrt_TraceFlags;
```  
### <a name="values"></a>값  
  
|이름|설명|  
|----------|-----------------|  
|`AgentEventFlag`||  
|`AllEventsFlag`||  
|`ContextEventFlag`||  
|`PPLEventFlag`||  
|`ResourceManagerEventFlag`||  
|`SchedulerEventFlag`||  
|`VirtualProcessorEventFlag`||

### <a name="requirements"></a>요구 사항  
 **헤더:** concrt.h

##  <a name="criticalregiontype"></a>CriticalRegionType 열거형  
 컨텍스트가 있는 위험 영역의 형식입니다.  
  
```
enum CriticalRegionType;
```  
### <a name="values"></a>값  
  
|이름|설명|  
|----------|-----------------|  
|`InsideCriticalRegion`|컨텍스트가 중요 영역 내에 있음을 나타냅니다. 중요 영역 내에 있을 때 비동기 보류 스케줄러에서 숨겨집니다. 이런 보류 일어나지, 리소스 관리자 실행 가능 하 게 하 고 스케줄러를 다시 호출 하는 대신 다시 시작 하는 스레드 대기. 이러한 영역 내에서 잠금은 가져올 아주 조심 스럽게 고려해 야 합니다.|  
|`InsideHyperCriticalRegion`|컨텍스트가 매우 중요 한 영역 내에 있음을 나타냅니다. 매우 중요 한 영역 내에 있는 경우 동기 및 비동기 보류 스케줄러에서 숨겨집니다. 이런 보류 하거나 차단이 발생 하는 리소스 관리자 대기 스레드를 실행 가능 하 게 하 고 스케줄러를 다시 호출 하는 대신 다시 시작 합니다. 이러한 영역 내에 있는 잠금은 영역 외부에서 실행 되는 코드와 공유 해서는 안 됩니다. 이렇게 하면 예측할 수 없는 교착 상태가 발생 합니다.|  
|`OutsideCriticalRegion`|중요 영역 밖에 컨텍스트 임을 나타냅니다.|  
  
### <a name="requirements"></a>요구 사항  
 **헤더:** concrtrm.h 

##  <a name="dynamicprogressfeedbacktype"></a>DynamicProgressFeedbackType 열거형  
 `DynamicProgressFeedback` 정책에서 스케줄러에 대한 리소스를 스케줄러에서 수집한 통계 정보에 따라 균형을 조정할지, 아니면 `IVirtualProcessorRoot` 인터페이스의 `Activate` 및 `Deactivate` 메서드 호출을 통해 유휴 상태로 들어오고 나가는 가상 프로세서를 기준으로만 균형을 조정할지를 설명하는 데 사용됩니다. 사용 가능한 스케줄러 정책에 대 한 자세한 내용은 참조 하십시오. [PolicyElementKey](concurrency-namespace-enums.md)합니다.  
  
```
enum DynamicProgressFeedbackType;
```  
### <a name="values"></a>값  
  
|이름|설명|  
|----------|-----------------|  
|`ProgressFeedbackDisabled`|스케줄러에서 진행률 정보를 수집 하지 않습니다. 균형 조정 기본 하드웨어 스레드의 구독 수준에 따라 수행 됩니다. 구독 수준에 대 한 자세한 내용은 참조 하십시오. [iexecutionresource:: Currentsubscriptionlevel](IExecutionResource-structure.md)합니다.<br /><br /> 이 값은 런타임에서 사용 하기 위해 예약 되어 있습니다.|  
|`ProgressFeedbackEnabled`|진행률 정보를 수집 하 고 리소스 관리자에 게 전달 하는 스케줄러 합니다. 리소스 관리자는 리소스를 다시 기본 하드웨어 스레드의 구독 수준 외에도 스케줄러를 대신 하 여이 통계 정보를 사용 합니다. 구독 수준에 대 한 자세한 내용은 참조 하십시오. [iexecutionresource:: Currentsubscriptionlevel](IExecutionResource-structure.md)합니다.|  
##  <a name="join_type"></a>join_type 열거형  
 `join` 메시징 블록의 형식입니다.  
  
```
enum join_type;
```  
### <a name="values"></a>값  
  
|이름|설명|  
|----------|-----------------|  
|`greedy`|Greedy `join` 메시징 블록 전파 시 메시지를 즉시 적용 됩니다. 이 더 효율적 이지만 네트워크 구성에 따라 라이브 잠금 가능성이 있습니다.|  
|`non_greedy`|Non-greedy `join` 메시징 블록 메시지를 연기 하 고 해 모두 도착 한 후이 사용 합니다. 이러한 동작은 하지만 느려집니다 보장 됩니다.|  
  
### <a name="requirements"></a>요구 사항  
 **헤더:** agents.h  

##  <a name="message_status"></a>message_status 열거형  
 블록에 대한 `message` 개체 제공에 유효한 응답입니다.  
  
```
enum message_status;
```  
### <a name="values"></a>값  
  
|이름|설명|  
|----------|-----------------|  
|`accepted`|대상 메시지를 수락 합니다.|  
|`declined`|대상에서 메시지를 수락 하지 않았습니다.|  
|`missed`|대상 메시지를 수락 하 려 했지만 더 이상 사용할 수 있습니다.|  
|`postponed`|대상 메시지를 연기 합니다.|  
  
### <a name="requirements"></a>요구 사항  
 **헤더:** agents.h  

##  <a name="policyelementkey"></a>PolicyElementKey 열거형  
 스케줄러 동작의 측면을 설명하는 정책 키입니다. 각 정책 요소는 키-값 쌍으로 설명됩니다. 스케줄러에 스케줄러 정책 및 그 영향에 대 한 자세한 내용은 참조 [작업 스케줄러](../../../parallel/concrt/task-scheduler-concurrency-runtime.md)합니다.  
  
```
enum PolicyElementKey;
```  
### <a name="values"></a>값  
  
|이름|설명|  
|----------|-----------------|  
|`ContextPriority`|스케줄러에서 각 컨텍스트의 운영 체제 스레드 우선 순위입니다. 이 키 값으로 설정 되어 있으면 `INHERIT_THREAD_PRIORITY` 스케줄러에서 컨텍스트 스케줄러를 생성 하는 스레드의 우선 순위를 상속 합니다.<br /><br /> 유효한 값: Windows에 대 한 유효한 값이 하나라도 `SetThreadPriority` 함수 및 특수 값`INHERIT_THREAD_PRIORITY`<br /><br /> 기본값:`THREAD_PRIORITY_NORMAL`|  
|`ContextStackSize`|각 컨텍스트 (킬로바이트)에서 스케줄러에서 예약 된 스택 크기입니다.<br /><br /> 유효한 값: 양의 정수<br /><br /> 기본값: `0`, 나타내는 된 스택 크기에 대 한 프로세스의 기본 값이 사용 됩니다.|  
|`DynamicProgressFeedback`|스케줄러에 대 한 리소스가 스케줄러에서 수집한 또는 내부 하드웨어 스레드의 구독 수준에 따라만 통계 정보에 따라 균형 조정 수 있는지 여부를 결정 합니다. 자세한 내용은 참조 [DynamicProgressFeedbackType](#dynamicprogressfeedbacktype)합니다.<br /><br /> 유효한 값:의 멤버는 `DynamicProgressFeedbackType` 열거형 중 하나, `ProgressFeedbackEnabled` 또는`ProgressFeedbackDisabled`<br /><br /> 기본값:`ProgressFeedbackEnabled`|  
|`LocalContextCacheSize`|때는 `SchedulingProtocol` 정책 키 값으로 설정 되어 `EnhanceScheduleGroupLocality`,이 가상 프로세서 로컬 큐에 캐시 될 수는 실행 가능한 컨텍스트에의 최대 수를 지정 합니다. 이러한 컨텍스트는 일반적으로 실행 가능 하 게를 유발한 가상 프로세서에서 마지막에-선입 선출 (후입선출) 순서 대로 실행 됩니다. 이 정책 키에 의미가 없습니다 시기는 `SchedulingProtocol` 키가 값으로 설정 `EnhanceForwardProgress`합니다.<br /><br /> 유효한 값: 음수가 아닌 정수<br /><br /> 기본값:`8`|  
|`MaxConcurrency`|필요한 최대 동시성 수준 스케줄러가 있습니다. 리소스 관리자는 처음에 많은 가상 프로세서를 할당 하려고 합니다. 특수 값 [MaxExecutionResources](concurrency-namespace-constants1.md#maxexecutionresources) 원하는 동시성 수준이 동일한 시스템에 있는 하드웨어 스레드 수가 임을 나타냅니다. 에 대 한 지정 된 값이 `MinConcurrency` 시스템에 있는 하드웨어 스레드 수보다 크면 및 `MaxConcurrency` 로 지정 된 `MaxExecutionResources`에 대 한 값 `MaxConcurrency` 는에 설정 된 것과 일치 하기 위해 발생 `MinConcurrency`합니다.<br /><br /> 유효한 값: 양의 정수 및 특수 값`MaxExecutionResources`<br /><br /> 기본값:`MaxExecutionResources`|  
|`MaxPolicyElementKey`|최대 정책 요소 키입니다. 유효한 요소 키가 없습니다.|  
|`MinConcurrency`|리소스 관리자가 스케줄러에 제공 해야 하는 최소 동시성 수준입니다. 스케줄러에 할당 된 가상 프로세서 수가 최소 이동 하지 않습니다. 특수 값 [MaxExecutionResources](concurrency-namespace-constants1.md#maxexecutionresources) 최소 동시성 수준 시스템에 있는 하드웨어 스레드 수가 동일 임을 나타냅니다. 에 대 한 지정 된 값이 `MaxConcurrency` 시스템에 있는 하드웨어 스레드 수보다 작으면 및 `MinConcurrency` 로 지정 된 `MaxExecutionResources`에 대 한 값 `MinConcurrency` 에 대해 설정 된 것과 일치 하도록 낮아집니다은 `MaxConcurrency`합니다.<br /><br /> 유효한 값: 음수가 아닌 정수 및 특수 값 `MaxExecutionResources`합니다. 동시성 런타임이 스케줄러의 생성에 사용되는 스케줄러 정책의 경우에는 값 `0`이 유효하지 않습니다.<br /><br /> 기본값:`1`|  
|`SchedulerKind`|스레드 스케줄러 기본 실행 컨텍스트를 활용 하는 형식입니다. 자세한 내용은 참조 [SchedulerType](#schedulertype)합니다.<br /><br /> 유효한 값: `SchedulerType` 열거형의 멤버. 예: `ThreadScheduler`<br /><br /> 기본값: `ThreadScheduler`합니다. 이 모든 운영 체제에서 Win32 스레드를 변환 합니다.|  
|`SchedulingProtocol`|스케줄러에서 사용할 예약 알고리즘을 설명 합니다. 자세한 내용은 참조 [SchedulingProtocolType](#schedulingprotocoltype)합니다.<br /><br /> 유효한 값:의 멤버는 `SchedulingProtocolType` 열거형 중 하나, `EnhanceScheduleGroupLocality` 또는`EnhanceForwardProgress`<br /><br /> 기본값:`EnhanceScheduleGroupLocality`|  
|`TargetOversubscriptionFactor`|하드웨어 스레드 당 가상 프로세서의 미정 수입니다. 필요할 경우 시스템의 하드웨어 스레드로 `MaxConcurrency`를 만족시키기 위해 리소스 관리자에서 대상 초과 구독 비율을 증가시킬 수 있습니다.<br /><br /> 유효한 값: 양의 정수<br /><br /> 기본값:`1`|  
|`WinRTInitialization`||  
  
### <a name="requirements"></a>요구 사항  
 **헤더:** concrt.h  

##  <a name="schedulertype"></a>SchedulerType 열거형  
 `SchedulerKind` 정책에서 스케줄러가 기본 실행 컨텍스트에 활용해야 하는 스레드 형식을 설명하는 데 사용됩니다. 사용 가능한 스케줄러 정책에 대 한 자세한 내용은 참조 하십시오. [PolicyElementKey](concurrency-namespace-enums.md)합니다.  
  
```
enum SchedulerType;
``` 

### <a name="values"></a>값  
  
|이름|설명|  
|----------|-----------------|  
|`ThreadScheduler`|일반 Win32 스레드의 명시적 요청을 나타냅니다.|  
|`UmsThreadDefault`|사용자 모드 예약 가능 (UMS) 스레드는 동시성 런타임에서 Visual Studio 2013에서 지원 되지 않습니다. `UmsThreadDefault`를 `SchedulerType` 정책의 값으로 사용하면 오류가 발생하지 않습니다. 그러나 해당 정책을 사용하여 만들어진 스케줄러는 기본적으로 Win32 스레드를 사용합니다.|  
  
### <a name="requirements"></a>요구 사항  
 **헤더:** concrt.h  
  
##  <a name="schedulingprotocoltype"></a>SchedulingProtocolType 열거형  
 `SchedulingProtocol` 정책에서 스케줄러에 활용되는 일정 알고리즘을 설명하는 데 사용됩니다. 사용 가능한 스케줄러 정책에 대 한 자세한 내용은 참조 하십시오. [PolicyElementKey](concurrency-namespace-enums.md)합니다.  
  
```
enum SchedulingProtocolType;
```  
### <a name="values"></a>값  
  
|이름|설명|  
|----------|-----------------|  
|`EnhanceForwardProgress`|스케줄러는 라운드 로빈 일정 그룹을 통해 각 작업을 실행 합니다. 차단 되지 않은 컨텍스트는 일반적으로 선입 선출 (FIFO) 방식으로 예약 됩니다. 가상 프로세서는 차단 되지 않은 컨텍스트를 캐시 하지 않습니다.|  
|`EnhanceScheduleGroupLocality`|스케줄러는 다른 일정 그룹으로 이동 하기 전에 현재 일정 그룹 내에서 작업을 계속 합니다. 차단 되지 않은 컨텍스트 가상 프로세서 당 캐시 되 고 차단 하지 않는 있는 가상 프로세서를 마지막에-선입 선출 (후입선출) 방식으로 일반적으로 예약 됩니다.|  
  
### <a name="requirements"></a>요구 사항  
 **헤더:** concrt.h  
 
##  <a name="switchingproxystate"></a>SwitchingProxyState 열거형  
 다른 스레드 프록시로의 협조적 컨텍스트 전환을 실행하는 경우 스레드 프록시의 현재 상태를 나타내는 데 사용됩니다.  
  
```
enum SwitchingProxyState;
```  
### <a name="values"></a>값  
  
|이름|설명|  
|----------|-----------------|  
|`Blocking`|호출 스레드가 협조적으로 차단 하 고 단독으로 소유 해야 호출자가 이후에 다시 실행 하 고 다른 작업을 수행 될 때까지 나타냅니다.|  
|`Idle`|호출 스레드 스케줄러에서 더 이상 필요 없는 리소스 관리자에서 반환 되는 있음을 나타냅니다. 디스패치 중인 하는 컨텍스트를 더 이상 리소스 관리자에서 사용할 수 없습니다.|  
|`Nesting`|호출 스레드가 자식 스케줄러를 중첩 되 고 다른 스케줄러를 연결 하려면 호출자가 필요한 나타냅니다.|  

### <a name="remarks"></a>주의  
 형식의 매개 변수가 `SwitchingProxyState` 메서드에 전달 `IThreadProxy::SwitchTo` 리소스 관리자는 호출 스레드 프록시를 처리 하는 방법을 알려 줍니다.  
  
 이 형식은 사용 방법에 대 한 자세한 내용은 참조 하십시오. [ithreadproxy:: Switchto](ithreadproxy-structure.md#switchto)합니다.  
  
##  <a name="task_group_status"></a>task_group_status 열거형  
 `task_group` 또는 `structured_task_group` 개체의 실행 상태를 설명합니다. 이 형식의 값은 작업 그룹에 예약된 작업이 완료되기를 기다리는 수많은 메서드에 의해 반환됩니다.  
  
```
enum task_group_status;
```  
### <a name="values"></a>값  
  
|이름|설명|  
|----------|-----------------|  
|`canceled`|`task_group` 또는 `structured_task_group` 개체가 취소되었습니다. 하나 이상의 작업이 실행되지 않았을 수 있습니다.|  
|`completed`|`task_group` 또는 `structured_task_group` 개체의 큐에 대기 중인 작업이 성공적으로 완료되었습니다.|  
|`not_complete`|`task_group` 개체의 큐에 대기 중인 작업이 완료되지 않았습니다. 이 값은 현재 동시성 런타임에서 반환되지 않습니다.|  
  
### <a name="requirements"></a>요구 사항  
 **헤더:** pplinterface.h  

##  <a name="winrtinitializationtype"></a>WinRTInitializationType 열거형  
 `WinRTInitialization` 정책에서 Windows 8 또는 그 이상 버전의 운영 체제에서 실행되는 응용 프로그램에 대한 스케줄러 스레드에서 Windows 런타임이 초기화될지 여부와 초기화되는 방법을 설명하는데 사용됩니다. 사용 가능한 스케줄러 정책에 대 한 자세한 내용은 참조 하십시오. [PolicyElementKey](concurrency-namespace-enums.md)합니다.  
  
```
enum WinRTInitializationType;
```  
### <a name="values"></a>값  
  
|이름|설명|  
|----------|-----------------|  
|`DoNotInitializeWinRT`|응용 프로그램이 Windows 8 또는 그 이상 버전의 운영 체제에서 실행될 경우 스케줄러 내의 스레드는 Windows 런타임을 초기화하지 않습니다.|  
|`InitializeWinRTAsMTA`|응용 프로그램이 Windows 8 또는 그 이상 버전의 운영 체제에서 실행할 경우 스케줄러 내의 각 스레드는 Windows 런타임을 초기화하고 이것을 멀티스레드의 일부로 선언합니다.|  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** concrt.h  

## <a name="see-also"></a>참고 항목  
 [concurrency 네임스페이스](concurrency-namespace.md)
