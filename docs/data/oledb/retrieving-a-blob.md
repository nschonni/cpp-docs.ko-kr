---
title: "BLOB 검색 | Microsoft Docs"
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
  - "BLOB(이진 대형 개체), 검색"
  - "OLE DB, BLOB(이진 대형 개체)"
  - "BLOB 검색"
ms.assetid: 2893eb0a-5c05-4016-8914-1e40ccbaf0b3
caps.latest.revision: 7
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 7
---
# BLOB 검색
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

여러 방법으로 BLOB\(이진 대형 개체\)를 검색할 수 있습니다.  **DBTYPE\_BYTES**를 사용하여 BLOB를 바이트의 시퀀스로 검색하거나 `ISequentialStream` 같은 인터페이스를 사용할 수 있습니다.  자세한 내용은 *OLE DB Programmer's Reference*에서 [BLOBS and OLE Objects](https://msdn.microsoft.com/en-us/library/ms711511.aspx)를 참조하십시오.  
  
 다음 코드는 `ISequentialStream`을 사용하여 BLOB를 검색하는 방법에 대해 보여 줍니다.  매크로 [BLOB\_ENTRY](../../data/oledb/blob-entry.md)를 사용하면 인터페이스와 인터페이스에 사용되는 플래그를 지정할 수 있습니다.  테이블을 연 후 코드는 `ISequentialStream`에서 **Read**를 반복 호출하여 BLOB의 바이트를 읽습니다.  코드는 다음 레코드를 구하는 `MoveNext`를 호출하기 전에 **Release**를 호출하여 인터페이스 포인터를 삭제합니다.  
  
```  
class CCategories  
{  
public:  
   ISequentialStream*   pPicture;  
  
BEGIN_COLUMN_MAP(CCategories)  
   BLOB_ENTRY(4, IID_ISequentialStream, STGM_READ, pPicture)  
END_COLUMN_MAP()  
};  
  
CTable<CAccessor<CCategories> > categories;  
ULONG          cb;  
BYTE            myBuffer[65536];  
  
categories.Open(session, "Categories");  
while (categories.MoveNext() == S_OK)  
{  
   do  
   {  
      categories.pPicture->Read(myBuffer, 65536, &cb);  
      // Do something with the buffer  
   } while (cb > 0);  
   categories.pPicture->Release();  
}  
```  
  
 BLOB 데이터를 처리하는 매크로에 대한 자세한 내용은 [Macros and Global Functions for OLE DB Consumer Templates](../../data/oledb/macros-and-global-functions-for-ole-db-consumer-templates.md)의 "열 맵 매크로"를 참조하십시오.  
  
## 참고 항목  
 [접근자 사용](../../data/oledb/using-accessors.md)   
 [OLE DB 소비자 템플릿에 대한 매크로 및 전역 함수](../../data/oledb/macros-and-global-functions-for-ole-db-consumer-templates.md)