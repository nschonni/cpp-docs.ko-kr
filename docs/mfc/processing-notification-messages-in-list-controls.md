---
title: 목록 컨트롤에서 알림 메시지 처리 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- processing notifications [MFC]
- CListCtrl class [MFC], processing notifications
ms.assetid: 1f0e296e-d2a3-48fc-ae38-51d7fb096f51
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 4ab312a1ef64ce64ba39b43df722f9aaafa6dcb4
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46410743"
---
# <a name="processing-notification-messages-in-list-controls"></a>목록 컨트롤에서 알림 메시지 처리

사용자가 열 머리글을 클릭 아이콘을 끌어, 레이블 및 등과 목록 컨트롤 편집 ([CListCtrl](../mfc/reference/clistctrl-class.md)) 해당 부모 창에 알림 메시지를 보냅니다. 이에 대한 응답으로 작업을 수행하려는 경우 이러한 메시지를 처리합니다. 예를 들어 사용자가 열 머리글을 클릭 하면 Microsoft Outlook 처럼 클릭 한 열의 내용에 따라 항목을 정렬 하는 것이 좋습니다.

뷰 또는 대화 상자 클래스에서 목록 컨트롤에서 WM_NOTIFY 메시지를 처리 합니다. 속성 창을 사용 하 여 만들기는 [OnChildNotify](../mfc/reference/cwnd-class.md#onchildnotify) switch 문 사용 하 여 처리기 함수는 알림 메시지를 처리 하는 기반입니다.

목록 컨트롤을 해당 부모 창에 보낼 수 알림의 목록을 참조 하세요 [목록 뷰 컨트롤 참조](/windows/desktop/Controls/list-view-control-reference) Windows SDK에 있습니다.

## <a name="see-also"></a>참고 항목

[CListCtrl 사용](../mfc/using-clistctrl.md)<br/>
[컨트롤](../mfc/controls-mfc.md)

