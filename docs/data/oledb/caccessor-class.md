---
title: CAccessor 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-data
ms.topic: reference
f1_keywords:
- ATL.CAccessor<T>
- ATL::CAccessor
- CAccessor
- ATL::CAccessor<T>
- ATL.CAccessor
dev_langs:
- C++
helpviewer_keywords:
- CAccessor class
ms.assetid: b2ba959f-a686-46f3-8837-176248aef748
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 0ac3ad9da312ba1723fd7201b804260e11a64660
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50060700"
---
# <a name="caccessor-class"></a>CAccessor 클래스

접근자 형식 중 하나를 나타냅니다.

## <a name="syntax"></a>구문

```cpp
template <class T>
class CAccessor : public CAccessorBase, public T
```

### <a name="parameters"></a>매개 변수

*T*<br/>
사용자 레코드 클래스입니다.

## <a name="remarks"></a>설명

레코드를 데이터 원본에 정적으로 바인딩할 때 사용 됩니다. 레코드는 버퍼를 포함합니다. 이 클래스는 행 집합에서 여러 접근자를 지원합니다.

구조 및 데이터베이스의 형식을 알고 있는 경우이 접근자 유형이 사용 합니다.

접근자에 메모리를 가리키는 필드를 포함 하는 경우 (같은 `BSTR` 또는 인터페이스) 되어야 하는 멤버 함수를 호출 해제 [caccessorrowset:: Freerecordmemory](../../data/oledb/caccessorrowset-freerecordmemory.md) 다음 레코드를 읽을 합니다.

## <a name="requirements"></a>요구 사항

**헤더:** atldbcli.h

## <a name="see-also"></a>참고 항목

[OLE DB 소비자 템플릿](../../data/oledb/ole-db-consumer-templates-cpp.md)<br/>
[OLE DB 소비자 템플릿 참조](../../data/oledb/ole-db-consumer-templates-reference.md)