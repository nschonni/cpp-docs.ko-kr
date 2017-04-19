---
title: "network_link_registry 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- network_link_registry
- AGENTS/concurrency::network_link_registry
- AGENTS/concurrency::network_link_registry::add
- AGENTS/concurrency::network_link_registry::begin
- AGENTS/concurrency::network_link_registry::contains
- AGENTS/concurrency::network_link_registry::count
- AGENTS/concurrency::network_link_registry::remove
dev_langs:
- C++
helpviewer_keywords:
- network_link_registry class
ms.assetid: 3e7b4097-09f1-4252-964e-b15b8f7f7fc6
caps.latest.revision: 20
author: mikeblome
ms.author: mblome
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
ms.sourcegitcommit: 5faef5bd1be6cc02d6614a6f6193c74167a8ff23
ms.openlocfilehash: 28c13f1e2bf80624da3a7aba441944c051790d27
ms.lasthandoff: 03/17/2017

---
# <a name="networklinkregistry-class"></a>network_link_registry 클래스
`network_link_registry` 추상 기본 클래스는 소스 및 대상 블록 간의 연결을 관리합니다.  
  
## <a name="syntax"></a>구문  
  
```
template<class _Block>
class network_link_registry;
```  
  
#### <a name="parameters"></a>매개 변수  
 `_Block`  
 블록 데이터 형식에 저장 되는 `network_link_registry`합니다.  
  
## <a name="members"></a>멤버  
  
### <a name="public-typedefs"></a>공용 Typedefs  
  
|이름|설명|  
|----------|-----------------|  
|`const_pointer`|에 대 한 포인터를 제공 하는 형식은 `const` 요소에는 `network_link_registry` 개체입니다.|  
|`const_reference`|에 대 한 참조를 제공 하는 형식은 `const` 에 저장 된 요소는 `network_link_registry` 읽고 const 작업을 수행 하기 위해 개체입니다.|  
|`iterator`|반복기를 제공 하는 형식 읽거나에 있는 모든 요소를 수정할 수는 `network_link_registry` 개체입니다.|  
|`type`|에 저장 된 블록 형식을 나타내는 형식입니다는 `network_link_registry` 개체입니다.|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[add](#add)|파생된 클래스에서 재정의 되 면 추가에 대 한 링크는 `network_link_registry` 개체입니다.|  
|[begin](#begin)|파생된 클래스에서 재정의 되 면 첫 번째 요소에 반복기를 반환 된 `network_link_registry` 개체입니다.|  
|[포함](#contains)|파생된 클래스에서 재정의 되 면 검색 된 `network_link_registry` 지정된 된 블록에 대 한 개체입니다.|  
|[count](#count)|파생된 클래스에서 재정의 되 면에 있는 항목의 수를 반환 된 `network_link_registry` 개체입니다.|  
|[remove](#remove)|파생된 클래스에서 재정의 되 면 제거에서 지정된 된 블록은 `network_link_registry` 개체입니다.|  
  
## <a name="remarks"></a>주의  
 `network link registry` 동시 액세스에 대 한 안전 하지 않습니다.  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 `network_link_registry`  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** agents.h  
  
 **네임스페이스:** 동시성  
  
##  <a name="add"></a>추가 

 파생된 클래스에서 재정의 되 면 추가에 대 한 링크는 `network_link_registry` 개체입니다.  
  
```
virtual void add(_EType _Link) = 0;
```  
  
### <a name="parameters"></a>매개 변수  
 `_Link`  
 추가할 블록에 대 한 포인터입니다.  
  
##  <a name="begin"></a>시작 

 파생된 클래스에서 재정의 되 면 첫 번째 요소에 반복기를 반환 된 `network_link_registry` 개체입니다.  
  
```
virtual iterator begin() = 0;
```  
  
### <a name="return-value"></a>반환 값  
 첫 번째 요소를 주소 지정 하는 반복기는 `network_link_registry` 개체입니다.  
  
### <a name="remarks"></a>주의  
 반복기의 최종 상태도 표시 됩니다는 `NULL` 링크 합니다.  
  
##  <a name="contains"></a>포함 

 파생된 클래스에서 재정의 되 면 검색 된 `network_link_registry` 지정된 된 블록에 대 한 개체입니다.  
  
```
virtual bool contains(_EType _Link) = 0;
```  
  
### <a name="parameters"></a>매개 변수  
 `_Link`  
 에 대 한 검색 되는 블록에 대 한 포인터는 `network_link_registry` 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 `true`블록이 없으면 `false` 그렇지 않은 경우.  
  
##  <a name="count"></a>개수 

 파생된 클래스에서 재정의 되 면에 있는 항목의 수를 반환 된 `network_link_registry` 개체입니다.  
  
```
virtual size_t count() = 0;
```  
  
### <a name="return-value"></a>반환 값  
 항목 수는 `network_link_registry` 개체입니다.  
  
##  <a name="remove"></a>제거 

 파생된 클래스에서 재정의 되 면 제거에서 지정된 된 블록은 `network_link_registry` 개체입니다.  
  
```
virtual bool remove(_EType _Link) = 0;
```  
  
### <a name="parameters"></a>매개 변수  
 `_Link`  
 제거 될 경우 블록에 대 한 포인터를 찾을 수 있습니다.  
  
### <a name="return-value"></a>반환 값  
 `true`링크를 찾아 제거 했으면 `false` 그렇지 않은 경우.  
  
## <a name="see-also"></a>참고 항목  
 [Namespace 동시성](concurrency-namespace.md)   
 [single_link_registry 클래스](single-link-registry-class.md)   
 [multi_link_registry 클래스](multi-link-registry-class.md)
