---
title: "형식 캐스팅 변환 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "변환[C++], 형식 캐스팅"
  - "데이터 형식 변환[C++], 형식 캐스팅 변환"
  - "명시적 형식 변환"
  - "형식 캐스팅"
  - "형식 캐스팅[C++], 형식 캐스팅 변환 정보"
  - "형식 캐스팅 변환[C++]"
ms.assetid: 57ab5902-f12f-4326-a2f6-6282f1d4025a
caps.latest.revision: 8
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 8
---
# 형식 캐스팅 변환
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

형식 캐스팅을 사용하여 명시적으로 형식을 변환할 수 있습니다.  
  
 **구문**  
  
 *cast\-expression*:  
 *unary expression*  
  
 **\(**  *type\-name*  **\)**  *cast\-expression*  
  
 *type\-name*:  
 *specifier\-qualifier\-list abstract\-declarator*  opt  
  
 *type\-name*은 형식이고 *cast\-expression*은 해당 형식으로 변환할 값입니다.  형식 캐스팅을 사용하는 식은 l\-value가 아닙니다.  *cast\-expression*은 *type\-name* 형식의 변수에 할당된 것처럼 변환됩니다.  할당에 대한 변환 규칙\([할당 변환](../c-language/assignment-conversions.md)에 개괄되어 있음\)은 형식 캐스팅에도 적용됩니다.  다음 표에서는 임의의 형식으로 캐스팅될 수 있는 형식을 보여 줍니다.  
  
### 올바른 형식 캐스팅  
  
|대상 형식|잠재적 소스|  
|-----------|------------|  
|정수 계열 형식 표|임의의 정수 형식 또는 부동 소수점 형식이나 개체에 대한 포인터|  
|부동 소수점|산술 형식|  
|개체에 대한 포인터 또는 \(**void \***\)|임의의 정수 형식, \(**void \***\), 개체에 대한 포인터 또는 함수 포인터|  
|함수 포인터|임의의 정수 계열 형식, 개체에 대한 포인터 또는 함수 포인터|  
|구조체, 공용 구조체 또는 배열|없음|  
|void 형식|모든 형식|  
  
 모든 식별자를 `void` 형식으로 캐스팅할 수 있습니다.  그러나 형식 캐스트 식에 지정된 형식이 `void`가 아닌 경우 해당 형식으로 캐스팅되는 식별자가 `void` 식이 될 수 없습니다.  모든 식을 `void`로 캐스팅할 수 있지만 `void` 형식의 식은 다른 형식으로 캐스팅할 수 없습니다.  예를 들어, `void` 반환 형식이 포함된 함수의 반환 형식을 다른 형식으로 캐스팅할 수 없습니다.  
  
 **void \*** 식에는 `void` 형식이 아니라 `void`에 대한 형식 포인터가 있습니다.  개체가 `void` 형식으로 캐스팅되면 결과 식을 어떠한 항목에도 할당할 수 없습니다.  마찬가지로, 형식 캐스팅 개체가 허용 가능한 l\-value가 아니므로 형식 캐스팅 개체에 어떠한 항목도 할당할 수 없습니다.  
  
 **Microsoft 전용**  
  
 형식 캐스팅은 식별자의 크기가 변경되지 않는 한 l\-value 식이 될 수 있습니다.  l\-value 식에 대한 자세한 내용은 [L\-Value 및 R\-Value 식](../c-language/l-value-and-r-value-expressions.md)을 참조하십시오.  
  
 **Microsoft 전용 종료**  
  
 캐스팅을 사용하여 식을 `void` 형식으로 변환할 수 있지만 결과 식은 값이 필요하지 않은 위치에서만 사용할 수 있습니다.  **void \***로 변환되었다가 다시 원래 형식으로 변환된 개체 포인터는 해당 원래 값으로 되돌려집니다.  
  
## 참고 항목  
 [형식 변환](../c-language/type-conversions-c.md)