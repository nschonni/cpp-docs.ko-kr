---
title: "컴파일러 경고 (수준 1) C4925 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C4925
dev_langs:
- C++
helpviewer_keywords:
- C4925
ms.assetid: a4b206c0-016a-4f28-873a-bb8bb41bad50
caps.latest.revision: 6
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: 91429cdc35b3afd1e1d639c2641b4cd657f82b34
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-warning-level-1-c4925"></a>컴파일러 경고(수준 1) C4925
'method': 스크립트에서 dispinterface 메서드를 호출할 수 없습니다.  
  
 스크립트 언어에서 VT_BYREF 'in' 매개 변수를 만들 수 없습니다. VT_BYREF 'out' 매개 변수만 만들 수 있습니다.  
  
 이 경고를 해결하는 다른 방법은 매개 변수(정의 및 구현)를 포인터 형식으로 설정하지 않는 것입니다.  
  
 다음 샘플에서는 C4925를 생성합니다.  
  
```  
// C4925.cpp  
// compile with: /LD /W1  
#define _ATL_ATTRIBUTES 1  
#include <atlbase.h>  
#include <atlcom.h>  
[ module(name="Test")];  
  
[ dispinterface, uuid("00000000-0000-0000-0000-000000000001") ]  
__interface IDisp {  
   [id(9)] void f([in] int*);  
};  
  
[ coclass, uuid("00000000-0000-0000-0000-000000000002")  ]  
struct CDisp : IDisp {   // C4925  
   void f(int*) {}  
};  
```