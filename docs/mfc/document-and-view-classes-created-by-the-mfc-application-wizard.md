---
title: MFC 응용 프로그램 마법사에서 생성 된 클래스를 살펴보고 문서 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- document classes [MFC]
- document classes [MFC], created by application wizards
- application wizards [MFC], document/view classes created
- view classes [MFC], created by application wizards
ms.assetid: 70c34a60-2701-4981-acea-c08a5787d8e6
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: eb1a1fc6c35bfb9589e827d798cb112640fa9b2f
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46417620"
---
# <a name="document-and-view-classes-created-by-the-mfc-application-wizard"></a>MFC 응용 프로그램 마법사에서 만든 문서 및 뷰 클래스

MFC 응용 프로그램 마법사를 사용 하면 시작할 프로그램 개발의 기본 문서 및 뷰 클래스를 만들어 합니다. 할 수 있습니다 [명령 및 메시지를 이러한 클래스에 매핑하고](../mfc/reference/mapping-messages-to-functions.md) Visual c + + 소스 코드 편집기를 사용 하 여 해당 멤버 함수를 작성 합니다.

클래스에서 파생 된 MFC 응용 프로그램 마법사에서 만든 문서 클래스 [CDocument](../mfc/reference/cdocument-class.md)합니다. 뷰 클래스에서 파생 됩니다 [CView](../mfc/reference/cview-class.md)합니다. 이러한 클래스를 제공 하는 응용 프로그램 마법사를 포함 하는 파일 프로젝트 이름에 기반한 이름을 응용 프로그램 마법사 대화 상자에서 제공 합니다. 응용 프로그램 마법사에서 기본 이름을 변경 하려면 생성 된 클래스 페이지를 사용할 수 있습니다.

둘 이상의 문서 클래스, 클래스 보기 또는 frame-window 클래스 일부 응용 프로그램은 필요할 수 있습니다. 자세한 내용은 [여러 문서 형식, 뷰 및 프레임 Windows](../mfc/multiple-document-types-views-and-frame-windows.md)합니다.

## <a name="see-also"></a>참고 항목

[문서/뷰 아키텍처](../mfc/document-view-architecture.md)

