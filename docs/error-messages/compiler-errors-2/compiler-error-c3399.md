---
title: "컴파일러 오류 C3399 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3399
dev_langs:
- C++
helpviewer_keywords:
- C3399
ms.assetid: 306ad199-d150-4f6c-bcf1-24a7948b93be
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
ms.openlocfilehash: 1ef4492e3984ae66c4dc6bd41b0dc7c40c734c8a
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3399"></a>컴파일러 오류 C3399
'type': 제네릭 매개 변수의 인스턴스를 만들 때는 인수를 지정할 수 없습니다.  
  
 `gcnew()` 제약 조건을 지정할 때 제약 조건 형식이 매개 변수가 없는 생성자를 갖도록 지정합니다. 따라서 해당 형식을 인스턴스화하고 매개 변수를 전달하려고 하면 오류가 발생합니다.  
  
 참조 [제네릭 형식 매개 변수에 대 한 제약 조건 (C + + /cli CLI)](../../windows/constraints-on-generic-type-parameters-cpp-cli.md) 자세한 정보에 대 한 합니다.  
  
## <a name="example"></a>예제  
 다음 샘플에서는 C3399를 생성합니다.  
  
```  
// C3399.cpp  
// compile with: /clr /c  
generic <class T>   
where T : gcnew()  
void f() {  
   T t = gcnew T(1);   // C3399  
   T t2 = gcnew T();   // OK  
}  
```