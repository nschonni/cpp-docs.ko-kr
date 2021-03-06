---
title: ON_UPDATE_COMMAND_UI 매크로 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
f1_keywords:
- ON_UPDATE_COMMAND_UI
dev_langs:
- C++
helpviewer_keywords:
- ON_UPDATE_COMMAND_UI macro [MFC]
- update handlers [MFC]
- command-handler macros
- updating user-interface objects [MFC]
ms.assetid: 3e72b50f-4119-4c82-81cf-6e09b132de05
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 17111e24a63d527996eadd82c804e5147ad78552
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46433467"
---
# <a name="onupdatecommandui-macro"></a>ON_UPDATE_COMMAND_UI 매크로

사용 합니다 **속성** 창 사용자 인터페이스 개체를 명령 대상 개체에 명령 업데이트 처리기에 연결 합니다. 자동으로 ON_UPDATE_COMMAND_UI 매크로에 사용자 인터페이스 개체의 ID를 연결 하 고 업데이트를 처리 하는 개체에서 처리기를 만듭니다 합니다. 참조 [함수에 메시지 매핑](../mfc/reference/mapping-messages-to-functions.md) 자세한 내용은 합니다.

예를 들어, 프로그램의 편집 메뉴에서 모두 지우기 명령을 업데이트 하려면 사용 합니다 **속성** 명령 업데이트 처리기에 대 한 함수 선언 선택한 클래스의 메시지 맵 항목을 추가 하기 위한 창을 호출 `OnUpdateEditClearAll` 클래스에서 선언 및 클래스의 구현 파일에 있는 빈 함수 템플릿. 함수 프로토타입에 다음과 같습니다.

[!code-cpp[NVC_MFCDocView#2](../mfc/codesnippet/cpp/on-update-command-ui-macro_1.h)]

모든 처리기 함수에 나와 있는 같은 합니다 **afx_msg** 키워드입니다. 모든 업데이트 처리기와 같은 해당 인수 하나에 대 한 포인터를 `CCmdUI` 개체입니다.

## <a name="see-also"></a>참고 항목

[방법: 사용자 인터페이스 개체 업데이트](../mfc/how-to-update-user-interface-objects.md)

