---
title: "표준 컨트롤에서 컨트롤 파생시키기 | Microsoft Docs"
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
  - "공용 컨트롤[C++], 파생"
  - "컨트롤[MFC], 파생"
  - "파생 컨트롤"
  - "표준 컨트롤"
  - "표준 컨트롤, 컨트롤 파생"
  - "Windows 공용 컨트롤[C++], 파생"
ms.assetid: a6f84315-7007-4e0e-8576-78be81254802
caps.latest.revision: 11
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 7
---
# 표준 컨트롤에서 컨트롤 파생시키기
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

As with any [CWnd](../mfc/reference/cwnd-class.md)\-derived class, you can modify a control's behavior by deriving a new class from an existing control class.  
  
### To create a derived control class  
  
1.  Derive your class from an existing control class and optionally override the **Create** member function so that it provides the necessary arguments to the base\-class **Create** function.  
  
2.  Provide message\-handler member functions and message\-map entries to modify the control's behavior in response to specific Windows messages.  [함수에 메시지 매핑](../mfc/reference/mapping-messages-to-functions.md)을 참조하십시오.  
  
3.  Provide new member functions to extend the functionality of the control \(optional\).  
  
 Using a derived control in a dialog box requires extra work.  The types and positions of controls in a dialog box are normally specified in a dialog\-template resource.  If you create a derived control class, you cannot specify it in a dialog template since the resource compiler knows nothing about your derived class.  
  
#### To place your derived control in a dialog box  
  
1.  Embed an object of the derived control class in the declaration of your derived dialog class.  
  
2.  Override the `OnInitDialog` member function in your dialog class to call the `SubclassDlgItem` member function for the derived control.  
  
 `SubclassDlgItem` "dynamically subclasses" a control created from a dialog template.  When a control is dynamically subclassed, you hook into Windows, process some messages within your own application, then pass the remaining messages on to Windows.  For more information, see the [SubclassDlgItem](../Topic/CWnd::SubclassDlgItem.md) member function of class `CWnd` in the *MFC Reference*.  The following example shows how you might write an override of `OnInitDialog` to call `SubclassDlgItem`:  
  
 [!code-cpp[NVC_MFCControlLadenDialog#3](../mfc/codesnippet/CPP/deriving-controls-from-a-standard-control_1.cpp)]  
  
 Because the derived control is embedded in the dialog class, it will be constructed when the dialog box is constructed, and it will be destroyed when the dialog box is destroyed.  Compare this code to the example in [Adding Controls By Hand](../mfc/adding-controls-by-hand.md).  
  
## 참고 항목  
 [컨트롤 만들기 및 사용](../mfc/making-and-using-controls.md)   
 [컨트롤](../mfc/controls-mfc.md)