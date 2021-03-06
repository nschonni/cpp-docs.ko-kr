---
title: SemaphoreTraits 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 09/27/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::SemaphoreTraits
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::SemaphoreTraits::Unlock
dev_langs:
- C++
helpviewer_keywords:
- Microsoft::WRL::Wrappers::HandleTraits::SemaphoreTraits structure
- Microsoft::WRL::Wrappers::HandleTraits::SemaphoreTraits::Unlock method
ms.assetid: eddb8576-d063-409b-9201-cc87ca5d111e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 553d0cbb69bcf3167974cb42abb26f4aae04bfb3
ms.sourcegitcommit: 1d9bd38cacbc783fccd3884b7b92062161c91c84
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/03/2018
ms.locfileid: "48234140"
---
# <a name="semaphoretraits-structure"></a>SemaphoreTraits 구조체

일반적인 특성 정의 `Semaphore` 개체입니다.

## <a name="syntax"></a>구문

```cpp
struct SemaphoreTraits : HANDLENullTraits;
```

## <a name="members"></a>멤버

### <a name="public-methods"></a>Public 메서드

이름                               | 설명
---------------------------------- | --------------------------------------
[Semaphoretraits:: Unlock](#unlock) | 공유 리소스의 릴리스 컨트롤입니다.

## <a name="inheritance-hierarchy"></a>상속 계층

`HANDLENullTraits`

`SemaphoreTraits`

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers::HandleTraits

## <a name="unlock"></a>Semaphoretraits:: Unlock

공유 리소스의 릴리스 컨트롤입니다.

```cpp
inline static void Unlock(
   _In_ Type h
);
```

### <a name="parameters"></a>매개 변수

*h*<br/>
에 대 한 핸들을 `Semaphore` 개체입니다.

### <a name="remarks"></a>설명

잠금 해제 작업이 성공적 이면 `Unlock()` 실패의 원인을 나타내는 오류를 생성 합니다.
