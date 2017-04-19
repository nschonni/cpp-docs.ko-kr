---
title: "인터넷의 액티브 문서 | Microsoft Docs"
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
  - "활성 문서[C++], 만들기"
  - "활성 문서[C++], 프로그래밍 단계"
  - "활성 문서[C++], 응용 프로그램 마법사 사용"
  - "응용 프로그램 마법사[C++]"
  - "응용 프로그램 마법사[C++], 활성 문서"
ms.assetid: a46bd8a0-e27a-4116-b1bf-dacdb7ae78d1
caps.latest.revision: 10
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 6
---
# 인터넷의 액티브 문서
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Active documents provide an extension to traditional embedded objects.  The Active documents may be multipage and are displayed in the entire client area.  They do traditional menu negotiation, and can be edited in\-place as well as in an open window in the server application.  Instead of displaying as a small rectangle surrounded by a hatched border, Active documents are full frame and always in\-place active.  
  
 Active documents can be viewed in a container like the Microsoft Office Binder, which provides a way to create a compound document made up of different document types like Excel, Word, and your custom document type, each of which can be edited full frame.  Active documents can also be displayed in a browser such as Microsoft Internet Explorer, which is an Active document container.  
  
 **Active document advantages include:**  
  
-   Documents can be viewed full frame, in the entire client window.  
  
-   Documents can be opened in a separate application window.  
  
     For the document to open, the helper application must exist on the client, or be downloaded separately before the application can run.  A viewer may be written to provide limited functionality \(Word, PowerPoint, and Excel provide viewers for their documents\).  The full version of the application can provide full editing support.  
  
-   Documents are always in\-place active.  
  
-   Menu commands invoked from the container can be routed to your document.  
  
-   Documents can be viewed in a Web browser.  This provides seamless integration between your documents and other Web pages.  
  
     A user can browse an HTML Web page, then an Excel spreadsheet, and then to a document that you have written using MFC support for Active documents.  The user can navigate using the familiar Web interface, as the browser switches seamlessly between the menus and views of an HTML page, Excel, and your application's document.  
  
-   All applications are displayed in a common frame.  
  
## Requirements for Active Documents  
 The interfaces listed in the table below include interfaces already required for embedded servers and several new interfaces specific to Active documents.  MFC provides default implementations for most of these interfaces in the [COleServerDoc](../mfc/reference/coleserverdoc-class.md) class.  
  
|A document that ...|Implements these interfaces|  
|-------------------------|---------------------------------|  
|Uses compound files as its storage mechanism.|`IPersistStorage`.|  
|Supports the basic embedding features of Active documents, including Create From File.|`IPersistFile`, `IOleObject` 및 `IDataObject`|  
|Supports in\-place activation.|`IOleInPlaceObject` and `IOleInPlaceActiveObject` \(using the container's `IOleInPlaceSite` and **IOleInPlaceFrame** interfaces\).|  
|Supports the Active document extensions that involve these new interfaces.  Some interfaces are optional.|`IOleDocument`, `IOleDocumentView`, `IOleCommandTarget` 및 `IPrint`가 있습니다.|  
  
 MFC provides support for extending existing embedded server support to Active documents.  
  
## Add Active Document Support to a New Application  
 To create a new application with Active document support: In the MFC Application Wizard, on the **Compound Document Support** page, under "Select compound document support" choose **Full\-server** or **Container\/Full\-server**, and under "Select additional options" select the check box for **Active document server**.  
  
##  <a name="_core_convert_an_existing_mfc_in.2d.process_server_to_an_activex_document_server"></a> Convert an Existing MFC In\-Process Server to an Active Document Server  
 If your application was created with a version of Visual C\+\+ prior to version 4.2 and is already an in\-process server, you can add Active document support by making changes to the following classes:  
  
|Class type|Formerly derived from|Change to derive from|  
|----------------|---------------------------|---------------------------|  
|In\-Place Frame|`COleIPFrameWnd`|**COleDocIPFrameWnd**|  
|항목|`COleServerItem`|`CDocObjectServerItem`|  
  
 You will also change how information is entered in the registry, and make several other changes.  If your application currently has no COM components support, you can add server support by running the Application Wizard and integrating the COM component\-specific code with your existing application.  
  
## 참고 항목  
 [MFC 인터넷 프로그래밍 작업](../mfc/mfc-internet-programming-tasks.md)   
 [MFC 인터넷 프로그래밍 기본 사항](../mfc/mfc-internet-programming-basics.md)