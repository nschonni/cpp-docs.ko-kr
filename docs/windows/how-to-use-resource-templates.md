---
title: '방법: 리소스 템플릿 (c + +)를 사용 하 여 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- language-specific template files [C++]
- resource templates
- resources [C++], creating
- rct files [C++]
- templates, resource templates
- resources [C++], templates
- .rct files [C++]
ms.assetid: bdfe7060-f98e-4859-8285-9c8570360e9d
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 677828343fa7247e64a8dfbd8faede4efbc9df24
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46393752"
---
# <a name="how-to-use-resource-templates-c"></a>방법: 리소스 템플릿 (c + +)를 사용 합니다.

리소스 템플릿은 .rct 파일로 저장한 사용자 지정 리소스입니다. 리소스 템플릿을 다른 리소스를 만들기 위한 시작 지점으로 사용할 수 있습니다. 리소스 템플릿을 사용하면 표준 컨트롤 및 기타 반복 요소와 같이 기능을 공유하는 추가 리소스 또는 리소스 그룹을 개발하는 시간을 절약할 수 있습니다. 예를 들어 여러 대화 상자에 도움말 단추와 회사 로고 아이콘을 포함할 수 있습니다. 이 작업을 빠르게 하려면 새 대화 상자 템플릿을 만들고 로고와 도움말 단추를 사용하여 템플릿을 사용자 지정합니다.

템플릿 폴더 (또는 포함 경로에 지정 된 위치)에서 변경 내용을 저장 해야 리소스 템플릿을 사용자 지정한 후 해당 리소스 형식에 새 리소스 템플릿이 표시 되도록는 [리소스추가대화상자](../windows/add-resource-dialog-box.md). 그다음에 새 리소스 템플릿을 필요할 때마다 사용할 수 있습니다.

> [!NOTE]
> 주 템플릿 디렉터리의 하위 디렉터리에 언어 관련 템플릿 파일을 배치할 수 있습니다. 예를 들어 영어 전용 템플릿 파일에 배치할 수 있습니다 \\< 리소스 템플릿 디렉터리\>\1033 합니다.

### <a name="to-create-a-template-for-resources"></a>리소스에 대한 템플릿을 만들려면

1. **솔루션 탐색기**, 프로젝트를 마우스 오른쪽 단추로 클릭 합니다.

2. 바로 가기 메뉴에서 선택 **추가**, 클릭 **새 항목 추가**합니다.

3. 에 **새 항목 추가** 대화 상자의 합니다 **템플릿:** 창 선택 **리소스 템플릿 파일 (.rct)** 합니다.

4. 이름 및 새.rct 파일의 위치를 제공 하 고 클릭 **열려**합니다.

5. 새.rct 파일이 프로젝트에 추가 되 고 나타나는 **솔루션 탐색기** 아래의 합니다 **리소스** 폴더입니다.

   이제 문서 창에서 열려는.rct 파일을 두 번 클릭 다음 리소스를 추가할 수 있습니다 (문서 창에서 파일을 마우스 오른쪽 단추로 클릭 하 고 선택 **리소스 추가** 바로 가기 메뉴에서). 그다음에 해당 리소스를 사용자 지정하고 .rct 파일을 저장할 수 있습니다.

   > [!NOTE]
   > 새 RCT 파일을 만들면 Visual Studio 검색 \Program Files\Microsoft Visual Studio 9.0\VC\VCResourceTemplates에서 \Program Files\Microsoft Visual Studio 9.0\VC\VCResourceTemplates\\*LCID* ( 1033 영어)와 같은 *또는* 곳에 [경로 포함](../windows/how-to-specify-include-directories-for-resources.md)합니다. RCT 파일을 다른 파일 폴더(예: \My Documents)에 저장하려는 경우 이 폴더를 포함 경로에 추가하면 Visual Studio에서 RCT 파일을 찾습니다.

### <a name="to-convert-an-existing-rc-file-to-an-rct-file"></a>기존 .rc 파일을 .rct 파일로 변환하려면

1. [독립 실행형 파일로.rc 파일을 열고](../windows/how-to-open-a-resource-script-file-outside-of-a-project-standalone.md)합니다.

2. 에 **파일** 메뉴에서 클릭 **저장 \< *사용자의 파일 이름*>으로**입니다.

3. 위치를 지정 하 고 클릭 **확인**합니다.

### <a name="to-create-a-new-resource-from-a-template"></a>템플릿에서 새 리소스를 만들려면

1. 에 [리소스 뷰](../windows/resource-view-window.md) 창에서.rc 파일을 마우스 오른쪽 단추로 클릭 하 고 선택 **리소스 추가** 바로 가기 메뉴에서.

2. 에 **리소스 추가** 대화 상자에서 더하기 기호를 클릭 (**+**) 옆에 있는 리소스를 리소스 노드를 확장 하 고 해당 리소스에 대 한 사용 가능한 모든 템플릿을 참조 하세요.

3. 사용할 템플릿을 두 번 클릭합니다.

4. 리소스 편집기에서 추가된 리소스를 필요에 따라 수정합니다.

   리소스 편집기에서 자동으로 고유한 리소스 ID를 제공합니다. 수정할 수는 [리소스 속성](../windows/changing-the-properties-of-a-resource.md) 필요에 따라 합니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[리소스 파일](../windows/resource-files-visual-studio.md)<br/>
[리소스 편집기](../windows/resource-editors.md)