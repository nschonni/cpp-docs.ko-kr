---
title: RuntimeClassBaseT 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 10/03/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::Details::RuntimeClassBaseT
- implements/Microsoft::WRL::Details::RuntimeClassBaseT::AsIID
- implements/Microsoft::WRL::Details::RuntimeClassBaseT::GetImplementedIIDS
dev_langs:
- C++
helpviewer_keywords:
- Microsoft::WRL::Details::RuntimeClassBaseT structure
- Microsoft::WRL::Details::RuntimeClassBaseT::AsIID method
- Microsoft::WRL::Details::RuntimeClassBaseT::GetImplementedIIDS method
ms.assetid: a62775fb-3359-4f45-9ff1-c07fa8da464b
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 9c46e89dc11f4c6fe216cfd61c3222a9c52d9e45
ms.sourcegitcommit: 955ef0f9d966e7c9c65e040f1e28fa83abe102a5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48789139"
---
# <a name="runtimeclassbaset-structure"></a>RuntimeClassBaseT 구조체

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

## <a name="syntax"></a>구문

```cpp
template <unsigned int RuntimeClassTypeT>
friend struct Details::RuntimeClassBaseT;
```

### <a name="parameters"></a>매개 변수

*RuntimeClassTypeT*<br/>
플래그 중 하나 이상 지정 하는 필드 [RuntimeClassType](../windows/runtimeclasstype-enumeration.md) 열거자입니다.

## <a name="remarks"></a>설명

도우미 메서드를 제공 `QueryInterface` 작업과 인터페이스 Id를 시작 합니다.

## <a name="members"></a>멤버

### <a name="protected-methods"></a>보호된 메서드

이름                                                         | 설명
------------------------------------------------------------ | -----------------------------------------------------------------------------
[Runtimeclassbaset:: Asiid](#asiid)                           | 지정 된 인터페이스 ID에 대 한 포인터를 검색합니다.
[Runtimeclassbaset:: Getimplementediids](#getimplementediids) | 지정된 된 형식에서 구현 되는 Id 인터페이스의 배열을 검색 합니다.

## <a name="inheritance-hierarchy"></a>상속 계층

`RuntimeClassBaseT`

## <a name="requirements"></a>요구 사항

**헤더:** implements.h

**Namespace:** Microsoft::WRL::Details

## <a name="asiid"></a>Runtimeclassbaset:: Asiid

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

```cpp
template<typename T>
__forceinline static HRESULT AsIID(
   _In_ T* implements,
   REFIID riid,
   _Deref_out_ void **ppvObject
);
```

### <a name="parameters"></a>매개 변수

*T*<br/>
매개 변수로 지정 된 인터페이스 ID를 구현 하는 형식을 *riid*합니다.

*구현*<br/>
템플릿 매개 변수로 지정 된 형식의 변수로 *T*합니다.

*riid*<br/>
검색할 인터페이스 ID입니다.

*ppvObject*<br/>
이 작업에 성공한 경우 포인터-에-a-인터페이스에서 지정한 매개 변수 *riid*합니다.

### <a name="return-value"></a>반환 값

성공 하면 s_ok이 고 그렇지 않으면 오류를 설명 하는 HRESULT입니다.

### <a name="remarks"></a>설명

지정 된 인터페이스 ID에 대 한 포인터를 검색합니다.

## <a name="getimplementediids"></a>Runtimeclassbaset:: Getimplementediids

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

```cpp
template<typename T>
__forceinline static HRESULT GetImplementedIIDS(
   _In_ T* implements,
   _Out_ ULONG *iidCount,
   _Deref_out_ _Deref_post_cap_(*iidCount) IID **iids
);
```

### <a name="parameters"></a>매개 변수

*T*<br/>
형식의 합니다 *구현* 매개 변수입니다.

*구현*<br/>
매개 변수에 의해 지정 된 형식에 대 한 포인터 *T*합니다.

*iidCount*<br/>
검색할 인터페이스 Id의 최대 수입니다.

*iid*<br/>
이 작업 완료, 인터페이스 형식에 의해 구현 되는 Id의 배열을 *T*합니다.

### <a name="return-value"></a>반환 값

성공 하면 s_ok이 고 그렇지 않으면 오류를 설명 하는 HRESULT입니다.

### <a name="remarks"></a>설명

지정된 된 형식에서 구현 되는 Id 인터페이스의 배열을 검색 합니다.
