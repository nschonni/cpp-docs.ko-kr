---
title: "컴파일러 오류 C3126 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3126
dev_langs:
- C++
helpviewer_keywords:
- C3126
ms.assetid: e72658a3-5d85-4a31-89a4-dbc3d475973d
caps.latest.revision: 8
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
translationtype: Machine Translation
ms.sourcegitcommit: c243063a9770542f137d5950e8a269f771960f74
ms.openlocfilehash: 619760ac4696f7cf083015216f0c940b207e0372
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-error-c3126"></a>컴파일러 오류 C3126
' union' 관리 되는 ' type ' 내에서 정의할 수 없습니다.  
  
 관리 되는 형식 내 공용 구조체를 정의할 수 없습니다.  
  
 다음 샘플에서는 C3126 오류가 생성 됩니다.  
  
```  
// C3126_2.cpp  
// compile with: /clr /c  
ref class Test  
{  
   union x  
   {   // C3126  
      int a;  
      int b;  
   };  
};  
```  
