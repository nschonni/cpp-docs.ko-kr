---
title: HANDLETraits 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 09/27/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::HANDLETraits
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::HANDLETraits::Close
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::HANDLETraits::GetInvalidValue
dev_langs:
- C++
helpviewer_keywords:
- Microsoft::WRL::Wrappers::HandleTraits::HANDLETraits structure
- Microsoft::WRL::Wrappers::HandleTraits::HANDLETraits::Close method
- Microsoft::WRL::Wrappers::HandleTraits::HANDLETraits::GetInvalidValue method
ms.assetid: 22963e88-d857-4624-9182-7c986daff722
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 3e670dca205f07d1e13a93f8acd0df5965b45109
ms.sourcegitcommit: 8480f16893f09911f08a58caf684405404f7ac8e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49161712"
---
# <a name="handletraits-structure"></a>HANDLETraits 구조체

핸들의 공통 된 특징을 정의합니다.

## <a name="syntax"></a>구문

```cpp
struct HANDLETraits;
```

## <a name="members"></a>멤버

### <a name="public-typedefs"></a>공용 Typedefs

이름   | 설명
------ | ---------------------
`Type` | 핸들에 대 한 동의어입니다.

### <a name="public-methods"></a>Public 메서드

이름                                              | 설명
------------------------------------------------- | -----------------------------
[Handletraits:: Close](#close)                     | 지정된 된 핸들을 닫습니다.
[Handletraits:: Getinvalidvalue](#getinvalidvalue) | 잘못 된 핸들을 나타냅니다.

## <a name="inheritance-hierarchy"></a>상속 계층

`HANDLETraits`

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers::HandleTraits

## <a name="close"></a>Handletraits:: Close

지정된 된 핸들을 닫습니다.

```cpp
inline static bool Close(
   _In_ Type h
);
```

### <a name="parameters"></a>매개 변수

*h*<br/>
핸들 닫기입니다.

### <a name="return-value"></a>반환 값

**true** 경우 처리할 *h* 이 고, 그렇지 않으면 닫은 **false**합니다.

## <a name="getinvalidvalue"></a>Handletraits:: Getinvalidvalue

잘못 된 핸들을 나타냅니다.

```cpp
inline static HANDLE GetInvalidValue();
```

### <a name="return-value"></a>반환 값

항상 INVALID_HANDLE_VALUE를 반환합니다. (INVALID_HANDLE_VALUE Windows에서 정의 됩니다.)
