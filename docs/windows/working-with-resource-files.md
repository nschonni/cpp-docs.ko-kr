---
title: Working with Resource Files (c + +) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- resources [C++], about resources
- resources [C++], about resource files
- resource files [C++], about resource files
ms.assetid: 2699a539-b369-4b78-80f0-df03eb7b6780
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: d72e37b8625480779620025dfd1e1eda1101b824
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46430555"
---
# <a name="working-with-resource-files"></a>리소스 파일에 대한 작업

> [!WARNING]
> 이 섹션의 내용은 C++로 작성된 Windows 데스크톱 응용 프로그램에 적용됩니다. C + +로 작성 된 유니버설 Windows 플랫폼 앱의 리소스에 대 한 자세한 내용은 [앱 리소스 정의](/windows/uwp/app-resources/)합니다.
>
> C + 리소스를 추가 하는 방법은 + CLI 프로젝트를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다.

리소스는 사용자에게 정보를 제공하는 인터페이스 요소(예: 비트맵, 아이콘, 커서), 응용 프로그램에 필요한 데이터를 포함하는 사용자 지정 리소스, 설치 API에 사용되는 버전 리소스 그리고 메뉴 및 대화 상자 리소스를 포함하는 광범위한 요소로 구성될 수 있습니다.

프로젝트에 새 리소스를 추가하고 적절한 리소스 편집기를 사용하여 이러한 리소스를 수정할 수 있습니다. 대부분의 Visual C++ 마법사에서는 프로젝트에 대해 .rc 파일을 자동으로 생성합니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리 되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대 한 내용은 참조 하세요 [데스크톱 앱에 대 한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)합니다. 전역화 및 지역화 관리 되는 앱의 리소스에 대 한 내용은 참조 하세요 [Globalizing and Localizing.NET Framework Applications](/dotnet/standard/globalization-localization/index)합니다.

## <a name="in-this-section"></a>섹션 내용

[리소스 파일](../windows/resource-files-visual-studio.md)<br/>
리소스 파일과, Windows 데스크톱 응용 프로그램에서 리소스 파일의 사용 방법을 설명합니다. 또한 리소스 파일 사용 방법을 설명하는 항목에 대한 링크도 제공합니다.

[기호: 리소스 식별자](../windows/symbols-resource-identifiers.md)<br/>
기호에 대해 설명하고, **리소스 기호** 대화 상자를 사용하여 프로젝트의 기호를 관리하는 방법에 대한 정보를 제공합니다.

[리소스 편집기](../windows/resource-editors.md)<br/>
Visual Studio에서 제공되는 리소스 편집기와 각 편집기로 수정할 수 있는 리소스의 형식에 대해 설명하며 각 편집기를 사용하는 방법에 대한 자세한 정보를 확인할 수 있는 링크를 제공합니다.

## <a name="related-sections"></a>관련 단원

[Visual C++](../visual-cpp-in-visual-studio.md)<br/>
Visual C++ 설명서에 대한 링크를 제공합니다.

[의견 보내기](/visualstudio/ide/talk-to-us)<br/>
설명서 집합을 사용하고 기술 지원에 문의하고 액세스 가능성 기능을 적용하는 방법에 대한 정보를 확인할 수 있는 링크를 제공합니다.

## <a name="see-also"></a>참고 항목

[Windows 데스크톱 응용 프로그램](../windows/windows-desktop-applications-cpp.md)<br/>
[메뉴 및 기타 리소스](https://msdn.microsoft.com/library/windows/desktop/ms632583.aspx)