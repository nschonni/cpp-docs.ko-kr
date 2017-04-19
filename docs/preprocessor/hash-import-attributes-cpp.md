---
title: "#import 특성 (C++) | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
  - "C"
helpviewer_keywords: 
  - "#import 지시문, 특성"
ms.assetid: 2a5085e3-82ee-4f83-892b-0aa6cc13863b
caps.latest.revision: 7
caps.handback.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# #import 특성 (C++)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

\#import 지시문에 사용된 특성에 대한 링크를 제공합니다.  
  
 **Microsoft 전용**  
  
 다음 특성은 \#import 지시문에서 사용할 수 있습니다.  
  
|특성|설명|  
|--------|--------|  
|[auto\_rename](../preprocessor/auto-rename.md)|변수 이름에 잠재적인 이름 충돌을 해결하는 두 개의 밑줄\(\_\_\)을 추가하여 C\+\+ 예약어의 이름을 바꿉니다.|  
|[auto\_search](../preprocessor/auto-search.md)|형식 라이브러리를 \#import로 참조하고 형식 라이브러리 자체가 다른 형식 라이브러리를 참조할 때 컴파일러가 다른 형식 라이브러리에 대해 암시적 \#import를 수행할 수 있도록 지정합니다.|  
|[embedded\_idl](../preprocessor/embedded-idl.md)|특성에서 생성된 코드를 유지한 상태에서 형식 라이브러리가 .tlh 파일에 작성되도록 지정합니다.|  
|[Exclude](../preprocessor/exclude-hash-import.md)|생성되는 형식 라이브러리 헤더 파일에서 항목을 제외시킵니다.|  
|[high\_method\_prefix](../preprocessor/high-method-prefix.md)|상위 수준 속성과 메서드 명명에 사용될 접두사를 지정합니다.|  
|[high\_property\_prefixes](../preprocessor/high-property-prefixes.md)|세 가지 속성 메서드의 대체 접두사를 지정합니다.|  
|[implementation\_only](../preprocessor/implementation-only.md)|.tlh 헤더 파일\(기본 헤더 파일\)을 생성하지 않습니다.|  
|[include\(\)](../preprocessor/include-parens.md)|자동 제외를 사용하지 않도록 설정합니다.|  
|[inject\_statement](../preprocessor/inject-statement.md)|소스 텍스트로서 인수를 형식 라이브러리 헤더에 삽입합니다.|  
|[named\_guids](../preprocessor/named-guids.md)|이전 스타일의 GUID 변수를 **LIBID\_MyLib**, **CLSID\_MyCoClass**, **IID\_MyInterface** 및 **DIID\_MyDispInterface** 형식으로 정의하고 초기화하도록 컴파일러에 지시합니다.|  
|[no\_auto\_exclude](../preprocessor/no-auto-exclude.md)|자동 제외를 사용하지 않도록 설정합니다.|  
|[no\_dual\_interfaces](../preprocessor/no-dual-interfaces.md)|컴파일러가 이중 인터페이스 메서드에 대한 래퍼 함수를 생성하는 방법을 변경합니다.|  
|[no\_implementation](../preprocessor/no-implementation.md)|래퍼 멤버 함수의 구현이 포함된 .tli 헤더를 생성하지 않습니다.|  
|[no\_namespace](../preprocessor/no-namespace.md)|컴파일러가 생성하지 않은 네임스페이스 이름을 지정합니다.|  
|[no\_registry](../preprocessor/no-registry.md)|형식 라이브러리에 대한 레지스트리를 검색하지 않도록 컴파일러에 지시합니다.|  
|[no\_search\_namespace](../preprocessor/no-search-namespace.md)|[no\_namespace](../preprocessor/no-namespace.md) 특성과 동일한 기능을 갖지만, [auto\_search](../preprocessor/auto-search.md) 특성을 가진 \#import 지시문이 사용되는 형식 라이브러리에서 사용됩니다.|  
|[no\_smart\_pointers](../preprocessor/no-smart-pointers.md)|형식 라이브러리의 모든 인터페이스에 대한 스마트 포인터를 만들지 않습니다.|  
|[raw\_dispinterfaces](../preprocessor/raw-dispinterfaces.md)|**IDispatch::Invoke**를 호출하고 `HRESULT` 오류 코드를 반환하는 dispinterface 메서드 및 속성에 대해 하위 수준의 래퍼 함수를 생성하라고 컴파일러에 지시합니다.|  
|[raw\_interfaces\_only](../preprocessor/raw-interfaces-only.md)|오류 처리 래퍼 함수 및 해당 래퍼 함수를 사용하는 [속성](../cpp/property-cpp.md) 선언을 생성하지 않습니다.|  
|[raw\_method\_prefix](../preprocessor/raw-method-prefix.md)|이름 충돌을 방지하기 위해 다른 접두사를 지정합니다.|  
|[원시 네이티브 형식](../preprocessor/raw-native-types.md)|상위 수준의 래퍼 함수에서 COM 지원 클래스를 사용하지 않도록 설정하고 대신 하위 수준의 데이터 형식을 사용하도록 합니다.|  
|[raw\_property\_prefixes](../preprocessor/raw-property-prefixes.md)|세 가지 속성 메서드의 대체 접두사를 지정합니다.|  
|[이름 바꾸기](../preprocessor/rename-hash-import.md)|이름 충돌 문제 해결 작업|  
|[네임스페이스 이름 변경](../preprocessor/rename-namespace.md)|형식 라이브러리의 콘텐츠가 들어있는 네임스페이스의 이름을 바꿉니다.|  
|[rename\_search\_namespace](../preprocessor/rename-search-namespace.md)|[네임스페이스 이름 변경](../preprocessor/rename-namespace.md) 특성과 동일한 기능을 갖지만, [auto\_search](../preprocessor/auto-search.md) 특성을 가진 \#import 지시문이 사용되는 형식 라이브러리에서 사용됩니다.|  
|[tlbid](../preprocessor/tlbid.md)|기본 형식 라이브러리 이외의 라이브러리를 로드할 수 있도록 합니다.|  
  
 **Microsoft 전용 종료**  
  
## 참고 항목  
 [\#import 지시문](../preprocessor/hash-import-directive-cpp.md)