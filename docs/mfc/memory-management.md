---
title: 메모리 관리 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- memory [MFC]
- MFC, memory management
- memory allocation [MFC]
- memory [MFC], managing
- memory allocation [MFC], MFC
ms.assetid: 934ac81b-d630-4232-88e5-ea74f7187987
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: e4e83342dde85aae626c9fb83a9493f3e3dd668b
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46383999"
---
# <a name="memory-management"></a>메모리 관리

문서의이 그룹의 Microsoft Foundation 클래스 라이브러리 (MFC) 메모리 관리와 관련 된 일반적인 서비스를 활용 하는 방법을 설명 합니다. 메모리 할당 두 범주로 나눌 수 있습니다: 프레임 할당 및 힙 할당 합니다.

두 할당 기술 간의 주요 차이점 중 하나는 일반적으로 실제 메모리를 사용 하 여 작업할 프레임 할당을 사용 하 여 블록 자체를 힙 할당을 사용 하 여 항상 제공 됩니다에 대 한 포인터는 메모리 블록에 있지만 됩니다. 두 스키마의 또 다른 주요 차이점은 된 프레임 개체는 자동으로 삭제, 프로그래머가 힙 개체를 명시적으로 삭제 해야 하는 동안.

Windows의 프로그램에서 메모리 관리에 대 한 비 MFC 정보를 참조 하세요 [메모리 관리](https://msdn.microsoft.com/library/windows/desktop/aa366779) Windows SDK에 있습니다.

## <a name="what-do-you-want-to-know-more-about"></a>자세히 알아보려는 항목

- [프레임 할당](../mfc/memory-management-frame-allocation.md)

- [힙 할당](../mfc/memory-management-heap-allocation.md)

- [배열에 대 한 메모리를 할당합니다.](../mfc/memory-management-examples.md)

- [힙에서 배열에 대 한 메모리를 할당 해제](../mfc/memory-management-examples.md)

- [데이터 구조에 대 한 메모리를 할당합니다.](../mfc/memory-management-examples.md)

- [개체에 대 한 메모리를 할당합니다.](../mfc/memory-management-examples.md)

- [크기 조정 가능한 메모리 블록](../mfc/memory-management-resizable-memory-blocks.md)

## <a name="see-also"></a>참고 항목

[개념](../mfc/mfc-concepts.md)<br/>
[일반 MFC 항목](../mfc/general-mfc-topics.md)

