---
title: "컴파일러 오류 C3488 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3488
dev_langs:
- C++
helpviewer_keywords:
- C3488
ms.assetid: 0a6fcd76-dd3b-48d7-abb3-22eccda96034
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
ms.openlocfilehash: 6c7f36a63d5922672e89faf0c7d73c95100b256d
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3488"></a>컴파일러 오류 C3488
기본 캡처 모드가 참조 방식인 경우 'var'을 사용할 수 없습니다.  
  
 람다 식에 대한 기본 캡처 모드를 참조 방식으로 지정할 경우 해당 식의 캡처 절에 변수를 참조로 전달할 수 없습니다.  
  
### <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
-   변수를 캡처 절에 명시적으로 전달하지 마세요. 또는  
  
-   참조 방식을 기본 캡처 모드로 지정하지 마세요. 또는  
  
-   값 방식을 기본 캡처 모드로 지정합니다. 또는  
  
-   변수를 캡처 절에 값으로 전달합니다. 이 경우 람다 식의 동작이 변경될 수 있습니다.  
  
## <a name="example"></a>예제  
 다음 예제에서는 기본 모드가 참조 방식인 람다 식의 캡처 절에 `n` 변수에 대한 참조가 나타나기 때문에 C3488을 생성합니다.  
  
```  
// C3488a.cpp  
  
int main()  
{  
   int n = 5;  
   [&, &n]() { return n; } (); // C3488  
}  
```  
  
## <a name="example"></a>예제  
 다음 예제에서는 C3488에 대한 네 가지 해결 방법을 보여 줍니다.  
  
```  
// C3488b.cpp  
  
int main()  
{  
   int n = 5;  
  
   // Possible resolution 1:  
   // Do not explicitly pass &n to the capture clause.  
   [&]() { return n; } ();  
  
   // Possible resolution 2:  
   // Do not specify by-reference as the default capture mode.  
   [&n]() { return n; } ();  
  
   // Possible resolution 3:  
   // Specify by-value as the default capture mode.  
   [=, &n]() { return n; } ();  
  
   // Possible resolution 4:  
   // Pass n by value to the capture clause.  
   [n]() { return n; } ();  
}  
```  
  
## <a name="see-also"></a>참고 항목  
 [람다 식](../../cpp/lambda-expressions-in-cpp.md)