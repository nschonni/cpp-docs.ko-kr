---
title: 속성 추가(Visual C++) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-ide
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- interfaces, adding properties
- properties [C++], adding to interfaces
ms.assetid: 37bd4db7-efd3-4faa-87ad-64902ed16a36
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: bca3d282318217ad9d19c0576b933b45fcbc0b41
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46393960"
---
# <a name="adding-a-property-visual-c"></a>속성 추가(Visual C++)

[속성 추가 마법사](../ide/names-add-property-wizard.md)를 사용하여 프로젝트의 인터페이스에 메서드를 추가할 수 있습니다.

### <a name="to-add-a-property-to-your-object"></a>개체에 속성을 추가하려면

1. [클래스 뷰](/visualstudio/ide/viewing-the-structure-of-code)에서 속성을 추가할 인터페이스의 이름을 마우스 오른쪽 단추로 클릭합니다.

   > [!NOTE]
   > 프로젝트에 특성이 지정되지 않은 경우 라이브러리 노드 내에 중첩된 dispinterface에 속성을 추가할 수도 있습니다.

1. 바로 가기 메뉴에서 **추가**를 클릭한 다음, **속성 추가**를 클릭합니다.

1. [속성 추가 마법사](../ide/names-add-property-wizard.md)에서 속성을 만드는 데 필요한 정보를 제공합니다.

1. 마법사의 [IDL 특성](../ide/idl-attributes-add-property-wizard.md) 페이지에서 이 속성에 대한 IDL(인터페이스 정의 언어) 설정을 지정합니다.

1. **마침**을 클릭하여 속성을 추가합니다.

속성의 **가져오기** 및 `Put` 메서드는 속성이 정의된 인터페이스에서 클래스 뷰에 두 개의 아이콘으로 표시됩니다. 두 아이콘 중 하나를 두 번 클릭하여 .Idl 파일에서 속성 선언을 볼 수 있습니다.

- ATL 인터페이스의 경우 **Get** 및 **Put** 함수가 .cpp 파일에 추가되고, 이러한 함수에 대한 참조가 .h 파일에 추가됩니다.

- MFC dispinterface의 경우 구현 형식으로 **멤버 변수**를 선택하면, 메서드 및 변수가 구현 클래스에 추가됩니다. 구현 형식으로 **Get/Set 메서드**를 선택하면 이를 구현하는 클래스에 두 메서드가 추가됩니다.

## <a name="see-also"></a>참고 항목

[COM 인터페이스 만들기](../ide/creating-a-com-interface-visual-cpp.md)<br>
[COM 인터페이스 편집](../ide/editing-a-com-interface.md)<br>
[구성 요소 개체 모델](/windows/desktop/com/the-component-object-model)<br>
[인터페이스 포인터 및 인터페이스](/windows/desktop/com/interface-pointers-and-interfaces)