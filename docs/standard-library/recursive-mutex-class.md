---
title: "recursive_mutex 클래스 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- mutex/std::recursive_mutex
dev_langs:
- C++
ms.assetid: eb5ffd1b-7e78-4559-8391-bb220ead42fc
caps.latest.revision: 9
author: corob-msft
ms.author: corob
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
ms.sourcegitcommit: a937c9d083a7e4331af63323a19fb207142604a0
ms.openlocfilehash: c82c8302be5d3e01de90adda2049a022100b8443
ms.lasthandoff: 02/24/2017

---
# <a name="recursivemutex-class"></a>recursive_mutex 클래스
*뮤텍스 형식*을 나타냅니다. [mutex](../standard-library/mutex-class-stl.md)와 달리 이미 잠겨 있는 개체에 대한 잠금 메서드 호출 동작은 적절하게 정의됩니다.  
  
## <a name="syntax"></a>구문  
  
```
class recursive_mutex;
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[recursive_mutex 생성자](#recursive_mutex__recursive_mutex_constructor)|`recursive_mutex` 개체를 생성합니다.|  
|[~recursive_mutex 소멸자](#recursive_mutex___dtorrecursive_mutex_destructor)|`recursive_mutex` 개체에서 사용하는 리소스를 모두 해제합니다.|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[lock](#recursive_mutex__lock_method)|스레드가 뮤텍스의 소유권을 가져올 때까지 호출 스레드를 차단합니다.|  
|[try_lock](#recursive_mutex__try_lock_method)|차단되지 않고 뮤텍스의 소유권을 가져오려고 시도합니다.|  
|[unlock](#recursive_mutex__unlock_method)|뮤텍스의 소유권을 해제합니다.|  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** mutex  
  
 **네임스페이스:** std  
  
##  <a name="a-namerecursivemutexlockmethoda--lock"></a><a name="recursive_mutex__lock_method"></a>  lock  
 스레드가 `mutex`의 소유권을 가져올 때까지 호출 스레드를 차단합니다.  
  
```cpp  
void lock();
```  
  
### <a name="remarks"></a>설명  
 호출 스레드가 `mutex`를 이미 소유하고 있으면 메서드는 결과를 즉시 반환하며 이전 잠금은 적용된 상태로 유지됩니다.  
  
##  <a name="a-namerecursivemutexrecursivemutexconstructora--recursivemutex"></a><a name="recursive_mutex__recursive_mutex_constructor"></a>  recursive_mutex  
 잠기지 않은 `recursive_mutex` 개체를 생성합니다.  
  
```cpp  
recursive_mutex();
```  
  
##  <a name="a-namerecursivemutexdtorrecursivemutexdestructora--recursivemutex"></a><a name="recursive_mutex___dtorrecursive_mutex_destructor"></a>  ~recursive_mutex  
 개체에서 사용하는 리소스를 모두 해제합니다.  
  
```cpp  
~recursive_mutex();
```  
  
### <a name="remarks"></a>설명  
 소멸자가 실행될 때 개체가 잠겨 있는 경우, 이 동작은 정의되지 않습니다.  
  
##  <a name="a-namerecursivemutextrylockmethoda--trylock"></a><a name="recursive_mutex__try_lock_method"></a>  try_lock  
 차단되지 않고 `mutex`의 소유권을 가져오려고 시도합니다.  
  
```cpp  
bool try_lock() noexcept;
```  
  
### <a name="return-value"></a>반환 값  
 메서드가 `mutex`의 소유권을 정상적으로 가져오거나 호출 스레드가 `mutex`를 이미 소유하고 있으면 `true`이고 그렇지 않으면 `false`입니다.  
  
### <a name="remarks"></a>설명  
 호출 스레드가 `mutex`를 이미 소유하고 있으면 함수는 `true`를 즉시 반환하며 이전 잠금은 적용된 상태로 유지됩니다.  
  
##  <a name="a-namerecursivemutexunlockmethoda--unlock"></a><a name="recursive_mutex__unlock_method"></a>  unlock  
 뮤텍스의 소유권을 해제합니다.  
  
```cpp  
void unlock();
```  
  
### <a name="remarks"></a>설명  
 이 메서드는 `recursive_mutex` 개체에 대해 [lock](#recursive_mutex__lock_method) 및 [try_lock](#recursive_mutex__try_lock_method)이 정상적으로 호출된 횟수만큼 호출된 후에만 `mutex`의 소유권을 해제합니다.  
  
 호출 스레드가 `mutex`를 소유하지 않은 경우, 이 동작은 정의되지 않습니다.  
  
## <a name="see-also"></a>참고 항목  
 [헤더 파일 참조](../standard-library/cpp-standard-library-header-files.md)   
 [\<mutex>](../standard-library/mutex.md)



