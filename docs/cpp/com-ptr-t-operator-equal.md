---
title: "_com_ptr_t::operator = | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
f1_keywords: 
  - "_com_ptr_t.operator="
  - "_com_ptr_t::operator="
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "= 연산자, 특정 Visual C++ 개체와 사용"
  - "operator =, 포인터"
  - "operator=, 포인터"
ms.assetid: 46849455-371c-4d0f-bae4-c1f737d2ca4a
caps.latest.revision: 6
caps.handback.revision: 6
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# _com_ptr_t::operator =
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

**Microsoft 전용**  
  
 기존 `_com_ptr_t` 개체에 새 값을 할당합니다.  
  
## 구문  
  
```  
  
      template<typename _OtherIID>   
_com_ptr_t& operator=(   
   const _com_ptr_t<_OtherIID>& p   
);  
  
// Sets a smart pointer to be a different smart pointer of a different   
// type or a different raw interface pointer. QueryInterface is called   
// to find an interface pointer of this smart pointer's type, and   
// Release is called to decrement the reference count for the previously   
// encapsulated pointer. If QueryInterface fails with an E_NOINTERFACE,   
// a NULL smart pointer results.  
template<typename _InterfaceType>   
_com_ptr_t& operator=(   
   _InterfaceType* p   
);  
  
// Encapsulates a raw interface pointer of this smart pointer's type.   
// AddRef is called to increment the reference count for the encapsulated  
// interface pointer, and Release is called to decrement the reference   
// count for the previously encapsulated pointer.  
template<> _com_ptr_t&    
operator=(   
   Interface* pInterface   
) throw();  
  
// Sets a smart pointer to be a copy of another instance of the same   
// smart pointer of the same type. AddRef is called to increment the   
// reference count for the encapsulated interface pointer, and Release   
// is called to decrement the reference count for the previously   
// encapsulated pointer.  
_com_ptr_t& operator=(   
   const _com_ptr_t& cp   
) throw();  
  
// Sets a smart pointer to NULL. The NULL argument must be a zero.  
_com_ptr_t& operator=(   
   int null   
);  
// Sets a smart pointer to be a _variant_t object. The encapsulated   
// VARIANT must be of type VT_DISPATCH or VT_UNKNOWN, or it can be   
// converted to one of these two types. If QueryInterface fails with an   
// E_NOINTERFACE error, a NULL smart pointer results.  
_com_ptr_t& operator=(   
   const _variant_t& varSrc   
);  
```  
  
## 설명  
 이 `_com_ptr_t` 개체에 인터페이스 포인터를 할당합니다.  
  
 **Microsoft 전용 종료**  
  
## 참고 항목  
 [\_com\_ptr\_t 클래스](../cpp/com-ptr-t-class.md)