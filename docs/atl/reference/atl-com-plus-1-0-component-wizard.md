---
title: "ATL COM + 1.0 구성 요소 마법사 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- vc.codewiz.class.atl.mts.overview
dev_langs:
- C++
helpviewer_keywords:
- ATL projects, adding components
- ATL COM+ 1.0 Component Wizard
ms.assetid: 11670681-8671-4122-96a4-2e52f8dadce0
caps.latest.revision: 13
author: mikeblome
ms.author: mblome
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
translationtype: Machine Translation
ms.sourcegitcommit: 3168772cbb7e8127523bc2fc2da5cc9b4f59beb8
ms.openlocfilehash: 2729975c5e823965f4f5c16d5bfe317ce10a3670
ms.lasthandoff: 02/24/2017

---
# <a name="atl-com-10-component-wizard"></a>ATL COM+ 1.0 구성 요소 마법사
개체는 트랜잭션을 포함 하 여 COM + 1.0 서비스를 지 원하는 프로젝트에 추가 하려면이 마법사를 사용 합니다.  
  
 이중 인터페이스와 자동화 개체를 지원 하는지 여부를 지정할 수 있습니다. 오류 정보 인터페이스, 향상 된 개체 컨트롤, 트랜잭션 및 비동기 메시지 큐에 대 한 지원을 나타낼 수도 있습니다.  
  
## <a name="remarks"></a>주의  
 부터는 [!INCLUDE[vs_orcas_long](../../atl/reference/includes/vs_orcas_long_md.md)],이 마법사에서 생성 된 등록 스크립트에서 해당 COM 구성 요소를 등록 합니다 **HKEY_CURRENT_USER** 대신 **HKEY_LOCAL_MACHINE**합니다. 이 동작을 수정 하려면 설정의 **모든 사용자에 대 한 구성 요소 등록** ATL 마법사의 옵션입니다.  
  
## <a name="names"></a>이름  
 개체, 인터페이스 및 프로젝트에 추가할 클래스에 대 한 이름을 지정 합니다. 제외 **약식 이름**, 다른 모든 상자의 개별적으로 편집할 수 있습니다. 에 대 한 텍스트를 변경 하는 경우 **약식 이름**,이 페이지에 있는 다른 모든 상자의 이름에는 변경 내용이 반영 됩니다. 변경 하는 경우는 **Coclass** 변경 COM 섹션에는 이름에 반영 됩니다는 **형식** 및 **ProgID** 상자 하지만 **인터페이스** 이름은 변경 되지 않습니다. 이 명명 문제는 모든 이름을 쉽게 식별할 수 있도록 사용자에 대 한 컨트롤을 개발할 때 설계 되었습니다.  
  
 **짧은 이름**  
 개체에 대 한 약식된 이름을 설정합니다. 결정을 제공 하는 이름을 `Class` 및 `Coclass` 이름는 **.cpp 파일** 및 **.h 파일** 이름는 **인터페이스** 이름는 **형식** 이름 및 **ProgID**해당 필드를 개별적으로 변경 하지 않는 한 합니다.  
  
 **.h 파일**  
 새 개체의 클래스에 대 한 헤더 파일의 이름을 설정합니다. 기본적으로이 이름은에서 제공 하는 이름에 따라 **약식 이름**합니다. 사용자가 선택한 위치에 파일 이름을 저장 하거나 기존 파일을 클래스 선언 추가 하려면 줄임표 단추를 클릭 합니다. 기존 파일을 선택 하면 마법사 파일이 저장 되지 것입니다 선택한 위치에 때까지 클릭 **마침** 마법사에서.  
  
 마법사 파일을 덮어쓰지 않습니다. 선택한 경우 기존 파일의 이름을 클릭 하면 **마침**, 클래스 선언에는 파일의 내용을 추가할 것인지 묻는 합니다. 클릭 **예** ; 파일을 추가 클릭 **No** 마법사 돌아가서 다른 파일 이름을 지정 하려면.  
  
 **클래스**  
 만들 클래스의 이름을 설정 합니다. 이 이름은 기반에서 제공한 이름으로 **약식 이름**, 클래스 이름에 대 한 일반적인 접두사 'c' 앞에 옵니다.  
  
 **.cpp 파일**  
 새 개체의 클래스에 대 한 구현 파일의 이름을 설정합니다. 기본적으로이 이름은에서 제공 하는 이름에 따라 **약식 이름**합니다. 원하는 위치에 파일 이름을 저장 하려면 줄임표 단추를 클릭 합니다. 클릭할 때까지 파일이 선택한 위치에 저장 되지는 않습니다 **마침** 마법사에서.  
  
 마법사 파일을 덮어쓰지 않습니다. 선택한 경우 기존 파일의 이름을 클릭 하면 **완료**, 마법사에서 클래스에 구현 파일의 내용에 추가할 것인지 여부를 묻는 메시지를 표시 합니다. 클릭 **예** ; 파일을 추가 클릭 **No** 마법사 돌아가서 다른 파일 이름을 지정 하려면.  
  
 **특성 사용**  
 개체가 특성을 사용 하는지 여부를 나타냅니다. ATL 프로젝트 특성 사용된 하는 개체를 추가 하는 경우에이 옵션이 선택 되며 변경할 수 없습니다. 즉, 특성이 지정 된 개체만 특성 지원을 사용 하 여 만든 프로젝트에 추가할 수 있습니다.  
  
 특성을 지원 하지 않은 ATL 프로젝트에 대해이 옵션을 선택 하면 마법사는 특성의 지원 프로젝트에 추가할 것인지 여부를 지정 하 라는 메시지가 표시 됩니다.  
  
 이 옵션을 설정한 후를 추가 하는 모든 개체는 (확인란 선택) 기본적으로 특성을 사용 하는 것으로 지정 됩니다. 특성을 사용 하지 않는 개체를 추가 하려면이 상자를 지울 수 있습니다.  
  
 참조 [ATL 프로젝트 마법사, 응용 프로그램 설정](../../atl/reference/application-settings-atl-project-wizard.md) 및 [특성의 기본 메커니즘](../../windows/basic-mechanics-of-attributes.md) 에 대 한 자세한 내용은 합니다.  
  
### <a name="com"></a>COM  
 개체에 대 한 COM 기능에 대 한 정보를 제공합니다.  
  
 **Coclass**  
 개체에 의해 지원 되는 인터페이스의 목록을 포함 하는 구성 요소 클래스의 이름을 설정 합니다.  
  
> [!NOTE]
>  특성을 사용 하 여 프로젝트를 만들면 또는 ATL 포함 되어 있지 않으므로이 옵션을 변경할 수 없습니다을 지정할 경우이 마법사 페이지에서 COM + 1.0 구성 요소 특성을 사용 하는 경우는 `coclass` 특성입니다.  
  
 **Type**  
 레지스트리에 나타나는 개체 설명 설정  
  
 **인터페이스**  
 개체의 만들 인터페이스를 설정 합니다. 이 인터페이스는 사용자 지정 메서드를 포함합니다.  
  
 **ProgID**  
 컨테이너 개체의 CLSID 대신 사용할 수 있는 이름을 설정 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [ATL COM + 1.0 구성 요소](../../atl/reference/adding-an-atl-com-plus-1-0-component.md)

