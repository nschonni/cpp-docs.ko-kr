---
title: SRWLock 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 09/25/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::SRWLock
- corewrappers/Microsoft::WRL::Wrappers::SRWLock::LockExclusive
- corewrappers/Microsoft::WRL::Wrappers::SRWLock::LockShared
- corewrappers/Microsoft::WRL::Wrappers::SRWLock::SRWLock
- corewrappers/Microsoft::WRL::Wrappers::SRWLock::SRWLock_
- corewrappers/Microsoft::WRL::Wrappers::SRWLock::~SRWLock
- corewrappers/Microsoft::WRL::Wrappers::SRWLock::TryLockExclusive
- corewrappers/Microsoft::WRL::Wrappers::SRWLock::TryLockShared
dev_langs:
- C++
helpviewer_keywords:
- Microsoft::WRL::Wrappers::SRWLock class
- Microsoft::WRL::Wrappers::SRWLock::LockExclusive method
- Microsoft::WRL::Wrappers::SRWLock::LockShared method
- Microsoft::WRL::Wrappers::SRWLock::SRWLock, constructor
- Microsoft::WRL::Wrappers::SRWLock::SRWLock_ data member
- Microsoft::WRL::Wrappers::SRWLock::~SRWLock, destructor
- Microsoft::WRL::Wrappers::SRWLock::TryLockExclusive method
- Microsoft::WRL::Wrappers::SRWLock::TryLockShared method
ms.assetid: 4fa250e3-5f29-4b06-ac24-61b6c04ade93
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 771a375d46177bb3b9d263f0a5221039bb963bc2
ms.sourcegitcommit: 1d9bd38cacbc783fccd3884b7b92062161c91c84
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/03/2018
ms.locfileid: "48233972"
---
# <a name="srwlock-class"></a>SRWLock 클래스

슬림 판독기/작성기 잠금을 나타냅니다.

## <a name="syntax"></a>구문

```cpp
class SRWLock;
```

## <a name="remarks"></a>설명

슬림 판독기/기록기 잠금 개체 또는 리소스에는 스레드 간에 액세스를 동기화에 사용 됩니다. 자세한 내용은 [동기화 함수](/windows/desktop/Sync/synchronization-functions)합니다.

## <a name="members"></a>멤버

### <a name="public-typedefs"></a>공용 Typedefs

이름                | 설명
------------------- | -------------------------------------------------------------------
`SyncLockExclusive` | 에 대 한 동의어를 `SRWLock` 배타 모드에 획득 된 개체입니다.
`SyncLockShared`    | 에 대 한 동의어를 `SRWLock` 공유 모드에서 획득 된 개체입니다.

### <a name="public-constructors"></a>Public 생성자

이름                                     | 설명
---------------------------------------- | --------------------------------------------------
[Srwlock:: Srwlock](#srwlock-constructor) | `SRWLock` 클래스의 새 인스턴스를 초기화합니다.
[SRWLock:: ~ SRWLock](#tilde-srwlock)      | 인스턴스를 초기화 해제는 `SRWLock` 클래스입니다.

### <a name="public-methods"></a>Public 메서드

이름                                           | 설명
---------------------------------------------- | -------------------------------------------------------------------------------------------------------
[Srwlock:: Lockexclusive](#lockexclusive)       | 획득 한 `SRWLock` 단독 모드의 개체입니다.
[Srwlock:: Lockshared](#lockshared)             | 획득 한 `SRWLock` 공유 모드의 개체입니다.
[Srwlock:: Trylockexclusive](#trylockexclusive) | 획득 하 려 한 `SRWLock` 현재 또는 지정 된 단독 모드의 개체 `SRWLock` 개체입니다.
[Srwlock:: Trylockshared](#trylockshared)       | 획득 하 려는 `SRWLock` 개체를 현재 또는 지정 된 공유 모드로 `SRWLock` 개체입니다.

### <a name="protected-data-member"></a>보호 된 데이터 멤버

이름                                      | 설명
----------------------------------------- | -----------------------------------------------------------------------
[Srwlock:: Srwlock_](#srwlock-data-member) | 현재 기본 잠금 변수를 포함 `SRWLock` 개체입니다.

## <a name="inheritance-hierarchy"></a>상속 계층

`SRWLock`

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers

## <a name="tilde-srwlock"></a>SRWLock:: ~ SRWLock

인스턴스를 초기화 해제는 `SRWLock` 클래스입니다.

```cpp
~SRWLock();
```

## <a name="lockexclusive"></a>Srwlock:: Lockexclusive

획득 한 `SRWLock` 단독 모드의 개체입니다.

```cpp
SyncLockExclusive LockExclusive();

static SyncLockExclusive LockExclusive(
   _In_ SRWLOCK* lock
);
```

### <a name="parameters"></a>매개 변수

*lock*<br/>
에 대 한 포인터를 `SRWLock` 개체입니다.

### <a name="return-value"></a>반환 값

`SRWLock` 단독 모드의 개체입니다.

## <a name="lockshared"></a>Srwlock:: Lockshared

획득 한 `SRWLock` 공유 모드의 개체입니다.

```cpp
SyncLockShared LockShared();

static SyncLockShared LockShared(
   _In_ SRWLOCK* lock
);
```

### <a name="parameters"></a>매개 변수

*lock*<br/>
에 대 한 포인터를 `SRWLock` 개체입니다.

### <a name="return-value"></a>반환 값

`SRWLock` 공유 모드의 개체입니다.

## <a name="srwlock-constructor"></a>Srwlock:: Srwlock

`SRWLock` 클래스의 새 인스턴스를 초기화합니다.

```cpp
SRWLock();
```

## <a name="srwlock-data-member"></a>Srwlock:: Srwlock_

현재 기본 잠금 변수를 포함 `SRWLock` 개체입니다.

```cpp
SRWLOCK SRWLock_;
```

## <a name="trylockexclusive"></a>Srwlock:: Trylockexclusive

획득 하 려 한 `SRWLock` 현재 또는 지정 된 단독 모드의 개체 `SRWLock` 개체입니다. 호출이 성공 하면 호출 스레드는 잠금 소유권을 받습니다.

```cpp
SyncLockExclusive TryLockExclusive();

static SyncLockExclusive TryLockExclusive(
   _In_ SRWLOCK* lock
);
```

### <a name="parameters"></a>매개 변수

*lock*<br/>
에 대 한 포인터를 `SRWLock` 개체입니다.

### <a name="return-value"></a>반환 값

성공 하면는 `SRWLock` 개체 단독 모드 및 호출 스레드는 잠금 소유권을 받습니다. 그렇지 않은 경우는 `SRWLock` 개체 상태가 올바르지 않습니다.

## <a name="trylockshared"></a>Srwlock:: Trylockshared

획득 하 려는 `SRWLock` 개체를 현재 또는 지정 된 공유 모드로 `SRWLock` 개체입니다.

```cpp
WRL_NOTHROW SyncLockShared TryLockShared();
WRL_NOTHROW static SyncLockShared TryLockShared(
   _In_ SRWLOCK* lock
);
```

### <a name="parameters"></a>매개 변수

*lock*<br/>
에 대 한 포인터를 `SRWLock` 개체입니다.

### <a name="return-value"></a>반환 값

성공 하면는 `SRWLock` 개체 공유 모드 및 호출 스레드는 잠금 소유권을 받습니다. 그렇지 않은 경우는 `SRWLock` 개체 상태가 올바르지 않습니다.
