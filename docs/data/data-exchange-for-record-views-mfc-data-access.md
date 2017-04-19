---
title: "레코드 뷰의 데이터 교환   (MFC Data Access) | Microsoft Docs"
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
  - "DDX(대화 상자 데이터 교환), 레코드 뷰"
  - "DFX(DAO 레코드 필드 교환)"
  - "DFX(DAO 레코드 필드 교환), 데이터 교환 메커니즘"
  - "DFX(DAO 레코드 필드 교환), 레코드 뷰"
  - "레코드 뷰, 데이터 교환"
  - "RFX(레코드 필드 교환)"
  - "RFX(레코드 필드 교환), 데이터 교환 메커니즘"
  - "RFX(레코드 필드 교환), 레코드 뷰"
ms.assetid: abc52ca7-6997-47a7-98f3-f347f52b1f72
caps.latest.revision: 9
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 9
---
# 레코드 뷰의 데이터 교환   (MFC Data Access)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

[클래스 추가](../mfc/reference/adding-an-mfc-odbc-consumer.md)를 사용하여 레코드 뷰 대화 상자 템플릿 리소스의 컨트롤을 레코드 집합의 필드에 매핑하면 프레임워크가 양방향\(레코드 집합에서 컨트롤로\/컨트롤에서 레코드 집합으로\)의 데이터 교환을 관리합니다.  DDX 메커니즘을 사용하면 데이터를 전송하는 코드를 직접 작성할 필요가 없습니다.  
  
 레코드 뷰의 DDX는 다음 항목과 연동됩니다.  
  
-   `CRecordset` 클래스\(ODBC\)의 레코드 집합용 [RFX](../data/odbc/record-field-exchange-rfx.md)  
  
-   `CDaoRecordset` 클래스\(DAO\)의 레코드 집합용 DFX  
  
 RFX와 DFX의 구현은 다르지만 인터페이스 수준에서는 매우 비슷한 데이터 교환 메커니즘입니다.  DAO 버전인 DFX는 이전 ODBC 버전인 RFX와 비슷하게 모델링됩니다.  따라서 RFX 사용 방법을 알고 있다면 DFX 사용 방법도 알고 있는 것입니다.  
  
 RFX와 DFX는 데이터 소스의 현재 레코드와 레코드 집합 개체의 필드 데이터 멤버 간에 데이터를 이동합니다.  DDX는 필드 데이터 멤버에서 폼의 컨트롤로 데이터를 이동합니다.  이 조합은 먼저 폼 컨트롤을 채운 다음 사용자가 레코드 간을 이동할 때 계속해서 컨트롤을 채웁니다.  또한 업데이트된 데이터를 레코드 집합으로 다시 이동했다가 데이터 소스로 이동할 수도 있습니다.  
  
 다음 그림에는 레코드 뷰에 대한 DDX와 RFX 또는 DFX의 관계가 나와 있습니다.  
  
 ![DDE&#40;Dialog Data Exchange&#41; 및 레코드 필드 교환](../data/media/vc37xt1.gif "vc37XT1")  
DDE\(Dialog Data Exchange\) 및 레코드 필드 교환  
  
 DDX에 대한 자세한 내용은 [대화 상자 데이터 교환 및 유효성 검사](../mfc/dialog-data-exchange-and-validation.md)를 참조하세요.  RFX에 대한 자세한 내용은 [RFX\(레코드 필드 교환\)](../data/odbc/record-field-exchange-rfx.md)를 참조하세요.  
  
## 참고 항목  
 [레코드 뷰  \(MFC Data Access\)](../data/record-views-mfc-data-access.md)   
 [ODBC 드라이버 목록](../data/odbc/odbc-driver-list.md)