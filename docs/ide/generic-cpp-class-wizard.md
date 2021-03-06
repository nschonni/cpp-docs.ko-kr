---
title: 일반 C++ 클래스 마법사 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-ide
ms.topic: conceptual
f1_keywords:
- vc.codewiz.class.generic
dev_langs:
- C++
helpviewer_keywords:
- Generic C++ Class Wizard [C++]
ms.assetid: aa95be9e-fc1b-45db-a11d-0d32c4929077
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 7b104c0631fde3164ef4299cead47caba912874b
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46431088"
---
# <a name="generic-c-class-wizard"></a>일반 C++ 클래스 마법사

프로젝트에 일반 C++ 클래스를 추가합니다. 클래스는 ATL 또는 MFC에서 상속되지 않습니다.

- **클래스 이름**

   새 클래스의 이름을 설정합니다.

- **.h 파일**

   새 클래스의 헤더 파일 이름을 설정합니다. 기본적으로 이 이름은 **클래스 이름**에 지정한 이름을 기반으로 합니다. 헤더 파일을 선택한 위치에 저장하거나 클래스 선언을 기존 파일에 추가하려면 줄임표 단추(**...** )를 클릭합니다. 기존 파일을 지정하는 경우 **마침**을 클릭하면 마법사는 파일 내용에 클래스 선언을 추가할지 여부를 지정하라는 메시지를 표시합니다. 선언을 추가하려면 **예**를 클릭하고, 마법사로 돌아가서 다른 파일 이름을 지정하려면 **아니요**를 클릭합니다.

- **.cpp 파일**

   새 클래스의 구현 파일 이름을 설정합니다. 기본적으로 이 이름은 **클래스 이름**에 지정한 이름을 기반으로 합니다. 구현 파일을 선택한 위치에 저장하거나 클래스 정의를 기존 파일에 추가하려면 줄임표 단추(**...** )를 클릭합니다. 기존 파일을 지정하는 경우 **마침**을 클릭하면 마법사는 파일 내용에 클래스 정의를 추가할지 여부를 지정하라는 메시지를 표시합니다. 정의를 추가하려면 **예**를 클릭하고, 마법사로 돌아가서 다른 파일 이름을 지정하려면 **아니요**를 클릭합니다.

- **기본 클래스**

   새 클래스의 기본 클래스를 설정합니다.

- **Access**

   새 클래스의 기본 클래스 멤버 액세스 권한을 설정합니다. 액세스 한정자는 클래스 멤버 함수에 대한 다른 클래스의 액세스 수준을 지정하는 키워드입니다. 액세스 권한을 지정하는 방법에 대한 자세한 내용은 [멤버 액세스 제어](../cpp/member-access-control-cpp.md)를 참조하세요. 기본적으로 클래스 액세스 수준은 `public`으로 설정됩니다.

   - `public`

   - `protected`

   - `private`

   - **기본값**(액세스 한정자가 생성되지 않습니다.)

- **가상 소멸자**

   클래스 소멸자가 가상인지 여부를 지정합니다. 가상 소멸자를 사용하면 파생 클래스의 인스턴스를 삭제할 때 올바른 소멸자가 호출됩니다.

- **인라인**

   헤더 파일에서 클래스 생성자와 클래스 정의를 인라인 함수로 생성합니다.

- **관리**

   이 옵션을 선택하면 관리되는 클래스 및 헤더 파일이 추가됩니다. 이 옵션을 취소하면 원시 클래스 및 헤더 파일이 추가됩니다.

## <a name="see-also"></a>참고 항목

[일반 C++ 클래스 추가](../ide/adding-a-generic-cpp-class.md)