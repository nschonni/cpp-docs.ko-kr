---
title: CCmdUI 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
f1_keywords:
- CCmdUI
dev_langs:
- C++
helpviewer_keywords:
- updating user interface objects [MFC]
- user interface objects [MFC], updating
- CCmdUI class [MFC], menu updating
- update handlers [MFC]
- toolbars [MFC], updating
ms.assetid: 2f2bae62-8c29-45a4-bbce-490eb01907d5
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 18b5675aff2d10f224238a1ba6d3b919e1b285a7
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46374584"
---
# <a name="the-ccmdui-class"></a>CCmdUI 클래스

프레임 워크를 update 명령을 해당 처리기를 라우팅하는 경우 처리기에 대 한 포인터를 전달를 `CCmdUI` 개체 (또는 개체에 `CCmdUI`-파생 클래스). 이 개체는 메뉴 항목이 나 도구 모음 단추 또는 명령을 생성 하는 다른 사용자 인터페이스 개체를 나타냅니다. 업데이트 처리기 멤버 함수를 호출 합니다 `CCmdUI` 사용자 인터페이스 개체 업데이트에 대 한 포인터를 통해 구조입니다. 예를 들어 다음과 같습니다. 모두 지우기 메뉴 항목에 대 한 업데이트 처리기

[!code-cpp[NVC_MFCDocView#3](../mfc/codesnippet/cpp/the-ccmdui-class_1.cpp)]

이 처리기를 호출 합니다 `Enable` 메뉴 항목에 대 한 액세스를 사용 하 여 개체의 멤버 함수입니다. `Enable` 사용 가능한 항목을 만듭니다.

## <a name="see-also"></a>참고 항목

[방법: 사용자 인터페이스 개체 업데이트](../mfc/how-to-update-user-interface-objects.md)

