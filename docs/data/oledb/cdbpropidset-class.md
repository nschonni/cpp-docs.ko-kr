---
title: CDBPropIDSet 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-data
ms.topic: reference
f1_keywords:
- CDBPropIDSet
- ATL.CDBPropIDSet
- ATL::CDBPropIDSet
- CDBPropIDSet.AddPropertyID
- CDBPropIDSet::AddPropertyID
- AddPropertyID
- ATL.CDBPropIDSet.AddPropertyID
- ATL::CDBPropIDSet::AddPropertyID
- ATL::CDBPropIDSet::CDBPropIDSet
- CDBPropIDSet
- CDBPropIDSet.CDBPropIDSet
- CDBPropIDSet::CDBPropIDSet
- ATL.CDBPropIDSet.CDBPropIDSet
- CDBPropIDSet.operator=
- ATL.CDBPropIDSet.operator=
- ATL::CDBPropIDSet::operator=
- CDBPropIDSet::operator=
- CDBPropIDSet.SetGUID
- ATL::CDBPropIDSet::SetGUID
- SetGUID
- ATL.CDBPropIDSet.SetGUID
- CDBPropIDSet::SetGUID
dev_langs:
- C++
helpviewer_keywords:
- CDBPropIDSet class
- AddPropertyID method
- CDBPropIDSet class, constructor
- operator =, property sets
- = operator, with OLE DB templates
- operator=, property sets
- SetGUID method
ms.assetid: 52bb806c-9581-494d-9af7-50d8a4834805
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 6ab6e58ad6f25232be5c298673cefe6d0488f63b
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50083102"
---
# <a name="cdbpropidset-class"></a>CDBPropIDSet 클래스

상속 되는 `DBPROPIDSET` 구조체 및 키 필드를 초기화 하는 생성자를 추가 뿐만 [AddPropertyID](../../data/oledb/cdbpropidset-addpropertyid.md) 메서드에 액세스 합니다.

## <a name="syntax"></a>구문

```cpp
class CDBPropIDSet : public tagDBPROPIDSET
```

## <a name="requirements"></a>요구 사항

**헤더:** atldbcli.h

## <a name="members"></a>멤버

### <a name="methods"></a>메서드

|||
|-|-|
|[AddPropertyID](#addpropertyid)|속성 ID 집합에는 속성을 추가합니다.|
|[CDBPropIDSet](#cdbpropidset)|생성자입니다.|
|[SetGUID](#setguid)|집합 속성 ID의 GUID를 설정 합니다.|

### <a name="operators"></a>연산자

|||
|-|-|
|[operator =](#op_equal)|할당 한 속성 ID의 내용을 다른로 설정 합니다.|

## <a name="remarks"></a>설명

OLE DB 소비자가 사용 하 여 `DBPROPIDSET` 는 소비자가 속성 정보를 가져올 속성 Id의 배열을 전달 하는 구조입니다. 단일에서 식별 된 속성을 [DBPROPIDSET](/previous-versions/windows/desktop/ms717981) 구조 하나의 속성 집합에 속합니다.

## <a name="addpropertyid"></a> Cdbpropidset:: Addpropertyid

속성 ID 집합에 속성 ID를 추가합니다.

### <a name="syntax"></a>구문

```cpp
bool AddPropertyID(DBPROPID propid) throw();
```

#### <a name="parameters"></a>매개 변수

*propid*<br/>
[in] 속성 ID에 추가할 속성 ID를 설정 합니다.

## <a name="cdbpropidset"></a> Cdbpropidset:: Cdbpropidset

생성자입니다. 초기화 합니다 `rgProperties`, `cProperties`, 및 (선택 사항) `guidPropertySet` 의 필드를 [DBPROPIDSET](/previous-versions/windows/desktop/ms717981) 구조입니다.

### <a name="syntax"></a>구문

```cpp
CDBPropIDSet(const GUID& guid);

CDBPropIDSet(const CDBPropIDSet& propidset);

CDBPropIDSet();
```

#### <a name="parameters"></a>매개 변수

*guid*<br/>
[in] GUID를 초기화 하는 데는 `guidPropertySet` 필드입니다.

*propidset*<br/>
[in] 복사 생성을 위한 다른 `CDBPropIDSet` 개체입니다.

## <a name="setguid"></a> Cdbpropidset:: Setguid

GUID 필드 설정 된 `DBPROPIDSET` 구조입니다.

### <a name="syntax"></a>구문

```cpp
void SetGUID(const GUID& guid) throw();
```

#### <a name="parameters"></a>매개 변수

*guid*<br/>
[in] 설정 하는 데 GUID를 `guidPropertySet` 필드를 [DBPROPIDSET](/previous-versions/windows/desktop/ms717981) 구조입니다.

### <a name="remarks"></a>설명

이 필드에서 설정할 수는 [생성자](../../data/oledb/cdbpropidset-cdbpropidset.md) 도 합니다. 이 클래스에 대 한 기본 생성자를 사용 하는 경우이 함수를 호출 합니다.

## <a name="op_equal"></a> Cdbpropidset:: Operator =

다른 ID 속성 집합으로 설정 된 하나의 속성 ID의 콘텐츠를 할당 합니다.

### <a name="syntax"></a>구문

```cpp
CDBPropIDSet& operator =(CDBPropIDSet& propset) throw();
```

## <a name="see-also"></a>참고 항목

[OLE DB 소비자 템플릿](../../data/oledb/ole-db-consumer-templates-cpp.md)<br/>
[OLE DB 소비자 템플릿 참조](../../data/oledb/ole-db-consumer-templates-reference.md)