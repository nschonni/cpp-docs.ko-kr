---
title: "메시지 | Microsoft Docs"
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
  - "메시지"
  - "메시지, MFC"
ms.assetid: b1476310-a135-42ca-817c-444fb3675491
caps.latest.revision: 9
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 5
---
# 메시지
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

The message loop in the **Run** member function of class `CWinApp` retrieves queued messages generated by various events.  For example, when the user clicks the mouse, Windows sends several mouse\-related messages, such as `WM_LBUTTONDOWN` when the left mouse button is pressed and `WM_LBUTTONUP` when the left mouse button is released.  The framework's implementation of the application message loop dispatches the message to the appropriate window.  
  
 The important categories of messages are described in [Message Categories](../mfc/message-categories.md).  
  
## 참고 항목  
 [프레임워크의 메시지 및 명령](../mfc/messages-and-commands-in-the-framework.md)