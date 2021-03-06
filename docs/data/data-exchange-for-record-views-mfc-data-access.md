---
title: 레코드 뷰 (MFC Data Access)에 대 한 데이터 교환 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-data
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- RFX (record field exchange), data exchange mechanism
- RFX (record field exchange), record views
- record views, data exchange
- DDX (dialog data exchange), record views
- RFX (record field exchange)
ms.assetid: abc52ca7-6997-47a7-98f3-f347f52b1f72
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 6b6b0109baaf17f804a0ea15eff2e9e766196b86
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50052815"
---
# <a name="data-exchange-for-record-views---mfc-data-access"></a>레코드 뷰의 데이터 교환   (MFC Data Access)

사용 하는 경우 [클래스 추가](../mfc/reference/adding-an-mfc-odbc-consumer.md) 레코드 뷰 대화 상자 템플릿 리소스에서 컨트롤을 레코드 집합의 필드에 매핑할 프레임 워크는 양방향 데이터 교환을 관리-컨트롤에 대 한 레코드 집합에서 레코드 집합에는 컨트롤입니다. DDX 메커니즘을 사용하면 데이터를 전송하는 코드를 직접 작성할 필요가 없습니다.

와 함께에서 작동 하는 레코드 뷰의 DDX [RFX](../data/odbc/record-field-exchange-rfx.md) 클래스의 레코드 집합 용 `CRecordset` (ODBC).  RFX는 데이터 소스의 현재 레코드 및 레코드 집합 개체의 필드 데이터 멤버 간에 데이터를 이동합니다. DDX는 필드 데이터 멤버에서 폼의 컨트롤로 데이터를 이동합니다. 이 조합은 먼저 폼 컨트롤을 채운 다음 사용자가 레코드 간을 이동할 때 계속해서 컨트롤을 채웁니다. 또한 업데이트된 데이터를 레코드 집합으로 다시 이동했다가 데이터 소스로 이동할 수도 있습니다.

다음 그림 레코드 뷰에 대 한 DDX와 RFX 간의 관계를 보여 줍니다.

![대화&#45;데이터 교환 및 레코드&#45;exchange 필드](../data/media/vc37xt1.gif "vc37xt1")<br/>
DDE(Dialog Data Exchange) 및 레코드 필드 교환

DDX에 대한 자세한 내용은 [대화 상자 데이터 교환 및 유효성 검사](../mfc/dialog-data-exchange-and-validation.md)를 참조하세요. RFX에 대 한 자세한 내용은 참조 하세요. [Exchange RFX (레코드 필드)](../data/odbc/record-field-exchange-rfx.md)합니다.

## <a name="see-also"></a>참고 항목

[레코드 뷰(MFC Data Access)](../data/record-views-mfc-data-access.md)<br/>
[ODBC 드라이버 목록](../data/odbc/odbc-driver-list.md)