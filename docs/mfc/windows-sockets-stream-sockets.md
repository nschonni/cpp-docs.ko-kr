---
title: "Windows 소켓: 스트림 소켓 | Microsoft Docs"
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
  - "소켓[C++], 스트림 소켓"
  - "스트림 소켓[C++]"
  - "Windows 소켓[C++], 스트림 소켓"
ms.assetid: 31faaa34-a995-493f-a30b-b8115293d619
caps.latest.revision: 12
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 8
---
# Windows 소켓: 스트림 소켓
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

This article describes stream sockets, one of the two Windows Socket types available. \(The other type is the [datagram socket](../mfc/windows-sockets-datagram-sockets.md).\)  
  
 Stream sockets provide for a data flow without record boundaries: a stream of bytes that can be bidirectional \(the application is full duplex: it can both transmit and receive through the socket\).  Streams can be relied upon to deliver sequenced, unduplicated data. \("Sequenced" means that packets are delivered in the order sent. "Unduplicated" means that you get a particular packet only once.\) Receipt of stream messages is guaranteed, and streams are well suited to handling large amounts of data.  
  
 The network transport layer may break up or group data into packets of reasonable size.  The `CSocket` class will handle the packing and unpacking for you.  
  
 Streams are based on explicit connections: socket A requests a connection to socket B; socket B accepts or rejects the connection request.  
  
 A telephone call provides a good analogy for a stream.  Under normal circumstances, the receiving party hears what you say in the order that you say it, without duplication or loss.  Stream sockets are appropriate, for example, for implementations such as the File Transfer Protocol \(FTP\), which facilitates transferring ASCII or binary files of arbitrary size.  
  
 Stream sockets are preferable to datagram sockets when the data must be guaranteed to arrive and when data size is large.  For more information about stream sockets, see the Windows Sockets specification.  사양은 [!INCLUDE[winSDK](../atl/includes/winsdk_md.md)]에서 사용할 수 있습니다.  
  
 Using stream sockets can be superior to applications designed to use a datagram socket for broadcasting to all receiving sockets on the network because  
  
-   The broadcast model is subject to network flood \(or "storm"\) problems.  
  
-   The client\-server model adopted subsequently is more efficient.  
  
-   The stream model supplies reliable data transfer, where the datagram model does not.  
  
-   The final model takes advantage of the ability to communicate between Unicode and ANSI socket applications that class CArchive lends to class CSocket.  
  
    > [!NOTE]
    >  If you use class `CSocket`, you must use a stream.  An MFC assertion fails if you specify the socket type as **SOCK\_DGRAM**.  
  
## 참고 항목  
 [MFC의 Windows 소켓](../mfc/windows-sockets-in-mfc.md)   
 [Windows 소켓: 백그라운드](../mfc/windows-sockets-background.md)