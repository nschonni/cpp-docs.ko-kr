---
title: "컴파일러 오류 C2890 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2890
dev_langs:
- C++
helpviewer_keywords:
- C2890
ms.assetid: 49147375-182c-42b1-b170-f475cd436d47
caps.latest.revision: 9
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
ms.openlocfilehash: d29b7a2f9a618639b934a32d92d2655766f094ba
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-error-c2890"></a>컴파일러 오류 C2890
'class': ref 클래스는 하나의 인터페이스가 아닌 기본 클래스를 하나만 사용할 수 있습니다  
  
 참조 클래스에서 하나의 기본 클래스를 하나만 사용할 수 있습니다.  
  
 다음 샘플에서는 C2890 오류가 생성 됩니다.  
  
```  
// C2890.cpp  
// compile with: /clr /c  
ref class A {};  
ref class B {};  
ref class C : public A, public B {};   // C2890  
ref class D : public A {};   // OK  
```  
