---
title: 데이터 멤버 특성 (c + + COM) | Microsoft Docs
ms.custom: ''
ms.date: 10/02/2018
ms.technology:
- cpp-windows
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- attributes [C++/CLI], reference topics
- data members [C++], attributes
- data members [C++]
ms.assetid: 95b2397d-1daf-4ae4-8cd0-06956d005b13
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 5019503bed9dd0012d8aafc1ade4abd3107335ac
ms.sourcegitcommit: 955ef0f9d966e7c9c65e040f1e28fa83abe102a5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48791320"
---
# <a name="data-member-attributes"></a>데이터 멤버 특성

다음 특성을 클래스, coclass 등 또는 인터페이스에서 데이터 멤버에 적용 됩니다.

|특성|설명|
|---------------|-----------------|
|[db_accessor](db-accessor.md)|그룹 `db_column` 에 참여 하는 특성 `IAccessor`-바인딩을 기반으로 합니다.|
|[db_column](db-column.md)|행 집합에 지정된 된 열을 바인딩합니다.|
|[db_command](db-command.md)|OLE DB 명령을 만듭니다.|
|[db_param](db-param.md)|입력 또는 출력 매개 변수를 사용 하 여 지정 된 멤버 변수를 연결 하 고 변수를 구분 합니다.|
|[db_source](db-source.md)|데이터 원본에 연결을 만듭니다.|
|[db_table](db-table.md)|OLE DB 테이블을 엽니다.|
|[defaultbind](defaultbind.md)|개체를 가장 잘 나타내는 단일, 바인딩 가능한 속성을 나타냅니다.|
|[displaybind](displaybind.md)|바인딩 가능한 사용자에 게 표시 하는 속성을 나타냅니다.|
|[ID](id.md)|멤버 함수 (속성 또는 메서드를 인터페이스나 dispinterface)에 대 한 DISPID를 지정합니다.|
|[range](range-cpp.md)|인수 값은 런타임에 설정 된 필드에 허용 되는 값의 범위를 지정 합니다.|
|[rdx](rdx.md)|레지스트리 키를 만들거나 기존 레지스트리 키를 수정 합니다.|
|[readonly](readonly-cpp.md)|데이터 멤버에 대한 할당을 금지합니다.|
|[requestedit](requestedit.md)|속성을 지원함을 나타냅니다는 `OnRequestEdit` 알림.|

## <a name="see-also"></a>참고 항목

[용도별 특성](attributes-by-usage.md)