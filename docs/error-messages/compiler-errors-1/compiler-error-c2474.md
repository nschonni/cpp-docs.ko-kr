---
title: "컴파일러 오류 C2474 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2474
dev_langs:
- C++
helpviewer_keywords:
- C2474
ms.assetid: 64e6c61e-6e77-480e-bcf0-b30a2fc482ac
caps.latest.revision: 3
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
ms.openlocfilehash: 6ac71627aa3f87d3e61cc2815a70eee4884c0bd3
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c2474"></a>컴파일러 오류 C2474
'keyword': 인접한 세미콜론이 없습니다. 키워드거나 식별자일 수 있습니다.  
  
 컴파일러가 세미콜론을 찾아야 하며 사용자 의도를 확인할 수 없습니다. 이 오류를 해결하려면 세미콜론을 추가합니다.  
  
## <a name="example"></a>예제  
 다음 샘플에서는 C2474를 생성합니다.  
  
```  
// C2474.cpp  
// compile with: /clr /c  
  
ref class A {  
   ref class B {}  
   property int i;   // C2474 error  
};  
  
// OK  
ref class B {  
   ref class D {};  
   property int i;  
};  
  
ref class E {  
   ref class F {} property;   
   int i;  
};  
```