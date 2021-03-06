---
title: 'Module:: releasenotifier 클래스 | Microsoft Docs'
ms.custom: ''
ms.date: 09/17/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::Module::ReleaseNotifier
- module/Microsoft::WRL::Module::ReleaseNotifier::~ReleaseNotifier
- module/Microsoft::WRL::Module::ReleaseNotifier::Invoke
- module/Microsoft::WRL::Module::ReleaseNotifier::Release
- module/Microsoft::WRL::Module::ReleaseNotifier::ReleaseNotifier
dev_langs:
- C++
helpviewer_keywords:
- Microsoft::WRL::Module::ReleaseNotifier class
- Microsoft::WRL::Module::ReleaseNotifier::~ReleaseNotifier, destructor
- Microsoft::WRL::Module::ReleaseNotifier::Invoke method
- Microsoft::WRL::Module::ReleaseNotifier::Release method
- Microsoft::WRL::Module::ReleaseNotifier::ReleaseNotifier, constructor
ms.assetid: 17249cd1-4d88-42e3-8146-da9e942d12bd
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 2128164fe3196a77991e755b865357e1aefcac23
ms.sourcegitcommit: 0164af5615389ffb1452ccc432eb55f6dc931047
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49808487"
---
# <a name="modulereleasenotifier-class"></a>Module::ReleaseNotifier 클래스

모듈의 마지막 개체가 해제될 때 이벤트 처리기를 호출합니다.

## <a name="syntax"></a>구문

```cpp
class ReleaseNotifier;
```

## <a name="members"></a>멤버

### <a name="public-constructors"></a>Public 생성자

이름                                                                                | 설명
----------------------------------------------------------------------------------- | --------------------------------------------------------------------------
[Module:: releasenotifier:: ~ ReleaseNotifier](#releasenotifier-tilde-releasenotifier) | 현재 인스턴스를 초기화 해제는 `Module::ReleaseNotifier` 클래스입니다.
[Module::ReleaseNotifier::ReleaseNotifier](#releasenotifier-releasenotifier)        | `Module::ReleaseNotifier` 클래스의 새 인스턴스를 초기화합니다.

### <a name="public-methods"></a>Public 메서드

이름                                                         | 설명
------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------
[Module:: releasenotifier:: 호출](#releasenotifier-invoke)   | 구현될 때 모듈의 마지막 개체가 해제되면 이벤트 처리기를 호출합니다.
[Module::ReleaseNotifier::Release](#releasenotifier-release) | 현재 삭제 `Module::ReleaseNotifier` 개체의 매개 변수를 사용 하 여 생성 된 개체 **true**합니다.

## <a name="inheritance-hierarchy"></a>상속 계층

`ReleaseNotifier`

## <a name="requirements"></a>요구 사항

**헤더:** module.h

**네임스페이스:** Microsoft::WRL

## <a name="releasenotifier-tilde-releasenotifier"></a>Module:: releasenotifier:: ~ ReleaseNotifier

현재 인스턴스를 초기화 해제는 `Module::ReleaseNotifier` 클래스입니다.

```cpp
WRL_NOTHROW virtual ~ReleaseNotifier();
```

## <a name="releasenotifier-invoke"></a>Module:: releasenotifier:: 호출

구현될 때 모듈의 마지막 개체가 해제되면 이벤트 처리기를 호출합니다.

```cpp
virtual void Invoke() = 0;
```

## <a name="releasenotifier-release"></a>Module::ReleaseNotifier::Release

현재 삭제 `Module::ReleaseNotifier` 개체의 매개 변수를 사용 하 여 생성 된 개체 **true**합니다.

```cpp
void Release() throw();
```

## <a name="releasenotifier-releasenotifier"></a>Module::ReleaseNotifier::ReleaseNotifier

`Module::ReleaseNotifier` 클래스의 새 인스턴스를 초기화합니다.

```cpp
ReleaseNotifier(bool release) throw();
```

### <a name="parameters"></a>매개 변수

*release*<br/>
`true` 삭제 하려면이 인스턴스에 `Release` 메서드 호출 됩니다. `false` 이 인스턴스를 삭제 하지 않도록 합니다.
