---
title: 문서 템플릿 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
f1_keywords:
- vc.classes.document
dev_langs:
- C++
helpviewer_keywords:
- document templates [MFC], classes
ms.assetid: 901749e9-8048-44a0-b5e2-361554650a73
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 87984bf06d8ca178d2a21ac8ff475f828690668e
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46406063"
---
# <a name="document-template-classes"></a>문서 템플릿 클래스

문서, 뷰 및 프레임 창 개체 때 새 문서 생성을 조정 하는 문서 템플릿 개체 또는 뷰가 생성 됩니다.

[CDocTemplate](../mfc/reference/cdoctemplate-class.md)<br/>
문서 서식 파일에 대 한 기본 클래스입니다. 이 클래스를 직접 사용 하지 않습니다. 대신이 클래스에서 파생 된 다른 문서 템플릿 클래스 중 하나 사용 합니다.

[CMultiDocTemplate](../mfc/reference/cmultidoctemplate-class.md)<br/>
다중 문서 인터페이스 (MDI)의 문서에 대해 사용 되는 템플릿. MDI 응용 프로그램의 여러 문서를 한 번에 열을 가질 수 있습니다.

[CSingleDocTemplate](../mfc/reference/csingledoctemplate-class.md)<br/>
단일 문서 인터페이스 (SDI)의 문서에 대해 사용 되는 템플릿. SDI 응용 프로그램에는 한 번에 열린 문서가 두 개만 있습니다.

## <a name="related-class"></a>관련된 클래스

[CCreateContext](../mfc/reference/ccreatecontext-structure.md)<br/>
구조를 문서 템플릿에 문서, 뷰 및 프레임 창 개체의 생성을 조정 하 창 생성 함수에 전달 합니다.

## <a name="see-also"></a>참고 항목

[클래스 개요](../mfc/class-library-overview.md)

