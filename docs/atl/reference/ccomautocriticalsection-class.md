---
title: CComAutoCriticalSection 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-atl
ms.topic: reference
f1_keywords:
- CComAutoCriticalSection
- ATLCORE/ATL::CComAutoCriticalSection
- ATLCORE/ATL::CComAutoCriticalSection::CComAutoCriticalSection
dev_langs:
- C++
helpviewer_keywords:
- CComAutoCriticalSection class
ms.assetid: 491a9d90-3398-4f90-88f5-fd2172a46b30
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 40fa13ecf743bf8e6aa0cd75b16bec65131fe267
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50061081"
---
# <a name="ccomautocriticalsection-class"></a>CComAutoCriticalSection 클래스

`CComAutoCriticalSection` 가져오기 및 해제는 임계 영역 개체의 소유권에 대 한 메서드를 제공 합니다.

## <a name="syntax"></a>구문

```
class CComAutoCriticalSection : public CComCriticalSection
```

## <a name="members"></a>멤버

### <a name="public-constructors"></a>Public 생성자

|이름|설명|
|----------|-----------------|
|[CComAutoCriticalSection::CComAutoCriticalSection](#ccomautocriticalsection)|생성자입니다.|
|[CComAutoCriticalSection:: ~ CComAutoCriticalSection](#dtor)|소멸자입니다.|

## <a name="remarks"></a>설명

`CComAutoCriticalSection` 클래스와 유사한 [CComCriticalSection](../../atl/reference/ccomcriticalsection-class.md)를 제외 하 고 `CComAutoCriticalSection` 자동으로 생성자에 임계 영역 개체를 초기화 합니다.

일반적으로 사용 `CComAutoCriticalSection` 를 통해 합니다 `typedef` 이름 [AutoCriticalSection](ccommultithreadmodel-class.md#autocriticalsection)합니다. 이 이름을 참조 `CComAutoCriticalSection` 때 [CComMultiThreadModel](../../atl/reference/ccommultithreadmodel-class.md) 사용 되 고 있습니다.

합니다 `Init` 하 고 `Term` 메서드에서 [CComCriticalSection](../../atl/reference/ccomcriticalsection-class.md) 이 클래스를 사용 하는 경우에 사용할 수 없습니다.

## <a name="inheritance-hierarchy"></a>상속 계층

[CComCriticalSection](../../atl/reference/ccomcriticalsection-class.md)

`CComAutoCriticalSection`

## <a name="requirements"></a>요구 사항

**헤더:** atlcore.h

##  <a name="ccomautocriticalsection"></a>  CComAutoCriticalSection::CComAutoCriticalSection

생성자입니다.

```
CComAutoCriticalSection();
```

### <a name="remarks"></a>설명

Win32 함수 호출 [InitializeCriticalSection](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection)는 임계 영역 개체를 초기화 합니다.

##  <a name="dtor"></a>  CComAutoCriticalSection:: ~ CComAutoCriticalSection

소멸자입니다.

```
~CComAutoCriticalSection() throw();
```

### <a name="remarks"></a>설명

소멸자 호출 [DeleteCriticalSection](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection), 임계 영역 개체에서 사용 하는 모든 시스템 리소스를 해제 합니다.

## <a name="see-also"></a>참고 항목

[CComFakeCriticalSection 클래스](../../atl/reference/ccomfakecriticalsection-class.md)<br/>
[클래스 개요](../../atl/atl-class-overview.md)<br/>
[CComCriticalSection 클래스](../../atl/reference/ccomcriticalsection-class.md)
