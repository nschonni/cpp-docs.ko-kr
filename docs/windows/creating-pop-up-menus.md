---
title: "Creating Pop-up Menus | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "context menus, Menu Editor"
  - "pop-up menus, creating"
  - "menus, pop-up"
  - "menus, creating"
  - "shortcut menus, creating"
  - "pop-up menus, displaying"
ms.assetid: dff4dddf-2e8d-4c34-b755-90baae426b58
caps.latest.revision: 11
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 11
---
# Creating Pop-up Menus
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

[팝업 메뉴](../mfc/menus-mfc.md)에는 자주 사용되는 명령이 표시됩니다. 포인터 위치에 대한 상황에 맞는 메뉴일 수 있습니다. 응용 프로그램에서 팝업 메뉴를 사용하려면 메뉴 자체를 빌드한 후 응용 프로그램 코드에 연결해야 합니다.  
  
 메뉴 리소스를 만든 후에는 응용 프로그램 코드에서 메뉴 리소스를 로드하고 [TrackPopupMenu](http://msdn.microsoft.com/library/windows/desktop/ms648002)를 사용하여 메뉴를 표시해야 합니다. 사용자가 팝업 메뉴 바깥쪽을 클릭하여 해제하거나 명령을 클릭한 경우 해당 함수가 반환됩니다. 사용자가 명령을 선택하는 경우 해당 명령 메시지가 핸들이 전달된 창으로 전송됩니다.  
  
### 팝업 메뉴를 만들려면  
  
1.  빈 제목을 사용하여 [메뉴를 만듭니다](../windows/creating-a-menu.md). **캡션**을 제공하지 마세요.  
  
2.  [새 메뉴에 메뉴 명령을 추가](../windows/adding-commands-to-a-menu.md)합니다. 빈 메뉴 제목\(여기에 입력이라는 임시 캡션이 표시됨\) 아래의 첫 번째 메뉴 명령으로 이동합니다.**캡션** 및 기타 정보를 입력합니다.  
  
     팝업 메뉴의 다른 모든 메뉴 명령에 대해 이 프로세스를 반복합니다.  
  
3.  메뉴 리소스를 저장합니다.  
  
    > [!TIP]
    >  팝업 메뉴를 보는 방법에 대한 자세한 내용은 [팝업 메뉴로 메뉴 보기](../windows/viewing-a-menu-as-a-pop-up-menu.md)를 참조하세요.  
  
 관리되는 프로젝트에 리소스를 추가하는 방법은 *.NET Framework 개발자 가이드*에서 [응용 프로그램의 리소스](../Topic/Resources%20in%20Desktop%20Apps.md)를 참조하세요. 관리되는 프로젝트에 리소스 파일 추가, 리소스 액세스, 정적 리소스 표시, 속성에 리소스 문자열 할당 등의 작업을 수동으로 수행하는 방법에 대한 자세한 내용은 [Walkthrough: Using Resources for Localization with ASP.NET](../Topic/Walkthrough:%20Using%20Resources%20for%20Localization%20with%20ASP.NET.md) 항목을 참조하세요.  
  
 **요구 사항**  
  
 Win32  
  
## 참고 항목  
 [Connecting a Pop\-up Menu to Your Application](../windows/connecting-a-pop-up-menu-to-your-application.md)   
 [Menu Editor](../mfc/menu-editor.md)