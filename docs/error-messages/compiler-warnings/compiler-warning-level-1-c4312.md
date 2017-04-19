---
title: "컴파일러 경고 (수준 1) C4312 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C4312"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4312"
ms.assetid: 541906ed-4f62-4bcb-947f-cf9ae7411bcb
caps.latest.revision: 9
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 9
---
# 컴파일러 경고 (수준 1) C4312
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'identifier' : 'type1'에서 더 큰 'type2'\(으\)로의 변환입니다.  
  
 이 경고는 32비트 값을 64비트 포인터 형식에 할당하려는 식도를 감지합니다. 예를 들어 32비트 `int` 또는 `long`을 64비트 포인터로 캐스팅합니다.  
  
 이 변환은 부호 확장이 발생할 경우 32비트에 맞는 포인터 값에서도 안전하지 않을 수 있습니다.  음의 32비트 정수가 64비트 포인터 형식에 할당될 경우 부호 확장으로 인해 포인터 값이 정수의 값과 다른 메모리 주소를 참조할 수 있습니다.  
  
 이 경고는 64비트 컴파일 대상에 대해서만 표시됩니다.  자세한 내용은 [포인터 사용 규칙](http://msdn.microsoft.com/library/windows/desktop/aa384242)을 참조하세요.  
  
 다음 코드 예제에서는 64비트 대상에 대해 컴파일되는 경우의 C4312를 생성합니다.  
  
```  
// C4312.cpp  
// compile by using: cl /W1 /LD C4312.cpp  
void* f(int i) {  
   return (void*)i;   // C4312 for 64-bit targets  
}  
  
void* f2(__int64 i) {  
   return (void*)i;   // OK  
}  
```