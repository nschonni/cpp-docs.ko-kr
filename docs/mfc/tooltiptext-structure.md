---
title: "TOOLTIPTEXT 구조체 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "TOOLTIPTEXT"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "도구 설명[C++], 알림"
  - "TOOLTIPTEXT 구조체"
ms.assetid: 547591bf-80f5-400e-a2a7-0708cfffbb5d
caps.latest.revision: 13
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 9
---
# TOOLTIPTEXT 구조체
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

In writing your [tool tip notification handler](../mfc/handling-ttn-needtext-notification-for-tool-tips.md), you need to use the `TOOLTIPTEXT` structure.  The members of the `TOOLTIPTEXT`structure are:  
  
 `typedef struct {`  
  
 `NMHDR     hdr;        // required for all WM_NOTIFY messages`  
  
 `LPTSTR    lpszText;   // see below`  
  
 `TCHAR     szText[80]; // buffer for tool tip text`  
  
 `HINSTANCE hinst;      // see below`  
  
 `UINT      uflags;     // flag indicating how to interpret the`  
  
 `// idFrom member of the NMHDR structure`  
  
 `// that is included in the structure`  
  
 `} TOOLTIPTEXT, FAR *LPTOOLTIPTEXT;`  
  
 `hdr`  
 Identifies the tool that needs text.  The only member of this structure you might need is the control's command ID.  The control's command ID will be in the `idFrom` member of the `NMHDR` structure, accessed with the syntax `hdr.idFrom`.  See [NMHDR](http://msdn.microsoft.com/library/windows/desktop/bb775514) for a discussion of members of the `NMHDR` structure.  
  
 `lpszText`  
 Address of a string to receive the text for a tool.  
  
 `szText`  
 Buffer that receives the tool tip text.  An application can copy the text to this buffer as an alternative to specifying a string address.  
  
 `hinst`  
 Handle of the instance that contains a string to be used as the tool tip text.  If `lpszText` is the address of the tool tip text, this member is NULL.  
  
 When you handle the `TTN_NEEDTEXT` notification message, specify the string to be displayed in one of the following ways:  
  
-   Copy the text to the buffer specified by the `szText` member.  
  
-   Copy the address of the buffer that contains the text to the `lpszText` member.  
  
-   Copy the identifier of a string resource to the `lpszText` member, and copy the handle of the instance that contains the resource to the `hinst` member.  
  
## 참고 항목  
 [CFrameWnd에서 파생되지 않은 창의 도구 설명](../mfc/tool-tips-in-windows-not-derived-from-cframewnd.md)