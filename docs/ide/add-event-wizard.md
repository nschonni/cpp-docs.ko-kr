---
title: "이벤트 추가 마법사 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vc.codewiz.event.overview"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "이벤트 추가 마법사[C++]"
ms.assetid: bdd2a7bb-13d5-44d7-abc9-e785ba4e05ce
caps.latest.revision: 6
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 6
---
# 이벤트 추가 마법사
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

이 마법사에서는 MFC ActiveX 컨트롤 프로젝트에 이벤트를 추가합니다.  자신의 이벤트를 지정하거나, 일반적인 스톡 이벤트를 사용자 지정하거나, 스톡 이벤트 목록에서 원하는 이벤트를 선택할 수 있습니다.  
  
 **이벤트 이름**  
 클래스에서 이벤트를 요청하기 위해 자동화 클라이언트에서 사용하는 이름을 설정합니다.  이름을 입력하거나 목록에서 이름을 선택합니다.  
  
 **이벤트 형식**  
 추가할 이벤트 형식을 나타냅니다.  **이벤트 이름** 목록에서 이벤트 이름을 선택하는 경우에만 이 옵션을 사용할 수 있습니다.  
  
|옵션|설명|  
|--------|--------|  
|**스톡**|이 클래스에 대해 단추 클릭 등과 같은 스톡 이벤트가 구현되도록 지정합니다.  스톡 이벤트는 MFC\(Microsoft Foundation Class\) 라이브러리에 정의되어 있습니다.|  
|**사용자 지정**|사용자가 자신의 이벤트를 구현하도록 지정합니다.|  
  
 **내부 이름**  
 이벤트를 보내는 멤버 함수 이름을 설정합니다.  이 옵션은 사용자 지정 이벤트에만 사용할 수 있습니다.  이 이름은 **이벤트 이름**을 기본으로 합니다.  **이벤트 이름**과 다른 이름을 제공하려는 경우 내부 이름을 변경할 수 있습니다.  
  
 **매개 변수 형식**  
 **매개 변수 이름**의 형식을 설정합니다.  목록에서 형식을 선택합니다.  
  
 **매개 변수 이름**  
 이벤트를 통해 전달할 매개 변수의 이름을 설정합니다.  이름을 입력한 다음 **추가**를 클릭하여 매개 변수 목록에 추가해야 합니다.  
  
 **추가**를 클릭하면 **매개 변수 목록**에 매개 변수 이름이 나타납니다.  
  
> [!NOTE]
>  매개 변수 이름을 입력한 다음 **추가**를 클릭하기 전에 **마침**을 클릭하면 이벤트에 매개 변수가 추가되지 않습니다.  사용자가 직접 메서드를 찾고 매개 변수를 삽입해야 합니다. **매개 변수 목록**  
  
 **Add**  
 **매개 변수 이름**에 지정한 매개 변수와 매개 변수의 형식을 **매개 변수 목록**에 추가합니다.  매개 변수를 목록에 추가하려면 **추가**를 클릭해야 합니다.  
  
 **Remove**  
 **매개 변수 목록**에서 선택한 매개 변수를 목록에서 제거합니다.  
  
 **매개 변수 목록**  
 메서드에 대해 현재 추가된 모든 매개 변수와 매개 변수 형식을 표시합니다.  매개 변수를 추가하면 마법사에서는 **매개 변수 목록**을 업데이트하여 각 매개 변수와 해당 형식을 표시합니다.  
  
## 참고 항목  
 [이벤트 추가](../ide/adding-an-event-visual-cpp.md)