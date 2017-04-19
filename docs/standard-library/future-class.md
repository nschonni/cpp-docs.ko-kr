---
title: "future 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- future/std::future
dev_langs:
- C++
ms.assetid: 495e82c3-5341-4e37-87dd-b40107fbdfb6
caps.latest.revision: 13
author: corob-msft
ms.author: corob
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
ms.sourcegitcommit: a937c9d083a7e4331af63323a19fb207142604a0
ms.openlocfilehash: 6de4fecd3f5f65ac48cbb49f2ed4f874f4283487
ms.lasthandoff: 02/24/2017

---
# <a name="future-class"></a>future 클래스
*비동기 반환 개체*를 설명합니다.  
  
## <a name="syntax"></a>구문  
  
```
template <class Ty>
class future;
```  
  
## <a name="remarks"></a>설명  
 각 표준 *비동기 공급자*는 이 템플릿의 인스턴스화 형식이 포함된 개체를 반환합니다. 연결된 비동기 공급자에 액세스하려면 `future` 개체를 사용해야 합니다. 동일한 비동기 공급자와 연결된 여러 비동기 반환 개체가 필요할 경우 `future` 개체를 [shared_future](../standard-library/shared-future-class.md) 개체에 복사합니다.  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[future::future 생성자](#future__future_constructor)|`future` 개체를 생성합니다.|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[future::get](#future__get_method)|연결된 비동기 상태에 저장된 결과를 검색합니다.|  
|[future::share](#future__share_method)|개체를 `shared_future`로 변환합니다.|  
|[future::valid](#future__valid_method)|개체가 비어 있지 않은지 여부를 지정합니다.|  
|[future::wait](#future__wait_method)|연결된 비동기 상태가 ready로 설정될 때까지 현재 스레드를 차단합니다.|  
|[future::wait_for](#future__wait_for_method)|연결된 비동기 상태가 준비로 설정되거나 지정된 시간이 경과할 때까지 차단합니다.|  
|[future::wait_until](#future__wait_until_method)|연결된 비동기 상태가 준비로 설정되거나 지정된 시점이 될 때까지 차단합니다.|  
  
### <a name="public-operators"></a>Public 연산자  
  
|이름|설명|  
|----------|-----------------|  
|[future::operator=](#future__operator_eq)|지정된 개체에서 연결된 비동기 상태를 전송합니다.|  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** future  
  
 **네임스페이스:** std  
  
##  <a name="a-namefuturefutureconstructora--futurefuture-constructor"></a><a name="future__future_constructor"></a>  future::future 생성자  
 `future` 개체를 생성합니다.  
  
```
future() noexcept;
future(future&& Other) noexcept;
```  
  
### <a name="parameters"></a>매개 변수  
 `Other`  
 `future` 개체입니다.  
  
### <a name="remarks"></a>설명  
 첫 번째 생성자는 연결된 비동기 상태가 없는 `future` 개체를 구성합니다.  
  
 두 번째 생성자는 `future` 개체를 생성하며 `Other`로부터 연결된 비동기 상태를 전송합니다. `Other`에는 더 이상 연결된 비동기 상태가 없습니다.  
  
##  <a name="a-namefuturegetmethoda--futureget"></a><a name="future__get_method"></a>  future::get  
 연결된 비동기 상태에 저장된 결과를 검색합니다.  
  
```
Ty get();
```  
  
### <a name="return-value"></a>반환 값  
 결과가 예외이면 메서드는 예외를 다시 throw합니다. 그렇지 않으면 결과가 반환됩니다.  
  
### <a name="remarks"></a>설명  
 이 메서드는 결과를 검색하기 전에 연결된 비동기 상태가 준비로 설정될 때까지 현재 스레드를 차단합니다.  
  
 부분 특수화 `future<Ty&>`의 경우 저장되는 값은 실제로는 반환 값으로 비동기 공급자에 전달된 개체에 대한 참조입니다.  
  
 특수화 `future<void>`에 대해서는 저장된 값이 없으므로 메서드는 `void`를 반환합니다.  
  
 다른 특수화에서 메서드는 저장된 값에서 반환 값을 이동합니다. 따라서 이 메서드를 한 번만 호출합니다.  
  
##  <a name="a-namefutureoperatoreqa--futureoperator"></a><a name="future__operator_eq"></a>  future::operator=  
 지정된 개체에서 연결된 비동기 상태를 전송합니다.  
  
```
future& operator=(future&& Right) noexcept;
```  
  
### <a name="parameters"></a>매개 변수  
 `Right`  
 `future` 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 `*this`  
  
### <a name="remarks"></a>설명  
 전송 후 `Right`에는 더 이상 연결된 비동기 상태가 없습니다.  
  
##  <a name="a-namefuturesharemethoda--futureshare"></a><a name="future__share_method"></a>  future::share  
 개체를 [shared_future](../standard-library/shared-future-class.md) 개체로 변환합니다.  
  
```
shared_future<Ty> share();
```  
  
### <a name="return-value"></a>반환 값  
 `shared_future(move(*this))`  
  
##  <a name="a-namefuturevalidmethoda--futurevalid"></a><a name="future__valid_method"></a>  future::valid  
 개체에 연결된 비동기 상태가 있는지 여부를 지정합니다.  
  
```
bool valid() noexcept;
```  
  
### <a name="return-value"></a>반환 값  
 개체가 연결된 비동기 상태이면 `true`이고, 그렇지 않으면 `false`입니다.  
  
##  <a name="a-namefuturewaitmethoda--futurewait"></a><a name="future__wait_method"></a>  future::wait  
 연결된 비동기 상태가 *준비*로 설정될 때까지 현재 스레드를 차단합니다.  
  
```cpp  
void wait() const;
```  
  
### <a name="remarks"></a>설명  
 연결된 비동기 상태는 해당 비동기 공급자가 반환 값을 저장했거나 예외를 저장한 경우에만 *준비*입니다.  
  
##  <a name="a-namefuturewaitformethoda--futurewaitfor"></a><a name="future__wait_for_method"></a>  future::wait_for  
 연결된 비동기 상태가 *준비*로 설정되거나 지정된 시간 간격이 경과할 때까지 현재 스레드를 차단합니다.  
  
```
template <class Rep, class Period>
future_status wait_for(const chrono::duration<Rep, Period>& Rel_time) const;
```  
  
### <a name="parameters"></a>매개 변수  
 `Rel_time`  
 스레드가 차단되는 최대 시간 간격을 지정하는 [chrono::duration](../standard-library/duration-class.md) 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 반환 이유를 나타내는 [future_status](../standard-library/future-enums.md#future_status_enumeration)입니다.  
  
### <a name="remarks"></a>설명  
 연결된 비동기 상태는 해당 비동기 공급자가 반환 값을 저장했거나 예외를 저장한 경우에만 준비입니다.  
  
##  <a name="a-namefuturewaituntilmethoda--futurewaituntil"></a><a name="future__wait_until_method"></a>  future::wait_until  
 연결된 비동기 상태가 *준비*가 되거나 지정된 시점이 지날 때까지 현재 스레드를 차단합니다.  
  
```cpp  
template <class Clock, class Duration>
future_status wait_until(const chrono::time_point<Clock, Duration>& Abs_time) const;
```  
  
### <a name="parameters"></a>매개 변수  
 `Abs_time`  
 스레드 차단을 해제할 수 있는 시간을 지정하는 [chrono::time_point](../standard-library/time-point-class.md) 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 반환 이유를 나타내는 [future_status](../standard-library/future-enums.md#future_status_enumeration)입니다.  
  
### <a name="remarks"></a>설명  
 연결된 비동기 상태는 해당 비동기 공급자가 반환 값을 저장했거나 예외를 저장한 경우에만 *준비*입니다.  
  
## <a name="see-also"></a>참고 항목  
 [헤더 파일 참조](../standard-library/cpp-standard-library-header-files.md)   
 [\<future>](../standard-library/future.md)



