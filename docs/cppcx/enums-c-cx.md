---
title: "열거형(C++/CX) | Microsoft Docs"
ms.custom: ""
ms.date: "12/30/2016"
ms.prod: "windows-client-threshold"
ms.technology: ""
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 99fbbe28-c1cd-43af-9ead-60f90eba6e68
caps.latest.revision: 14
author: "ghogen"
ms.author: "ghogen"
manager: "ghogen"
caps.handback.revision: 14
---
# 열거형(C++/CX)
[!INCLUDE[cppwrt_short](../cppcx/includes/cppwrt-short-md.md)]는 표준 C\+\+ `public enum class`과 유사한 `scoped  enum` 키워드를 지원합니다.`public enum class` 키워드를 사용하여 선언된 열거자를 사용할 경우 열거형 식별자를 사용하여 각 열거자 값의 범위를 지정해야 합니다.  
  
## 설명  
 `public enum class`과 같은 액세스 지정자가 없는 `public`는 표준 C\+\+ [범위 지정 열거형](~/cpp/enumerations-cpp.md)으로 처리됩니다.  
  
 `public enum class` 자체에서는 플래그 열거형 형식이 int32 또는 uint32여야 하지만 `public enum struct` 또는 [!INCLUDE[wrt](../cppcx/includes/wrt-md.md)] 선언은 내부 형식이 모든 정수 계열 형식일 수 있습니다. 다음 구문에서는 `public enum class` 또는 `public enum struct` 부분을 설명합니다. 자세한 내용은 [enum class](~/windows/enum-class-cpp-component-extensions.md)을 참조하세요.  
  
 이 예제에서는 public enum 클래스를 정의하는 방법을 보여 줍니다.  
  
 [!code-cpp[cx_enums#01](../snippets/cpp/VS_Snippets_Misc/cx_enums/cpp/class1.h#01)]  
  
 다음 예제에서는 클래스를 사용하는 방법을 보여 줍니다.  
  
 [!code-cpp[cx_enums#02](../snippets/cpp/VS_Snippets_Misc/cx_enums/cpp/class1.h#02)]  
  
## 예제  
 다음 예제에서는 열거형을 선언하는 방법을 보여 줍니다.  
  
 [!code-cpp[cx_enums#03](../snippets/cpp/VS_Snippets_Misc/cx_enums/cpp/class1.h#03)]  
  
 다음 예제에서는 해당 숫자로 캐스팅하고 비교를 수행하는 방법을 보여 줍니다. 열거자 `One`의 사용은 `Enum1` 열거형 식별자로 범위가 지정되고, 열거자 `First`는 `Enum2`로 범위가 지정됩니다.  
  
 [!code-cpp[cx_enums#04](../snippets/cpp/VS_Snippets_Misc/cx_enums/cpp/class1.h#04)]  
  
## 참고 항목  
 [형식 시스템](../cppcx/type-system-c-cx.md)   
 [Visual C\+\+ 언어 참조](../cppcx/visual-c-language-reference-c-cx.md)   
 [네임스페이스 참조](../cppcx/namespaces-reference-c-cx.md)