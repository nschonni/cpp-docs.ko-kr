---
title: "omp_destroy_nest_lock | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "omp_destroy_nest_lock"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "omp_destroy_nest_lock OpenMP function"
ms.assetid: 0ab1352b-668f-43dd-b441-31ec4cc53e68
caps.latest.revision: 9
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 9
---
# omp_destroy_nest_lock
[!INCLUDE[vs2017banner](../../../assembler/inline/includes/vs2017banner.md)]

Nestable 잠금을 초기화 하지 않습니다.  
  
## 구문  
  
```  
void omp_destroy_nest_lock(  
   omp_nest_lock_t *lock  
);  
```  
  
## 설명  
 다음은 각 매개 변수에 대한 설명입니다.  
  
 `lock`  
 형식의 변수에 [omp\_nest\_lock\_t](../../../parallel/openmp/reference/omp-nest-lock-t.md) 로 초기화 된 [omp\_init\_nest\_lock](../../../parallel/openmp/reference/omp-init-nest-lock.md).  
  
## 설명  
 자세한 내용은 [3.2.2 omp\_destroy\_lock and omp\_destroy\_nest\_lock Functions](../../../parallel/openmp/3-2-2-omp-destroy-lock-and-omp-destroy-nest-lock-functions.md)를 참조하십시오.  
  
## 예제  
 참조 하십시오 [omp\_init\_nest\_lock](../../../parallel/openmp/reference/omp-init-nest-lock.md) 를 사용 하는 예에 대 한 `omp_destroy_nest_lock`.  
  
## 참고 항목  
 [Functions](../../../parallel/openmp/reference/openmp-functions.md)