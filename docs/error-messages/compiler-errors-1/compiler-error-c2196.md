---
title: "컴파일러 오류 C2196 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2196
dev_langs:
- C++
helpviewer_keywords:
- C2196
ms.assetid: fd2f6a58-48ce-4e58-96f8-e37720feb8e7
caps.latest.revision: 8
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
ms.openlocfilehash: 91a2bb14c96095cbab13e69512b9a79f86c8b6b1
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c2196"></a>컴파일러 오류 C2196
case 값 'value'를 이미 사용했습니다.  
  
 switch 문에서 동일한 case 값을 두 번 이상 사용합니다.  
  
 다음 샘플에서는 C2196을 생성합니다.  
  
```  
// C2196.cpp  
int main() {  
   int i = 0;  
   switch( i ) {  
   case 0:  
      break;  
   case 0:   // C2196  
   // try the following line instead  
   // case 1:  
      break;  
   }  
}  
```