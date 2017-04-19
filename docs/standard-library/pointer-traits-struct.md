---
title: "pointer_traits 구조체 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- memory/std::pointer_traits::element_type
- memory/std::pointer_traits::pointer
- memory/std::pointer_traits
- memory/std::pointer_traits::difference_type
- memory/std::pointer_traits::rebind
- xmemory0/std::pointer_traits::element_type
- xmemory0/std::pointer_traits::pointer
- xmemory0/std::pointer_traits
- xmemory0/std::pointer_traits::difference_type
- xmemory0/std::pointer_traits::rebind
dev_langs:
- C++
ms.assetid: 545aecf1-3561-4859-8b34-603c079fe1b3
caps.latest.revision: 13
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
translationtype: Machine Translation
ms.sourcegitcommit: a937c9d083a7e4331af63323a19fb207142604a0
ms.openlocfilehash: 3a5633fa4c9f45629d655edf922d40b02b68aaca
ms.lasthandoff: 02/24/2017

---
# <a name="pointertraits-struct"></a>pointer_traits 구조체
포인터 형식 `allocator_traits`를 사용하여 할당자를 설명하기 위해 템플릿 클래스 `Ptr`의 개체에 필요한 정보를 제공합니다.  
  
## <a name="syntax"></a>구문  
  
```cpp  
template <class Ptr>
struct pointer_traits;
```  
  
## <a name="remarks"></a>설명  
 Ptr은 `Ty *` 형식의 원시 포인터 또는 다음 속성을 포함하는 클래스일 수 있습니다.  
```  
struct Ptr
   { // describes a pointer type usable by allocators
   typedef Ptr pointer;
   typedef T1 element_type; // optional
   typedef T2 difference_type; // optional
   template <class Other>
   using rebind = typename Ptr<Other, Rest...>; // optional
   static pointer pointer_to(element_type& obj);
   // optional
   };  
```
### <a name="typedefs"></a>Typedefs  
  
|이름|설명|  
|----------|-----------------|  
|`typedef T2 difference_type`|`T2` 형식은 해당 형식이 있으면 `Ptr::difference_type`이고 그렇지 않으면 `ptrdiff_t`입니다. `Ptr`이 원시 포인터이면 형식은 `ptrdiff_t`입니다.|  
|`typedef T1 element_type`|`T1` 형식은 해당 형식이 있으면 `Ptr::element_type`이고 그렇지 않으면 `Ty`입니다. `Ptr`이 원시 포인터이면 형식은 `Ty`입니다.|  
|`typedef Ptr pointer`|형식은 `Ptr`입니다.|  
  
### <a name="structs"></a>Structs  
  
|이름|설명|  
|----------|-----------------|  
|`pointer_traits::rebind`|기본 포인터 형식을 지정된 형식으로 변환하려고 시도합니다.|  
  
### <a name="methods"></a>메서드  
  
|이름|설명|  
|----------|-----------------|  
|[pointer_to](#pointer_traits__pointer_to_method)|클래스 `Ptr`의 개체에 대한 임의 참조를 변환합니다.|  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<memory>  
  
 **네임스페이스:** std  
  
##  <a name="a-namepointertraitspointertomethoda--pointerto"></a><a name="pointer_traits__pointer_to_method"></a>  pointer_to  
 해당 함수가 있는 경우 `Ptr::pointer_to(obj)`를 반환하는 정적 메서드입니다. 그렇지 않으면 클래스 `Ptr`의 개체에 대한 임의 참조를 변환할 수 없습니다. `Ptr`이 원시 포인터이면 이 메서드는 `addressof(obj)`를 반환합니다.  
  
```cpp  
static pointer pointer_to(element_type& obj);
```  
  
## <a name="see-also"></a>참고 항목  
 [\<memory>](../standard-library/memory.md)   
 [allocator_traits 클래스](../standard-library/allocator-traits-class.md)

