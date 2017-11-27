---
title: "템플릿 및 이름 확인 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-language
ms.tgt_pltfrm: 
ms.topic: language-reference
dev_langs: C++
ms.assetid: 519ba7b5-cd25-4549-865a-9a7b9dffdc28
caps.latest.revision: "6"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 4013b35cf12fdc8b6c586a794df8340472584bc0
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/24/2017
---
# <a name="templates-and-name-resolution"></a>템플릿 및 이름 확인

템플릿 정의에는 3가지 형식의 이름이 있습니다.  
  
-   지역으로 선언된 이름(템플릿 자체의 이름과 템플릿 정의 내에 선언된 모든 이름 포함)  
  
-   템플릿 정의 바깥쪽 범위의 이름  
  
-   어떤 방식으로든 템플릿 인수에 종속되는 이름(종속 이름)  
  
 처음 두 이름은 클래스 및 함수 범위와 관련된 반면 종속 이름의 경우 복잡성을 처리하기 위해 템플릿 정의에 이름 확인을 위한 특별한 규칙이 요구됩니다. 이는 템플릿이 인스턴스화될 때까지 컴파일러가 이러한 이름에 대해 거의 알지 못하기 때문입니다. 이름의 형식은 사용되는 템플릿 인수에 따라 전혀 달라질 수 있습니다. 독립적 이름은 일반적인 규칙에 따라 템플릿 정의 시점에 조회됩니다. 템플릿 인수와는 별개인 이러한 이름은 모든 템플릿 특수화를 위해 한 번 조회됩니다. 종속 이름은 템플릿이 인스턴스화될 때까지 조회되지 않으며 각 특수화에 대해 개별적으로 조회됩니다.  
  
 형식은 템플릿 인수에 종속된 경우 종속적입니다. 특히 형식은 다음과 같은 경우 종속적입니다.  
  
-   템플릿 인수 자체임  
  
    ```cpp
    T  
    ```  
  
-   종속 형식을 포함하며 한정자를 사용하는 정규화된 이름임  
  
    ```cpp
    T::myType  
    ```  
  
-   정규화되지 않은 부분이 종속 형식을 식별하는 경우 정규화된 이름임  
  
    ```cpp
    N::T  
    ```  
  
-   기본 형식이 종속 형식인 const 또는 volatile 형식임  
  
    ```cpp
    const T  
    ```  
  
-   종속 형식 기반의 포인터, 참조, 배열 또는 함수 포인터 형식임  
  
    ```cpp
    T *, T &, T [10], T (*)()  
    ```  
  
-   크기가 템플릿 매개 변수를 기반으로 하는 배열임  
  
    ```cpp
    template <int arg> class X {  
    int x[arg] ; // dependent type  
    }  
    ```  
  
-   템플릿 매개 변수에서 생성된 템플릿 형식임  
  
    ```cpp
    T<int>, MyTemplate<T>  
    ```  
  
## <a name="type-dependence-and-value-dependence"></a>형식 종속성 및 값 종속성

 템플릿 매개 변수에 종속된 이름 및 식은 템플릿 매개 변수가 형식 매개 변수인지, 아니면 값 매개 변수인지에 따라 형식 종속 항목 또는 값 종속 항목으로 분류됩니다. 또한 템플릿 인수에 종속된 형식으로 템플릿에 선언된 모든 식별자는 값 종속 식으로 초기화된 정수 계열 또는 열거형 형식과 마찬가지로 값 종속 항목으로 간주됩니다.  
  
 형식 종속 및 값 종속 식은 형식 또는 값에 종속되는 변수가 포함된 식입니다. 이러한 식의 의미 체계는 템플릿에 사용되는 매개 변수에 따라 달라질 수 있습니다.  
  
## <a name="see-also"></a>참고 항목

 [템플릿](../cpp/templates-cpp.md)