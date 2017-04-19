---
title: "컴파일러 오류 C2378 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2378
dev_langs:
- C++
helpviewer_keywords:
- C2378
ms.assetid: 507a91c6-ca72-48df-b3a4-2cf931c86806
caps.latest.revision: 9
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
ms.openlocfilehash: fbb23b2e7528728e1c4378b043136c97e46cfb96
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c2378"></a>컴파일러 오류 C2378
'identifier': 재정의. 형식 정의를 사용하여 기호를 오버로드할 수 없습니다.  
  
 식별자가 `typedef`로 다시 정의되었습니다.  
  
 다음 샘플에서는 C2378을 생성합니다.  
  
```  
// C2378.cpp  
// compile with: /c  
int i;  
typedef int i;   // C2378  
typedef int b;   // OK  
```