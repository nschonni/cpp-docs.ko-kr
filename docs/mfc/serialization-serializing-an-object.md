---
title: 'Serialization: 개체 직렬화 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- serializing objects [MFC]
- serialization [MFC], objects
- objects [MFC], serializing
ms.assetid: 1db772b1-ad55-4fcf-b133-126cca082510
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: e05cce1132b180ac8f1350b68d951d776a62315f
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46381090"
---
# <a name="serialization-serializing-an-object"></a>Serialization: 개체 Serialize

이 문서 [Serialization: Serializable 클래스 만들기](../mfc/serialization-making-a-serializable-class.md) serializable 클래스를 만드는 방법을 보여 줍니다. Serializable 클래스를 만든 후 serialize 할 수 있습니다를 통해 파일에서 해당 클래스의 개체를 [CArchive](../mfc/reference/carchive-class.md) 개체입니다. 이 문서는 다음 사항을 설명합니다.

- [CArchive 개체의 정의](../mfc/what-is-a-carchive-object.md)합니다.

- [CArchive를 만드는 두 가지 방법을](../mfc/two-ways-to-create-a-carchive-object.md)합니다.

- [CArchive를 사용 하는 방법 <\< 고 >> 연산자](../mfc/using-the-carchive-output-and-input-operators.md)합니다.

- [Cobject 저장 및 로드 보관을 통해](../mfc/storing-and-loading-cobjects-via-an-archive.md)합니다.

프레임워크를 통해 Serializable 문서에 대한 보관 저장소를 만들거나 명시적으로 `CArchive` 개체를 직접 만들 수 있습니다. 사용 하 여 파일과 serializable 개체 간에 데이터를 전송할 수 있습니다는 <\< 및 >> 연산자에 대 한 `CArchive` 또는 호출 하 여 일부 경우에는 `Serialize` 함수를 `CObject`-파생 클래스.

## <a name="see-also"></a>참고 항목

[serialization](../mfc/serialization-in-mfc.md)

