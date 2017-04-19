---
title: "문서/뷰 아키텍처의 대체 | Microsoft Docs"
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
  - "CDocument 클래스, 공간 요구 사항"
  - "문서, 응용 프로그램"
  - "뷰, 응용 프로그램"
ms.assetid: 2c22f352-a137-45ce-9971-c142173496fb
caps.latest.revision: 9
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 5
---
# 문서/뷰 아키텍처의 대체
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

일반적으로 MFC 응용 프로그램은 문서\/뷰 아키텍처를 사용하여 정보, 파일 형식 및 사용자 데이터의 시각적 표현을 관리합니다.  대부분의 데스크톱 응용 프로그램에서는 문서\/뷰 아키텍처는 적당하고 효율적인 응용 프로그램 아키텍처입니다.  이 아키텍처 구분 데이터 보기에서 대부분의 경우에서 응용 프로그램을 간단히 만들고 코드 중복을 줄일 수 있습니다.  
  
 그러나 문서\/뷰 아키텍처는 일부 상황에 적합하지 않습니다.  이 예제를 참조하십시오:  
  
-   Windows 용 C에서에서 작성된 응용 프로그램을 포팅하는 경우 문서\/뷰 지원 응용 프로그램에 추가하기 전에 포트를 완료하는 것이 좋습니다.  
  
-   Lightweight 유틸리티를 작성 하는 경우, 문서\/뷰 아키텍처 없이 할 수 있다는 것을 알 수 있습니다.  
  
-   원래 코드가 이미 데이터보기와 데이터 관리를 혼합하는 경우, 문서 \/ 뷰 모델에 코드를 이동하는 것은 두 가지를 구분해야하기 때문에 노력할 가치가 없습니다.  코드를 벗어날 수도 있습니다.  
  
 문서\/뷰 아키텍처를 사용하지 않는 응용 프로그램을 만들려면 MFC 응용 프로그램 마법사의 1 단계에서 **문서\/뷰 아키텍처 지원** 체크박스를 해제합니다.  자세한 내용은 [MFC 응용 프로그램 마법사](../mfc/reference/mfc-application-wizard.md) 을 참조하십시오.  
  
> [!NOTE]
>  MFC 응용 프로그램 마법사에서 생성된 대화 상자 기반 응용 프로그램으로 문서\/뷰 아키텍처를 하지마십시오.  **문서\/뷰 아키텍처 지원** 체크 박스는 대화 응용 프로그램 종류를 선택 하면 비활성화됩니다.  
  
 Visual C\+\+ 마법사뿐만 아니라 소스 및 대화 상자 편집기는 단지 그들이 다른 마법사에서 생성 된 소프트웨어와 같이 생성된 응용 프로그램에서 작동합니다.  응용 프로그램 도구 모음, 스크롤 막대 및 상태 표시줄을 지원할 수 있으며 이  **About** 상자를 가집니다.  응용 프로그램은 문서 템플릿이 등록 되지 않고, 문서 클래스는 포함되지 않습니다.  
  
 생성된 응용 프로그램은 뷰 클래스와   `CWnd` 에서 파생된 **CChildView**을 갖는 것을 주목하십시오.  MFC 만들고 응용 프로그램에서 만든 프레임 창 내에서 뷰 클래스의 한 인스턴스를 배치합니다.  위치를 단순화하고 응용 프로그램의 콘텐츠를 관리하기 때문에 MFC에서는 여전히 보기 창을 사용하여 실시합니다.  이 클래스의  `OnPaint`  멤버에 그리기 코드를 추가할 수 있습니다.  코드에서는 프레임 대신 뷰에 스크롤 막대를 추가해야 합니다.  
  
 MFC에서 제공하는 문서 \/ 뷰 아키텍처는 응용 프로그램의 기본 기능을 많이 구현에 대한 책임이 있기 때문에, 프로젝트에 자사의 부재는 응용 프로그램의 많은 중요한 기능을 구현하기위한 책임이 있음을 의미합니다:  
  
-   MFC 응용 프로그램 마법사에서 제공된 경우, 응용 프로그램에 대한 메뉴는 오직 **파일** 메뉴의  `New`  및  `Exit`  명령만 포함합니다. \( `New` 명령은 문서\/뷰 없이 SDI 응용 프로그램을 지원하고, MDI 응용 프로그램에만 명령을 사용할 수 없습니다.\) 생성된 메뉴 리소스는 MRU \(최근에 사용한\) 목록을 지원하지 않습니다.  
  
-   처리기 함수를 구현하고 **파일**의 **열기** 및 **저장**을 포함한 응용 프로그램이 지원하는 모든 명령에 대한 구현을 해야합니다.   MFC 지원은 문서\/뷰 아키텍처에 바인딩되어 있지만 해당 일반적으로 이러한 기능을 지원하는 코드를 제공합니다.  
  
-   요청 하면 응용 프로그램의 도구 모음은 최소화될 것입니다.  
  
 강력한 마법사가 올바른 MFC 아키텍처를 보장 있기 때문에, 문서 \/ 뷰 아키텍처를하지 않고 응용 프로그램을 만들 수 MFC 응용 프로그램 마법사를 사용하는 것이 좋습니다.  그러나 마법사를 사용하지 않도록해야하는 경우, 코드에서 문서 \/ 뷰 아키텍처를 우회하기 위한 몇 가지 방법은 다음과 같습니다.  
  
-   문서를 사용하지 않는 부속물로 취급하고, 위에서 제안했듯이 뷰 클래스에서 데이터 관리 코드를 구현합니다.  문서에 대한 오버 헤드는 상대적으로 낮습니다.  단일  [CDocument](../mfc/reference/cdocument-class.md) 개체는 자체의 오버 헤드의 작은 양을 발생시키고,   **CDocument**의 기본 클래스인  [CCmdTarget](../mfc/reference/ccmdtarget-class.md) 및  [CObject](../mfc/reference/cobject-class.md)의 작은 오버 헤드를 더합니다.  후자의 클래스는 모두 작습니다.  
  
     **CDocument**에 선언합니다.  
  
    -   두  `CString`  개체입니다.  
  
    -   세 개의  **BOOL** 입니다.  
  
    -   하나의  `CDocTemplate`  포인터입니다.  
  
    -   문서 보기 목록이 들어있는 하나의  `CPtrList`  개체입니다.  
  
     또한, 문서는 문서 개체를 만들 수있는 시간의 양, 그 뷰 개체, 프레임 창 및 문서 템플릿 개체가 필요합니다.  
  
-   문서와 뷰를 사용하지 않는 전문으로 취급합니다.  데이터 관리 및 그리기 코드를 뷰 대신 프레임 창에 넣습니다.  이 방법은 C 언어 프로그래밍 모델에 더 가깝습니다.  
  
-   MFC 프레임 워크의 문서 및 뷰를 만들어 제거하는 부분을 재정의 합니다.  문서 작성 프로세스는  `CWinApp::AddDocTemplate` 을 호출하여 시작합니다.   `InitInstance`  의 프레임 창을 만드는 대신 응용 프로그램 클래스에서   `InitInstance`  멤버 함수를 호출하는 것을 제거합니다.  프레임 창 클래스에서 데이터 관리 코드를 넣습니다.  [문서\/뷰 만들기](../mfc/document-view-creation.md)에서는 문서\/뷰 만들기 프로세스를 보여 줍니다.  이 방법은 작업량이 많고 프레임 워크에 대한 깊은 이해가 필요하지만 문서\/뷰 오버 헤드를 완전히 해제하면 됩니다.  
  
 문서  [MFC: 문서 데이터베이스 클래스 사용 및 뷰](../data/mfc-using-database-classes-without-documents-and-views.md)는 데이터베이스 응용 프로그램의 컨텍스트에서 문서\/뷰 대안의 구체적인 예제를 제공합니다.  
  
## 참고 항목  
 [문서\/뷰 아키텍처](../mfc/document-view-architecture.md)