---
title: --생성자 주석 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- constructors comment
- declarations, constructors
- MFC source files, Constructors comment
- declaring constructors, code comments
- comments, MFC
- comments, constructors comment
- constructors [MFC], declaring
- instance constructors, code comments
ms.assetid: f400774e-ba85-49ed-85b7-70ef2f7dcb2b
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: f03a65c3f870b1e7648f03b70efe7242c35a21f9
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46429359"
---
# <a name="-constructors-comment"></a>// 생성자 주석

`// Constructors` MFC 클래스 선언의 섹션 생성자 (c + + 점에서) 뿐만 아니라 실제로 개체를 사용 하는 데 필요한 초기화 함수를 선언 합니다. 예를 들어 `CWnd::Create` 이므로 생성자 섹션을 사용 하기 전에 `CWnd` 이 생성 해야 합니다"완전히" 먼저 c + + 생성자를 호출 하 고 다음 호출 하 여 개체를 `Create` 함수입니다. 일반적으로 이러한 멤버는 public입니다.

예를 들어, 클래스 `CStdioFile` 아래 목록에 표시 된 것 중 하나는 세 가지 생성자가 [주석의 예제](../mfc/an-example-of-the-comments.md)합니다.

## <a name="see-also"></a>참고 항목

[MFC 소스 파일 사용](../mfc/using-the-mfc-source-files.md)<br/>
[구현 주석](../mfc/decrement-implementation-comment.md)<br/>
[특성 주석](../mfc/decrement-attributes-comment.md)<br/>
[작업 주석](../mfc/decrement-operations-comment.md)<br/>
[재정의 가능 주석](../mfc/decrement-overridables-comment.md)

