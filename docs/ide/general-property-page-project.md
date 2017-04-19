---
title: "일반 속성 페이지(프로젝트) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "VC.Project.VCConfiguration.IntermediateDirectory"
  - "VC.Project.VCConfiguration.ConfigurationType"
  - "VC.Project.VCConfiguration.ManagedExtensions"
  - "VC.Project.VCConfiguration.BuildBrowserInformation"
  - "VC.Project.VCConfiguration.BuildLogFile"
  - "VC.Project.VCConfiguration.PlatformToolset"
  - "VC.Project.VCConfiguration.TargetName"
  - "VC.Project.VCConfiguration."
  - "VC.Project.VCConfiguration.TargetExt"
  - "VC.Project.VCConfiguration.ATLMinimizesCRunTimeLibraryUsage"
  - "VC.Project.VCConfiguration.ReferencesPath"
  - "VC.Project.VCConfiguration.DeleteExtensionsOnClean"
  - "VC.Project.VCConfiguration.useOfMfc"
  - "VC.Project.VCConfiguration.CharacterSet"
  - "VC.Project.VCGeneralMakefileSettings.ConfigurationType"
  - "VC.Project.VCConfiguration.OutputDirectory"
  - "VC.Project.VCConfiguration.AppSupport"
  - "VC.Project.VCConfiguration.ToolFiles"
  - "VC.Project.VCConfiguration.useOfATL"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "빌드 정리 옵션"
  - "출력 파일, 디렉터리 설정"
  - "유니코드, C++ 빌드 구성 만들기"
ms.assetid: 593b383c-cd0f-4dcd-ad65-9ec9b4b19c45
caps.latest.revision: 30
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 30
---
# 일반 속성 페이지(프로젝트)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

솔루션 탐색기에서 프로젝트 노드를 마우스 오른쪽 단추로 클릭하고 **속성**을 선택하면 **일반** 속성 페이지에서 **구성 속성** 노드의 왼쪽 창에 다음 두 섹션이 표시됩니다.  
  
-   일반  
  
-   프로젝트 기본값  
  
## 일반  
 일반 섹션의 속성은 빌드 프로세스에서 생성되는 파일의 위치 및 **정리** 옵션\(**빌드** 메뉴\)이 선택된 경우 삭제할 파일에 영향을 줍니다.  
  
 **대상 플랫폼**  
 프로젝트를 실행할 플랫폼을 지정합니다. 예를 들어 Windows, Android 또는 iOS입니다. 값이 **Windows 10**이면 프로젝트가 유니버설 Windows 플랫폼을 대상으로 합니다. 이전 버전의 Windows를 대상으로 하는 경우 버전이 표시되지 않고 이 필드의 값이 단순히 **Windows**로 표시됩니다. 이 필드는 프로젝트를 만들 때 설정되는 읽기 전용 필드입니다.  
  
 **대상 플랫폼 버전**  
 Windows 플랫폼의 경우 프로젝트 빌드에 사용되는 Windows SDK의 버전을 지정합니다. Windows의 경우 Windows SDK 버전입니다.[!INCLUDE[vs_dev14](../ide/includes/vs_dev14_md.md)]는 Windows SDK 8.1과 함께 제공됩니다.[Windows 10용 도구](http://go.microsoft.com/fwlink/p/?LinkId=617631)를 설치한 경우 설치한 도구의 각 버전이 드롭다운에 나타납니다.  
  
 Windows 7 또는 Windows Vista를 대상으로 하려면 해당 플랫폼에 대해 Windows SDK 8.1이 이전 버전과 호환되므로 **8.1** 값을 사용합니다. 또한 targetver.h에서 \_WIN32\_WINNT에 대한 적절한 값을 정의해야 합니다. Windows 7의 경우 0x0601입니다.[WINVER 및 \_WIN32\_WINNT 수정](../porting/modifying-winver-and-win32-winnt.md)을 참조하세요.  
  
 [!INCLUDE[vs_dev11_long](../build/includes/vs_dev11_long_md.md)]에 포함된 v110\_xp 플랫폼 도구 집합을 설치하면 [!INCLUDE[vsprvs](../assembler/masm/includes/vsprvs_md.md)]의 최신 버전을 사용하여 Windows XP 및 [!INCLUDE[WinXPSvr](../build/includes/winxpsvr_md.md)] 프로젝트를 빌드할 수 있습니다. 이 플랫폼 도구 집합을 다운로드하고 사용하는 방법에 대한 자세한 내용은 [Windows XP용 C\+\+ 11 프로그램 구성](../build/configuring-programs-for-windows-xp.md)을 참조하세요. 플랫폼 도구 집합을 변경하는 방법에 대한 자세한 내용은 [방법: 대상 프레임워크 및 플랫폼 도구 집합 수정](../build/how-to-modify-the-target-framework-and-platform-toolset.md)을 참조하세요.  
  
 **대상 플랫폼 최소 버전**  
 프로젝트를 실행할 수 있는 가장 낮은 플랫폼 버전을 지정합니다. 이 속성은 Windows 유니버설 프로젝트와 같이 프로젝트 형식이 지원하는 경우에만 나타납니다. 앱이 최신 Windows SDK 버전의 기능을 활용할 수 있지만 해당 기능이 없는 이전 버전에서도 일부 기능은 손실되지만 실행될 수 있는 경우 이러한 두 속성의 값이 다를 수 있습니다. 이 경우 코드에서 런타임에 실행 중인 플랫폼의 버전을 확인해야 하며, 이전 플랫폼 버전에서 사용할 수 없는 기능은 사용하지 않도록 해야 합니다.  
  
 Visual C\+\+는 이 옵션을 적용하지 않습니다. C\# 및 JavaScript와 같은 다른 언어와의 일관성을 위해 및 프로젝트 사용자를 위한 지침으로 포함되었습니다. Visual C\+\+는 최소 버전에서 사용할 수 없는 기능을 사용하는 경우 오류를 생성하지 않습니다.  
  
 **출력 디렉터리**  
 링커 등의 도구가 빌드 프로세스 중에 생성되는 모든 최종 출력 파일을 배치하는 디렉터리를 지정합니다. 일반적으로 이 디렉터리에는 링커, 라이브러리 관리자 또는 BSCMake와 같은 도구의 출력이 포함됩니다.  
  
 프로그래밍 방식으로 이 속성에 액세스하려면 <xref:Microsoft.VisualStudio.VCProjectEngine.VCConfiguration.OutputDirectory%2A>를 참조하세요.  
  
 **중간 디렉터리**  
 컴파일러 등의 도구가 빌드 프로세스 중에 생성되는 모든 중간 파일을 배치하는 디렉터리를 지정합니다. 일반적으로 이 디렉터리에는 C\/C\+\+ 컴파일러, MIDL 및 리소스 컴파일러와 같은 도구의 출력이 포함됩니다.  
  
 프로그래밍 방식으로 이 속성에 액세스하려면 <xref:Microsoft.VisualStudio.VCProjectEngine.VCConfiguration.IntermediateDirectory%2A>를 참조하세요.  
  
 **대상 이름**  
 이 프로젝트에서 생성하는 파일 이름을 지정합니다.  
  
 **대상 확장명**  
 이 프로젝트에서 생성하는 파일 이름 확장명\(예: .exe 또는 .dll\)을 지정합니다.  
  
 **정리할 때 삭제할 확장명**  
 **정리** 옵션\(**빌드** 메뉴\)은 프로젝트 구성이 빌드되는 중간 디렉터리에서 파일을 삭제합니다. 이 속성을 통해 지정된 확장명을 가진 파일은 **정리**를 실행하거나 다시 빌드를 수행할 경우 삭제됩니다. 중간 디렉터리에 있는 이러한 확장명의 파일뿐 아니라 빌드 시스템은 위치에 관계없이 알려진 빌드 출력\(.obj 파일과 같은 중간 출력 포함\)도 삭제합니다. 와일드카드 문자를 지정할 수 있습니다.  
  
 프로그래밍 방식으로 이 속성에 액세스하려면 <xref:Microsoft.VisualStudio.VCProjectEngine.VCConfiguration.DeleteExtensionsOnClean%2A>를 참조하세요.  
  
 **빌드 로그 파일**  
 프로젝트를 빌드할 때마다 생성되는 로그 파일에 대해 기본값이 아닌 위치를 지정할 수 있습니다.  
  
 프로젝트 매크로를 사용하여 디렉터리 위치를 변경할 수 있습니다.[빌드 명령 및 속성 매크로](../ide/common-macros-for-build-commands-and-properties.md)을 참조하세요.  
  
 **플랫폼 도구 집합**  
 프로젝트가 다른 버전의 Visual C\+\+ 라이브러리 및 컴파일러를 대상으로 할 수 있도록 허용합니다.[!INCLUDE[vcprvc](../build/includes/vcprvc_md.md)] 프로젝트는 [!INCLUDE[vs_dev11_long](../build/includes/vs_dev11_long_md.md)]\(**v100**\)의 기본 도구 집합 혹은 Windows XP에서 실행 가능한 실행 파일을 만드는 도구 집합 중 하나를 대상으로 합니다.  
  
## 프로젝트 기본값  
 프로젝트 기본값 섹션의 속성은 수정할 수 있는 기본 속성을 나타냅니다. 이러한 속성에 대한 정의는 *설치 디렉터리*\\VC\\VCProjectDefaults의 .props 파일에서 확인할 수 있습니다.  
  
 **구성 형식**  
 선택할 수 있는 여러 구성 형식이 있습니다.  
  
-   **응용 프로그램\(.exe\)**은 링커 도구 집합\(C\/C\+\+ 컴파일러, MIDL, 리소스 컴파일러, 링커, BSCMake, XML 웹 서비스 프록시 생성기, 사용자 지정 빌드, 사전 빌드, 사전 링크, 사후 빌드 이벤트\)을 표시합니다.  
  
-   **동적 라이브러리\(.dll\)**는 링커 도구 집합을 표시하고 \/DLL 링커 옵션을 지정하고 CL에 \_WINDLL define을 추가합니다.  
  
-   **메이크파일**은 메이크파일 도구 집합\(NMake\)을 표시합니다.  
  
-   **정적 라이브러리\(.lib\)**는 라이브러리 관리자 도구 집합\(링커를 라이브러리 관리자로 대체하고 XML 웹 서비스 프록시 생성기를 생략하는 점을 제외하고 링커 도구 집합과 같음\)을 표시합니다.  
  
-   **유틸리티**는 유틸리티 도구 집합\(MIDL, 사용자 지정 빌드, 사전 빌드, 사후 빌드 이벤트\)을 표시합니다.  
  
 프로그래밍 방식으로 이 속성에 액세스하려면 <xref:Microsoft.VisualStudio.VCProjectEngine.VCConfiguration.ConfigurationType%2A>를 참조하세요.  
  
 **MFC 사용**  
 MFC 프로젝트가 MFC DLL에 정적 또는 동적으로 연결하는지를 지정합니다. 비 MFC 프로젝트는 **표준 Windows 라이브러리 사용**을 선택하여 MFC를 사용할 때 포함되는 다양한 Win32 라이브러리에 연결할 수 있습니다.  
  
 프로그래밍 방식으로 이 속성에 액세스하려면 <xref:Microsoft.VisualStudio.VCProject.VCProjectConfigurationProperties.useOfMfc%2A>를 참조하세요.  
  
 **ATL 사용**  
 ATL 프로젝트가 ATL .DLL에 정적 또는 동적으로 연결하는지를 지정합니다.**ATL 사용 안 함** 이외의 설정을 지정하면 컴파일러의 **명령줄** 속성 페이지에 define이 추가됩니다.  
  
 프로그래밍 방식으로 이 속성에 액세스하려면 <xref:Microsoft.VisualStudio.VCProject.VCProjectConfigurationProperties.useOfATL%2A>를 참조하세요.  
  
 **문자 집합**  
 \_UNICODE 또는 \_MBCS를 설정해야 하는지를 정의합니다. 해당하는 경우 링커 진입점에도 영향을 줍니다.  
  
 프로그래밍 방식으로 이 속성에 액세스하려면 <xref:Microsoft.VisualStudio.VCProject.VCProjectConfigurationProperties.CharacterSet%2A>를 참조하세요.  
  
 **공용 언어 런타임 지원**  
 [\/clr](../build/reference/clr-common-language-runtime-compilation.md) 컴파일러 옵션이 사용되게 합니다.  
  
 프로그래밍 방식으로 이 속성에 액세스하려면 <xref:Microsoft.VisualStudio.VCProject.VCProjectConfigurationProperties.ManagedExtensions%2A>를 참조하세요.  
  
 **전체 프로그램 최적화**  
 [\/GL](../build/reference/gl-whole-program-optimization.md) 컴파일러 옵션 및 [\/LTCG](../build/reference/ltcg-link-time-code-generation.md) 링커 옵션을 지정합니다.  
  
 **Windows 스토어 앱 지원**  
 이 프로젝트가 [!INCLUDE[win8_appname_long](../build/includes/win8_appname_long_md.md)] 응용 프로그램을 지원하는지 여부를 지정합니다. 자세한 내용은 [\/ZW\(Windows Runtime 컴파일\)](../build/reference/zw-windows-runtime-compilation.md) 및 Windows 개발자 센터를 참조하세요.  
  
## 참고 항목  
 [속성 페이지](../ide/property-pages-visual-cpp.md)