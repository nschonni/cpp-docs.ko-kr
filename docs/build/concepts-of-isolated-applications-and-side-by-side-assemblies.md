---
title: 격리 된 응용 프로그램 및 side-by-side-어셈블리의 개념 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- side-by-side assemblies [C++]
- isolated assemblies [C++]
ms.assetid: 945a885f-cb3e-4c8a-a0b9-2c2e3e02cc50
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 27ecefc5e448a1040e7eff3e45b94b0a31fbfc87
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45710258"
---
# <a name="concepts-of-isolated-applications-and-side-by-side-assemblies"></a>격리된 응용 프로그램 및 side-by-side 어셈블리 개념

응용 프로그램으로 간주 됩니다는 [격리 된 응용 프로그램](/windows/desktop/SbsCs/isolated-applications) 의 해당 구성 요소 모두 [side-by-side-어셈블리](/windows/desktop/SbsCs/about-side-by-side-assemblies-)합니다. side-by-side 어셈블리는 DLL 그룹, Windows 클래스, COM 서버, 형식 라이브러리 또는 인터페이스 같이 함께 배포되고 런타임에 실행할 응용 프로그램에 사용할 수 있는 리소스의 컬렉션입니다. 일반적으로 side-by-side 어셈블리는 여러 DLL 중 하나입니다.

## <a name="shared-or-private"></a>공유 또는 전용

side-by-side 어셈블리는 공유 또는 전용으로 설정할 수 있습니다. [공유 side-by-side-어셈블리](https://msdn.microsoft.com/library/aa375996.aspx) 는 매니페스트에서 어셈블리에 대 한 종속성을 지정 하는 여러 응용 프로그램에서 사용할 수 있습니다. 여러 버전의 side-by-side 어셈블리를 동시에 실행되는 서로 다른 응용 프로그램에서 공유할 수 있습니다. A [전용 어셈블리](/windows/desktop/SbsCs/about-private-assemblies-) 은 해당 응용 프로그램 에서만 단독으로 사용는 응용 프로그램과 함께 배포 되는 어셈블리입니다. 전용 어셈블리는 응용 프로그램의 실행 파일이 포함된 폴더나 하위 폴더 중 하나에 설치됩니다.

## <a name="manifests-and-search-order"></a>매니페스트 및 검색 순서

격리 된 응용 프로그램과 side-by-side-어셈블리에서 설명한 [매니페스트](https://msdn.microsoft.com/library/aa375365)합니다. 매니페스트는 응용 프로그램이나 어셈블리에 리소스로 포함되거나 외부 파일로 제공되는 XML 문서입니다. 격리된 응용 프로그램의 매니페스트 파일은 런타임에 응용 프로그램을 바인딩해야 하는 공유 side-by-side 어셈블리의 이름과 버전을 관리하는 데 사용됩니다. side-by-side 어셈블리의 매니페스트는 side-by-side 어셈블리의 종속 어셈블리, 이름, 버전 및 리소스를 지정합니다. 공유 side-by-side 어셈블리의 경우 매니페스트는 %WINDIR%\WinSxS\Manifests\ 폴더에 설치됩니다. 전용 어셈블리의 경우 매니페스트를 DLL에 ID가 1인 리소스로 포함하는 것이 좋습니다. 전용 어셈블리의 이름을 DLL과 같은 이름으로 지정할 수도 있습니다. 자세한 내용은 [전용 어셈블리에 대 한](/windows/desktop/SbsCs/about-private-assemblies-)합니다.

프로그램을 실행할 때 Windows에서는 응용 프로그램의 매니페스트에 있는 어셈블리 정보를 사용하여 필요한 side-by-side 어셈블리를 검색하고 로드합니다. 격리된 응용 프로그램에서 어셈블리 종속성을 지정하는 경우 운영 체제는 먼저 %WINDIR%\WinSxS\ 폴더에 있는 네이티브 어셈블리 캐시의 공유 어셈블리 중에서 필요한 어셈블리를 검색합니다. 필요한 어셈블리를 찾지 못하면 운영 체제는 응용 프로그램의 디렉터리 구조에서 관련 폴더의 전용 어셈블리를 검색합니다. 자세한 내용은 [어셈블리 검색 시퀀스](/windows/desktop/SbsCs/assembly-searching-sequence)합니다.

## <a name="changing-dependencies"></a>종속성 변경

응용 프로그램을 수정 하 여 배포 된 후에 side-by-side-어셈블리 종속성을 변경할 수 있습니다 합니다 [게시자 구성 파일](/windows/desktop/SbsCs/publisher-configuration-files) 하 고 [응용 프로그램 구성 파일](/windows/desktop/SbsCs/application-configuration-files)합니다. 게시자 정책 파일이라고도 하는 게시자 구성 파일은 side-by-side 어셈블리의 버전 사용에서 동일한 어셈블리의 다른 버전 사용으로 응용 프로그램과 어셈블리를 전체 리디렉션하는 XML 파일입니다. 예를 들어 side-by-side 어셈블리에 대해 버그 수정 또는 보안 수정이 배포되고 수정된 버전을 사용하기 위해 모든 응용 프로그램을 리디렉션하려고할 때 종속성을 변경할 수 있습니다. 응용 프로그램 구성 파일은 side-by-side 어셈블리의 버전 사용에서 동일한 어셈블리의 다른 버전 사용으로 특정 응용 프로그램을 리디렉션하는 XML 파일입니다. 응용 프로그램 구성 파일을 사용하여 게시자 구성 파일에 정의된 것과는 다른 side-by-side 어셈블리의 버전을 사용할 특정 응용 프로그램을 리디렉션할 수 있습니다. 자세한 내용은 [구성](/windows/desktop/SbsCs/configuration)을 참고하시기 바랍니다.

## <a name="visual-c-libraries"></a>Visual C++ 라이브러리

Visual Studio 2005 및 Visual Studio 2008에서 ATL, MFC, CRT, 표준 C++, OpenMP, MSDIA 등의 재배포 가능 라이브러리는 공유 side-by-side 어셈블리로 네이티브 어셈블리 캐시에 배포됩니다. 현재 버전에서는 재배포 가능 라이브러리가 중앙 배포를 사용합니다. 기본적으로 Visual C++를 사용하여 빌드된 모든 응용 프로그램은 매니페스트를 최종 이진에 포함하여 빌드되고 매니페스트는 Visual C++ 라이브러리에 대한 이진의 종속성을 설명합니다. Visual C++ 응용 프로그램에 대한 매니페스트 생성과 관련된 자세한 내용은 [Understanding Manifest Generation for C/C++ Programs](../build/understanding-manifest-generation-for-c-cpp-programs.md)를 참조하세요. 매니페스트는 응용 프로그램이 사용하거나 로컬 배포를 사용하는 라이브러리에 정적으로 연결된 응용 프로그램에는 필요하지 않습니다. 배포에 대한 자세한 내용은 [Deployment in Visual C++](../ide/deployment-in-visual-cpp.md)를 참조하세요.

## <a name="see-also"></a>참고 항목

[C/C++ 격리된 응용 프로그램 및 side-by-side 어셈블리 빌드](../build/building-c-cpp-isolated-applications-and-side-by-side-assemblies.md)