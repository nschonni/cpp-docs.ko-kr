---
title: "컴파일러 오류 C3262 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3262
dev_langs:
- C++
helpviewer_keywords:
- C3262
ms.assetid: 3e74b9aa-de3c-4492-9331-ee73012b958b
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
ms.sourcegitcommit: c243063a9770542f137d5950e8a269f771960f74
ms.openlocfilehash: fbb97c94a077f101c196628b74ef147f1ffa451a
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-error-c3262"></a>컴파일러 오류 C3262
잘못된 배열 인덱싱: '#'개 차원을 '#'차원 'array type'에 대해 지정했습니다.  
  
배열 아래 첨자가 잘못되었습니다. 인덱스 수가 배열 차원 수와 일치하지 않을 수 있습니다.  
  
다음 샘플에서는 C3262를 생성합니다.  
  
```  
// C3262.cpp  
// compile with: /clr  
#using <mscorlib.dll>  
using namespace System;  
  
#define ARRAY_SIZE 2  
  
ref class MyClass {  
public:  
   int m_i;  
};  
  
// returns a multidimensional managed array of a reference type  
array<MyClass^, 2>^ Test0() {  
   int i, j;  
   array< MyClass^, 2 >^ local = new array< MyClass^, 2 >  
      (ARRAY_SIZE, ARRAY_SIZE);  
  
   for (i = 0 ; i < ARRAY_SIZE ; i++)  
      for (j = 0 ; j < ARRAY_SIZE ; j++) {  
         local[i][j] = new MyClass;   // C3262  
         // try the following line instead  
         // local[i,j] = new MyClass;     
         local[i,j] -> m_i = i;  
      }  
  
      return local;  
}  
  
int main() {     
   int i, j;  
  
   array< MyClass^, 2 >^ MyClass0;  
   MyClass0 = Test0();  
}  
```  
