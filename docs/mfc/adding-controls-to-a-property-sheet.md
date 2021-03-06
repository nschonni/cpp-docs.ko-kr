---
title: 속성 시트에 컨트롤 추가 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- controls [MFC], adding to property sheets
- property sheets, adding controls
ms.assetid: 24ad4c0b-c1db-4850-b9f0-34aae8d74571
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 0783571ed77d3d8dfaca69edf06330e62d8e98d0
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46398510"
---
# <a name="adding-controls-to-a-property-sheet"></a>속성 시트에 컨트롤 추가

기본적으로 속성 시트의 속성 페이지, 탭 인덱스 및 OK, Cancel 및 적용 단추 창 영역을 할당합니다. (모덜리스 속성 시트가 없습니다 확인을 취소 하 고 단추를 적용 합니다.) 속성 시트에 다른 컨트롤을 추가할 수 있습니다. 예를 들어, 현재 설정을 모양을 외부 개체에 적용 하는 경우 사용자에 게 표시할 속성을 페이지 영역의 오른쪽에 미리 보기 창에 추가할 수 있습니다.

속성 시트 대화 상자에서 컨트롤을 추가할 수 있습니다는 `OnCreate` 처리기입니다. 추가 컨트롤을 일반적으로 수용 속성 시트 대화 상자의 크기를 확장 해야 합니다. 기본 클래스를 호출한 후 **CPropertySheet::OnCreate**를 호출 [GetWindowRect](../mfc/reference/cwnd-class.md#getwindowrect) 확장 사각형의 너비를 가져오고 현재 할당 된 속성 시트 창의 높이, 차원 및 호출 [MoveWindow](../mfc/reference/cwnd-class.md#movewindow) 속성 시트 창의 크기를 변경 합니다.

## <a name="see-also"></a>참고 항목

[속성 시트](../mfc/property-sheets-mfc.md)<br/>
[CPropertyPage 클래스](../mfc/reference/cpropertypage-class.md)<br/>
[CPropertySheet 클래스](../mfc/reference/cpropertysheet-class.md)
