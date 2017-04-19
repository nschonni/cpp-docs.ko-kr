---
title: "unordered_multiset 클래스 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- unordered_multiset
- std::unordered_multiset
- unordered_set/std::unordered_multiset
- std::unordered_multiset::allocator_type
- unordered_set/std::unordered_multiset::allocator_type
- std::unordered_multiset::const_iterator
- unordered_set/std::unordered_multiset::const_iterator
- std::unordered_multiset::const_local_iterator
- unordered_set/std::unordered_multiset::const_local_iterator
- std::unordered_multiset::const_pointer
- unordered_set/std::unordered_multiset::const_pointer
- std::unordered_multiset::const_reference
- unordered_set/std::unordered_multiset::const_reference
- std::unordered_multiset::difference_type
- unordered_set/std::unordered_multiset::difference_type
- std::unordered_multiset::hasher
- unordered_set/std::unordered_multiset::hasher
- std::unordered_multiset::iterator
- unordered_set/std::unordered_multiset::iterator
- std::unordered_multiset::key_equal
- unordered_set/std::unordered_multiset::key_equal
- std::unordered_multiset::key_type
- unordered_set/std::unordered_multiset::key_type
- std::unordered_multiset::local_iterator
- unordered_set/std::unordered_multiset::local_iterator
- std::unordered_multiset::pointer
- unordered_set/std::unordered_multiset::pointer
- std::unordered_multiset::reference
- unordered_set/std::unordered_multiset::reference
- std::unordered_multiset::size_type
- unordered_set/std::unordered_multiset::size_type
- std::unordered_multiset::value_type
- unordered_set/std::unordered_multiset::value_type
- std::unordered_multiset::begin
- unordered_set/std::unordered_multiset::begin
- std::unordered_multiset::bucket
- unordered_set/std::unordered_multiset::bucket
- std::unordered_multiset::bucket_count
- unordered_set/std::unordered_multiset::bucket_count
- std::unordered_multiset::bucket_size
- unordered_set/std::unordered_multiset::bucket_size
- std::unordered_multiset::cbegin
- unordered_set/std::unordered_multiset::cbegin
- std::unordered_multiset::cend
- unordered_set/std::unordered_multiset::cend
- std::unordered_multiset::clear
- unordered_set/std::unordered_multiset::clear
- std::unordered_multiset::count
- unordered_set/std::unordered_multiset::count
- std::unordered_multiset::emplace
- unordered_set/std::unordered_multiset::emplace
- std::unordered_multiset::emplace_hint
- unordered_set/std::unordered_multiset::emplace_hint
- std::unordered_multiset::empty
- unordered_set/std::unordered_multiset::empty
- std::unordered_multiset::end
- unordered_set/std::unordered_multiset::end
- std::unordered_multiset::equal_range
- unordered_set/std::unordered_multiset::equal_range
- std::unordered_multiset::erase
- unordered_set/std::unordered_multiset::erase
- std::unordered_multiset::find
- unordered_set/std::unordered_multiset::find
- std::unordered_multiset::get_allocator
- unordered_set/std::unordered_multiset::get_allocator
- std::unordered_multiset::hash_function
- unordered_set/std::unordered_multiset::hash_function
- std::unordered_multiset::insert
- unordered_set/std::unordered_multiset::insert
- std::unordered_multiset::key_eq
- unordered_set/std::unordered_multiset::key_eq
- std::unordered_multiset::load_factor
- unordered_set/std::unordered_multiset::load_factor
- std::unordered_multiset::max_bucket_count
- unordered_set/std::unordered_multiset::max_bucket_count
- std::unordered_multiset::max_load_factor
- unordered_set/std::unordered_multiset::max_load_factor
- std::unordered_multiset::max_size
- unordered_set/std::unordered_multiset::max_size
- std::unordered_multiset::rehash
- unordered_set/std::unordered_multiset::rehash
- std::unordered_multiset::size
- unordered_set/std::unordered_multiset::size
- std::unordered_multiset::swap
- unordered_set/std::unordered_multiset::swap
- std::unordered_multiset::unordered_multiset
- unordered_set/std::unordered_multiset::unordered_multiset
- std::unordered_multiset::operator=
- unordered_set/std::unordered_multiset::operator=
dev_langs:
- C++
helpviewer_keywords:
- unordered_multiset class
ms.assetid: 70c8dfc5-492a-4af2-84f5-1aa9cb04b71c
caps.latest.revision: 24
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
ms.openlocfilehash: cae7184dd2d0e241ee13e6867897e4699d7d56a1
ms.lasthandoff: 02/24/2017

---
# <a name="unorderedmultiset-class"></a>unordered_multiset 클래스
템플릿 클래스는 `const Key` 형식의 다양한 길이의 요소 시퀀스를 제어하는 개체를 설명합니다. 시퀀스는 해시 함수로 약하게 정렬됩니다. 즉, 시퀀스를 버킷이라고 하는 하위 시퀀스의 정렬된 집합으로 분할합니다. 비교 함수는 각 버킷 내에서 요소 쌍이 동일하게 정렬되었는지 여부를 확인합니다. 각 요소는 정렬 키와 값으로 사용됩니다. 시퀀스는 최소한 모든 버킷이 대략 동일한 크기일 경우 시퀀스의 요소 수와 상관없이 작업 수를 사용하여 임의 요소를 조회, 삽입, 제거하는 방식으로 나타냅니다(일정 시간). 모든 요소가 하나의 버킷에 있는 최악의 경우에는 작업 수가 시퀀스의 요소 수에 비례합니다(선형 시간). 또한, 요소를 삽입할 경우 어떤 반복기도 무효화되지 않으며, 요소를 제거할 경우 제거된 요소를 가리키고 있는 반복기만 무효화됩니다.  
  
## <a name="syntax"></a>구문  
  
```  
template <class Key,  
    class Hash = std::hash<Key>,  
    class Pred = std::equal_to<Key>,  
    class Alloc = std::allocator<Key>>  
class unordered_multiset;  
```  
  
#### <a name="parameters"></a>매개 변수  
  
|||  
|-|-|  
|매개 변수|설명|  
|`Key`|키 형식입니다.|  
|`Hash`|해시 함수 개체 형식입니다.|  
|`Pred`|같음 비교 함수 개체 형식입니다.|  
|`Alloc`|할당자 클래스입니다.|  
  
## <a name="members"></a>멤버  
  
|||  
|-|-|  
|형식 정의|설명|  
|[unordered_multiset::allocator_type](#unordered_multiset__allocator_type)|저장소 관리를 위한 할당자의 형식입니다.|  
|[unordered_multiset::const_iterator](#unordered_multiset__const_iterator)|제어되는 시퀀스에 대한 상수 반복기의 형식입니다.|  
|[unordered_multiset::const_local_iterator](#unordered_multiset__const_local_iterator)|제어되는 시퀀스에 대한 상수 버킷 반복기의 형식입니다.|  
|[unordered_multiset::const_pointer](#unordered_multiset__const_pointer)|요소에 대한 상수 포인터의 형식입니다.|  
|[unordered_multiset::const_reference](#unordered_multiset__const_reference)|요소에 대한 상수 참조의 형식입니다.|  
|[unordered_multiset::difference_type](#unordered_multiset__difference_type)|두 요소 사이의 부호가 있는 거리의 형식입니다.|  
|[unordered_multiset::hasher](#unordered_multiset__hasher)|해시 함수의 형식입니다.|  
|[unordered_multiset::iterator](#unordered_multiset__iterator)|제어되는 시퀀스에 대한 반복기의 형식입니다.|  
|[unordered_multiset::key_equal](#unordered_multiset__key_equal)|비교 함수의 형식입니다.|  
|[unordered_multiset::key_type](#unordered_multiset__key_type)|정렬 키의 형식입니다.|  
|[unordered_multiset::local_iterator](#unordered_multiset__local_iterator)|제어되는 시퀀스에 대한 버킷 반복기의 형식입니다.|  
|[unordered_multiset::pointer](#unordered_multiset__pointer)|요소에 대한 포인터의 형식입니다.|  
|[unordered_multiset::reference](#unordered_multiset__reference)|요소에 대한 참조의 형식입니다.|  
|[unordered_multiset::size_type](#unordered_multiset__size_type)|두 요소 사이의 부호가 없는 거리의 형식입니다.|  
|[unordered_multiset::value_type](#unordered_multiset__value_type)|요소의 형식입니다.|  
  
|||  
|-|-|  
|멤버 함수|설명|  
|[unordered_multiset::begin](#unordered_multiset__begin)|제어되는 시퀀스의 시작을 지정합니다.|  
|[unordered_multiset::bucket](#unordered_multiset__bucket)|키 값에 대한 버킷 개수를 가져옵니다.|  
|[unordered_multiset::bucket_count](#unordered_multiset__bucket_count)|버킷 개수를 가져옵니다.|  
|[unordered_multiset::bucket_size](#unordered_multiset__bucket_size)|버킷의 크기를 가져옵니다.|  
|[unordered_multiset::cbegin](#unordered_multiset__cbegin)|제어되는 시퀀스의 시작을 지정합니다.|  
|[unordered_multiset::cend](#unordered_multiset__cend)|제어되는 시퀀스의 끝을 지정합니다.|  
|[unordered_multiset::clear](#unordered_multiset__clear)|모든 요소를 제거합니다.|  
|[unordered_multiset::count](#unordered_multiset__count)|지정한 키와 일치하는 요소의 수를 찾습니다.|  
|[unordered_multiset::emplace](#unordered_multiset__emplace)|생성된 요소를 추가합니다.|  
|[unordered_multiset::emplace_hint](#unordered_multiset__emplace_hint)|힌트와 함께 생성된 요소를 추가합니다.|  
|[unordered_multiset::empty](#unordered_multiset__empty)|요소가 있는지 여부를 테스트합니다.|  
|[unordered_multiset::end](#unordered_multiset__end)|제어되는 시퀀스의 끝을 지정합니다.|  
|[unordered_multiset::equal_range](#unordered_multiset__equal_range)|지정된 키와 일치하는 범위를 찾습니다.|  
|[unordered_multiset::erase](#unordered_multiset__erase)|지정된 위치에 있는 요소를 제거합니다.|  
|[unordered_multiset::find](#unordered_multiset__find)|지정된 키와 일치하는 요소를 찾습니다.|  
|[unordered_multiset::get_allocator](#unordered_multiset__get_allocator)|저장된 할당자 개체를 가져옵니다.|  
|[unordered_multiset::hash_function](#unordered_multiset__hash_function)|저장된 해시 함수 개체를 가져옵니다.|  
|[unordered_multiset::insert](#unordered_multiset__insert)|요소를 추가합니다.|  
|[unordered_multiset::key_eq](#unordered_multiset__key_eq)|저장된 비교 함수 개체를 가져옵니다.|  
|[unordered_multiset::load_factor](#unordered_multiset__load_factor)|버킷당 평균 요소 수를 계산합니다.|  
|[unordered_multiset::max_bucket_count](#unordered_multiset__max_bucket_count)|최대 버킷 개수를 가져옵니다.|  
|[unordered_multiset::max_load_factor](#unordered_multiset__max_load_factor)|버킷당 최대 요소 수를 가져오거나 설정합니다.|  
|[unordered_multiset::max_size](#unordered_multiset__max_size)|제어되는 시퀀스의 최대 크기를 가져옵니다.|  
|[unordered_multiset::rehash](#unordered_multiset__rehash)|해시 테이블을 다시 빌드합니다.|  
|[unordered_multiset::size](#unordered_multiset__size)|요소 수를 계산합니다.|  
|[unordered_multiset::swap](#unordered_multiset__swap)|두 컨테이너의 내용을 바꿉니다.|  
|[unordered_multiset::unordered_multiset](#unordered_multiset__unordered_multiset)|컨테이너 개체를 만듭니다.|  
  
|||  
|-|-|  
|연산자|설명|  
|[unordered_multiset::operator=](#unordered_multiset__operator_eq)|해시 테이블을 복사합니다.|  
  
## <a name="remarks"></a>설명  
 개체는 저장된 두 개체, [unordered_multiset::key_equal](#unordered_multiset__key_equal) 형식의 비교 함수 개체, [unordered_multiset::hasher](#unordered_multiset__hasher) 형식의 해시 함수 개체를 호출하여 제어하는 시퀀스를 정렬합니다. 첫 번째 저장된 개체는 구성원 함수 [unordered_multiset::key_eq](#unordered_multiset__key_eq)`()`를 호출하여 액세스하며, 두 번째 저장된 개체는 구성원 함수 [unordered_multiset::hash_function](#unordered_multiset__hash_function)`()`을 호출하여 액세스합니다. 특히 `X` 형식의 모든 값 `Y` 및 `Key`의 경우 두 인수 값이 순서 지정이 동일할 경우 호출 `key_eq()(X, Y)`에서 true를 반환하며, 호출 `hash_function()(keyval)`은 형식 `size_t`의 값 분포를 생성합니다. 템플릿 클래스 [unordered_set 클래스](../standard-library/unordered-set-class.md)와 달리, 템플릿 클래스 `unordered_multiset`의 개체는 `key_eq()(X, Y)`가 제어된 시퀀스의 두 요소에 대해 항상 false라는 점에 대해 보장하지 않습니다. (키는 고유할 필요가 없습니다.)  
  
 개체는 또한 최대 로드 비율(버킷당 최대 평균 요소 수를 원하는 대로 지정)를 저장합니다. 요소를 삽입할 때 [unordered_multiset::load_factor](#unordered_multiset__load_factor)`()`에서 최대 로드 비율이 초과될 경우 컨테이너는 버킷 수를 증가시키고 필요에 따라 해시 테이블을 다시 빌드합니다.  
  
 제어된 시퀀스의 실제 요소 순서는 해시 함수, 비교 함수, 삽입 순서, 최대 로드 비율, 현재 버킷 수에 따라 달라집니다. 제어된 시퀀스의 요소 순서는 일반적으로 예측할 수 없습니다. 하지만 동일하게 정렬된 요소의 하위 집합은 제어된 시퀀스에서 항상 인접해 있습니다.  
  
 개체는 [unordered_multiset::allocator_type](#unordered_multiset__allocator_type) 형식의 저장된 할당자 개체를 통해 제어하는 시퀀스에 대한 저장소를 할당하고 해제합니다. 그러한 할당자 개체는 템플릿 클래스 `allocator`의 개체와 같은 외부 인터페이스가 있어야 합니다. 컨테이너 개체를 할당하는 경우 저장된 할당자 개체는 복사되지 않습니다.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<unordered_set>  
  
 **네임스페이스:** std  
  
##  <a name="a-nameunorderedmultisetallocatortypea--unorderedmultisetallocatortype"></a><a name="unordered_multiset__allocator_type"></a>  unordered_multiset::allocator_type  
 저장소 관리를 위한 할당자의 형식입니다.  
  
```  
typedef Alloc allocator_type;  
```  
  
### <a name="remarks"></a>설명  
 이 형식은 템플릿 매개 변수 `Alloc`의 동의어입니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_allocator_type.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
typedef std::allocator<std::pair<const char, int> > Myalloc;   
int main()   
    {   
    Myset c1;   
  
    Myset::allocator_type al = c1.get_allocator();   
    std::cout << "al == std::allocator() is "   
        << std::boolalpha << (al == Myalloc()) << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
al == std::allocator() is true  
```  
  
##  <a name="a-nameunorderedmultisetbegina--unorderedmultisetbegin"></a><a name="unordered_multiset__begin"></a>  unordered_multiset::begin  
 제어되는 시퀀스 또는 버킷의 시작을 지정합니다.  
  
```  
iterator begin();

const_iterator begin() const;

 
local_iterator begin(size_type nbucket);

const_local_iterator begin(size_type nbucket) const;
```  
  
### <a name="parameters"></a>매개 변수  
  
|||  
|-|-|  
|매개 변수|설명|  
|`nbucket`|버킷 번호입니다.|  
  
### <a name="remarks"></a>설명  
 처음 두 개의 멤버 함수는 시퀀스의 첫 번째 요소(또는 빈 시퀀스의 끝 바로 다음)를 가리키는 정방향 반복기를 반환합니다. 마지막 두 개의 멤버 함수는 버킷 `nbucket` 의 첫 번째 요소(또는 빈 버킷의 끝 바로 다음)를 가리키는 정방향 반복기를 반환합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_begin.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
// inspect first two items " [c] [b]"   
    Myset::iterator it2 = c1.begin();   
    std::cout << " [" << *it2 << "]";   
    ++it2;   
    std::cout << " [" << *it2 << "]";   
    std::cout << std::endl;   
  
// inspect bucket containing 'a'   
    Myset::const_local_iterator lit = c1.begin(c1.bucket('a'));   
    std::cout << " [" << *lit << "]";   
  
    return (0);   
    }  
  
```  
  
```Output  
[c] [b] [a]  
[c] [b]  
[a]  
```  
  
##  <a name="a-nameunorderedmultisetbucketa--unorderedmultisetbucket"></a><a name="unordered_multiset__bucket"></a>  unordered_multiset::bucket  
 키 값에 대한 버킷 개수를 가져옵니다.  
  
```  
size_type bucket(const Key& keyval) const;
```  
  
### <a name="parameters"></a>매개 변수  
 keyval  
 매핑할 키 값입니다.  
  
### <a name="remarks"></a>설명  
 멤버 함수는 현재 키 값 `keyval`에 해당하는 버킷 번호를 반환합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_bucket.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
// display buckets for keys   
    Myset::size_type bs = c1.bucket('a');   
    std::cout << "bucket('a') == " << bs << std::endl;   
    std::cout << "bucket_size(" << bs << ") == " << c1.bucket_size(bs)   
        << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
 [c] [b] [a]  
bucket('a') == 7  
bucket_size(7) == 1  
```  
  
##  <a name="a-nameunorderedmultisetbucketcounta--unorderedmultisetbucketcount"></a><a name="unordered_multiset__bucket_count"></a>  unordered_multiset::bucket_count  
 버킷 개수를 가져옵니다.  
  
```  
size_type bucket_count() const;
```  
  
### <a name="remarks"></a>설명  
 멤버 함수는 현재 버킷 수를 반환합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_bucket_count.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
// inspect current parameters   
    std::cout << "bucket_count() == " << c1.bucket_count() << std::endl;   
    std::cout << "load_factor() == " << c1.load_factor() << std::endl;   
    std::cout << "max_bucket_count() == "   
        << c1.max_bucket_count() << std::endl;   
    std::cout << "max_load_factor() == "   
        << c1.max_load_factor() << std::endl;   
    std::cout << std::endl;   
  
// change max_load_factor and redisplay   
    c1.max_load_factor(0.10f);   
    std::cout << "bucket_count() == " << c1.bucket_count() << std::endl;   
    std::cout << "load_factor() == " << c1.load_factor() << std::endl;   
    std::cout << "max_bucket_count() == "   
        << c1.max_bucket_count() << std::endl;   
    std::cout << "max_load_factor() == "   
        << c1.max_load_factor() << std::endl;   
    std::cout << std::endl;   
  
// rehash and redisplay   
    c1.rehash(100);   
    std::cout << "bucket_count() == " << c1.bucket_count() << std::endl;   
    std::cout << "load_factor() == " << c1.load_factor() << std::endl;   
    std::cout << "max_bucket_count() == "   
        << c1.max_bucket_count() << std::endl;   
    std::cout << "max_load_factor() == "   
        << c1.max_load_factor() << std::endl;   
    std::cout << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
 [c] [b] [a]  
bucket_count() == 8  
load_factor() == 0.375  
max_bucket_count() == 8  
max_load_factor() == 4  
  
bucket_count() == 8  
load_factor() == 0.375  
max_bucket_count() == 8  
max_load_factor() == 0.1  
  
bucket_count() == 128  
load_factor() == 0.0234375  
max_bucket_count() == 128  
max_load_factor() == 0.1  
  
```  
  
##  <a name="a-nameunorderedmultisetbucketsizea--unorderedmultisetbucketsize"></a><a name="unordered_multiset__bucket_size"></a>  unordered_multiset::bucket_size  
 버킷의 크기를 가져옵니다.  
  
```  
size_type bucket_size(size_type nbucket) const;
```  
  
### <a name="parameters"></a>매개 변수  
 `nbucket`  
 버킷 번호입니다.  
  
### <a name="remarks"></a>설명  
 멤버 함수는 버킷 번호 `nbucket`의 크기를 반환합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_bucket_size.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
// display buckets for keys   
    Myset::size_type bs = c1.bucket('a');   
    std::cout << "bucket('a') == " << bs << std::endl;   
    std::cout << "bucket_size(" << bs << ") == " << c1.bucket_size(bs)   
        << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
 [c] [b] [a]  
bucket('a') == 7  
bucket_size(7) == 1  
```  
  
##  <a name="a-nameunorderedmultisetcbegina--unorderedmultisetcbegin"></a><a name="unordered_multiset__cbegin"></a>  unordered_multiset::cbegin  
 범위의 첫 번째 요소를 주소 지정하는 `const` 반복기를 반환합니다.  
  
```  
const_iterator cbegin() const;
```  
  
### <a name="return-value"></a>반환 값  
 범위의 첫 번째 요소 또는 빈 범위의 끝 바로 다음 위치를 가리키는 `const` 정방향 액세스 반복기입니다(빈 범위의 경우 `cbegin() == cend()`).  
  
### <a name="remarks"></a>설명  
 `cbegin` 반환 값을 사용하여 범위의 요소를 수정할 수 없습니다.  
  
 `begin()` 멤버 함수 대신 이 멤버 함수를 사용하여 반환 값이 `const_iterator`임을 보장할 수 있습니다. 일반적으로 다음 예제와 같이 [auto](../cpp/auto-cpp.md) 형식 추론 키워드와 함께 사용합니다. 이 예제에서는 `Container`가 `begin()` 및 `cbegin()`을 지원하는 수정 가능(비`const`) 컨테이너라고 가정합니다.  
  
```cpp  
auto i1 = Container.begin();
// i1 is Container<T>::iterator   
auto i2 = Container.cbegin();

// i2 is Container<T>::const_iterator  
```  
  
##  <a name="a-nameunorderedmultisetcenda--unorderedmultisetcend"></a><a name="unordered_multiset__cend"></a>  unordered_multiset::cend  
 범위에서 마지막 요소 바로 다음의 위치를 주소 지정하는 `const` 반복기를 반환합니다.  
  
```  
const_iterator cend() const;
```  
  
### <a name="return-value"></a>반환 값  
 범위 끝의 바로 다음을 가리키는 `const` 정방향 액세스 반복기입니다.  
  
### <a name="remarks"></a>설명  
 `cend`는 반복기가 범위 끝을 통과했는지 여부를 테스트하는 데 사용됩니다.  
  
 `end()` 멤버 함수 대신 이 멤버 함수를 사용하여 반환 값이 `const_iterator`임을 보장할 수 있습니다. 일반적으로 다음 예제와 같이 [auto](../cpp/auto-cpp.md) 형식 추론 키워드와 함께 사용합니다. 이 예제에서는 `Container`가 `end()` 및 `cend()`를 지원하는 수정 가능(비`const`)한 컨테이너로 가정합니다.  
  
```cpp  
auto i1 = Container.end();
// i1 is Container<T>::iterator   
auto i2 = Container.cend();

// i2 is Container<T>::const_iterator  
```  
  
 `cend`에서 반환한 값은 역참조되지 않아야 합니다.  
  
##  <a name="a-nameunorderedmultisetcleara--unorderedmultisetclear"></a><a name="unordered_multiset__clear"></a>  unordered_multiset::clear  
 모든 요소를 제거합니다.  
  
```  
void clear();
```  
  
### <a name="remarks"></a>설명  
 구성원 함수는 [unordered_multiset::erase](#unordered_multiset__erase)`(` [unordered_multiset::begin](#unordered_multiset__begin)`(),` [unordered_multiset::end](#unordered_multiset__end)`())`를 호출합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_clear.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
// clear the container and reinspect   
    c1.clear();   
    std::cout << "size == " << c1.size() << std::endl;   
    std::cout << "empty() == " << std::boolalpha << c1.empty() << std::endl;   
    std::cout << std::endl;   
  
    c1.insert('d');   
    c1.insert('e');   
  
// display contents " [e] [d]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
    std::cout << "size == " << c1.size() << std::endl;   
    std::cout << "empty() == " << std::boolalpha << c1.empty() << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
 [c] [b] [a]  
size == 0  
empty() == true  
  
 [e] [d]  
size == 2  
empty() == false  
```  
  
##  <a name="a-nameunorderedmultisetconstiteratora--unorderedmultisetconstiterator"></a><a name="unordered_multiset__const_iterator"></a>  unordered_multiset::const_iterator  
 제어되는 시퀀스에 대한 상수 반복기의 형식입니다.  
  
```  
typedef T1 const_iterator;  
```  
  
### <a name="remarks"></a>설명  
 이 형식은 제어되는 시퀀스의 상수 정방향 반복기로 사용될 수 있는 개체를 설명합니다. 여기서는 구현에서 정의된 형식 `T1`의 동의어로 설명됩니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_const_iterator.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
[c] [b] [a]  
```  
  
##  <a name="a-nameunorderedmultisetconstlocaliteratora--unorderedmultisetconstlocaliterator"></a><a name="unordered_multiset__const_local_iterator"></a>  unordered_multiset::const_local_iterator  
 제어되는 시퀀스에 대한 상수 버킷 반복기의 형식입니다.  
  
```  
typedef T5 const_local_iterator;  
```  
  
### <a name="remarks"></a>설명  
 형식은 버킷의 상수 정방향 반복기로 사용될 수 있는 개체를 설명합니다. 여기서는 구현에서 정의된 형식 `T5`의 동의어로 설명됩니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_const_local_iterator.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
// inspect bucket containing 'a'   
    Myset::const_local_iterator lit = c1.begin(c1.bucket('a'));   
    std::cout << " [" << *lit << "]";   
  
    return (0);   
    }  
  
```  
  
```Output  
[c] [b] [a]  
[a]  
```  
  
##  <a name="a-nameunorderedmultisetconstpointera--unorderedmultisetconstpointer"></a><a name="unordered_multiset__const_pointer"></a>  unordered_multiset::const_pointer  
 요소에 대한 상수 포인터의 형식입니다.  
  
```  
typedef Alloc::const_pointer const_pointer;  
```  
  
### <a name="remarks"></a>설명  
 이 형식은 제어되는 시퀀스의 요소에 대한 상수 포인터로 사용될 수 있는 개체를 설명합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_const_pointer.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::iterator it = c1.begin();   
        it != c1.end(); ++it)   
        {   
        Myset::const_pointer p = &*it;   
        std::cout << " [" << *p << "]";   
        }   
    std::cout << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
[c] [b] [a]  
```  
  
##  <a name="a-nameunorderedmultisetconstreferencea--unorderedmultisetconstreference"></a><a name="unordered_multiset__const_reference"></a>  unordered_multiset::const_reference  
 요소에 대한 상수 참조의 형식입니다.  
  
```  
typedef Alloc::const_reference const_reference;  
```  
  
### <a name="remarks"></a>설명  
 이 형식은 제어되는 시퀀스의 요소에 대한 상수 참조로 사용될 수 있는 개체를 설명합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_const_reference.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::iterator it = c1.begin();   
        it != c1.end(); ++it)   
        {   
        Myset::const_reference ref = *it;   
        std::cout << " [" << ref << "]";   
        }   
    std::cout << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
[c] [b] [a]  
```  
  
##  <a name="a-nameunorderedmultisetcounta--unorderedmultisetcount"></a><a name="unordered_multiset__count"></a>  unordered_multiset::count  
 지정한 키와 일치하는 요소의 수를 찾습니다.  
  
```  
size_type count(const Key& keyval) const;
```  
  
### <a name="parameters"></a>매개 변수  
 `keyval`  
 검색할 키 값입니다.  
  
### <a name="remarks"></a>설명  
 구성원 함수는 [unordered_multiset::equal_range](#unordered_multiset__equal_range)`(keyval)`로 구분된 범위의 요소 수를 반환합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_count.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
    std::cout << "count('A') == " << c1.count('A') << std::endl;   
    std::cout << "count('b') == " << c1.count('b') << std::endl;   
    std::cout << "count('C') == " << c1.count('C') << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
 [c] [b] [a]  
count('A') == 0  
count('b') == 1  
count('C') == 0  
```  
  
##  <a name="a-nameunorderedmultisetdifferencetypea--unorderedmultisetdifferencetype"></a><a name="unordered_multiset__difference_type"></a>  unordered_multiset::difference_type  
 두 요소 사이의 부호가 있는 거리의 형식입니다.  
  
```  
typedef T3 difference_type;  
```  
  
### <a name="remarks"></a>설명  
 부호 있는 정수 형식은 제어되는 시퀀스에서 두 요소의 주소 간 차이점을 나타낼 수 있는 개체를 설명합니다. 여기서는 구현에서 정의된 형식 `T3`의 동의어로 설명됩니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_difference_type.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
// compute positive difference   
    Myset::difference_type diff = 0;   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        ++diff;   
    std::cout << "end()-begin() == " << diff << std::endl;   
  
// compute negative difference   
    diff = 0;   
    for (Myset::const_iterator it = c1.end();   
        it != c1.begin(); --it)   
        --diff;   
    std::cout << "begin()-end() == " << diff << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
 [c] [b] [a]  
end()-begin() == 3  
begin()-end() == -3  
```  
  
##  <a name="a-nameunorderedmultisetemplacea--unorderedmultisetemplace"></a><a name="unordered_multiset__emplace"></a>  unordered_multiset::emplace  
 생성된 요소를 제 위치에 삽입합니다. 복사 또는 이동 작업은 수행되지 않습니다.  
  
```  
template <class... Args>  
iterator emplace(Args&&... args);
```  
  
### <a name="parameters"></a>매개 변수  
  
|||  
|-|-|  
|매개 변수|설명|  
|`args`|unordered_multiset에 삽입할 요소를 생성하기 위해 전달되는 인수입니다.|  
  
### <a name="return-value"></a>반환 값  
 새로 삽입된 요소에 대한 반복기입니다.  
  
### <a name="remarks"></a>설명  
 이 함수는 컨테이너 요소에 대한 참조는 무효화하지 않지만 컨테이너에 대한 모든 반복기는 무효화할 수 있습니다.  
  
 삽입 중에 예외가 throw되었으나 컨테이너의 해시 함수에서 발생하지 않은 경우에는 컨테이너가 수정되지 않습니다. 예외가 해시 함수에서 throw된 경우 결과는 정의되어 있지 않습니다.  
  
 코드 예제를 보려면 [multiset::emplace](../standard-library/multiset-class.md#multiset__emplace)를 참조하세요.  
  
##  <a name="a-nameunorderedmultisetemplacehinta--unorderedmultisetemplacehint"></a><a name="unordered_multiset__emplace_hint"></a>  unordered_multiset::emplace_hint  
 배치 힌트를 사용하여 생성된 요소를 제 위치에 삽입합니다. 복사 또는 이동 작업은 수행되지 않습니다.  
  
```  
template <class... Args>  
iterator emplace_hint(
    const_iterator where,  
    Args&&... args);
```  
  
### <a name="parameters"></a>매개 변수  
  
|||  
|-|-|  
|매개 변수|설명|  
|`args`|unordered_multiset에 삽입할 요소를 생성하기 위해 전달되는 인수입니다.|  
|`where`|올바른 삽입 지점 검색을 시작할 위치와 관련된 힌트입니다.|  
  
### <a name="return-value"></a>반환 값  
 새로 삽입된 요소에 대한 반복기입니다.  
  
### <a name="remarks"></a>설명  
 이 함수는 컨테이너 요소에 대한 참조는 무효화하지 않지만 컨테이너에 대한 모든 반복기는 무효화할 수 있습니다.  
  
 삽입 중에 예외가 throw되었으나 컨테이너의 해시 함수에서 발생하지 않은 경우에는 컨테이너가 수정되지 않습니다. 예외가 해시 함수에서 throw된 경우 결과는 정의되어 있지 않습니다.  
  
 코드 예제를 보려면 [set::emplace_hint](../standard-library/set-class.md#set__emplace_hint)를 참조하세요.  
  
##  <a name="a-nameunorderedmultisetemptya--unorderedmultisetempty"></a><a name="unordered_multiset__empty"></a>  unordered_multiset::empty  
 요소가 있는지 여부를 테스트합니다.  
  
```  
bool empty() const;
```  
  
### <a name="remarks"></a>설명  
 멤버 함수는 빈 제어되는 시퀀스에 대해 true를 반환합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_empty.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
// clear the container and reinspect   
    c1.clear();   
    std::cout << "size == " << c1.size() << std::endl;   
    std::cout << "empty() == " << std::boolalpha << c1.empty() << std::endl;   
    std::cout << std::endl;   
  
    c1.insert('d');   
    c1.insert('e');   
  
// display contents " [e] [d]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
    std::cout << "size == " << c1.size() << std::endl;   
    std::cout << "empty() == " << std::boolalpha << c1.empty() << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
 [c] [b] [a]  
size == 0  
empty() == true  
  
 [e] [d]  
size == 2  
empty() == false  
```  
  
##  <a name="a-nameunorderedmultisetenda--unorderedmultisetend"></a><a name="unordered_multiset__end"></a>  unordered_multiset::end  
 제어되는 시퀀스의 끝을 지정합니다.  
  
```  
iterator end();
const_iterator end() const;

 
    local_iterator end(size_type nbucket);
const_local_iterator end(size_type nbucket) const;
```  
  
### <a name="parameters"></a>매개 변수  
 `nbucket`  
 버킷 번호입니다.  
  
### <a name="remarks"></a>설명  
 처음 두 멤버 함수는 시퀀스 끝의 바로 다음을 가리키는 정방향 반복기를 반환합니다. 마지막 두 멤버 함수는 `nbucket` 버킷 끝의 바로 다음을 가리키는 정방향 반복기를 반환합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_end.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
// inspect last two items " [a] [b]"   
    Myset::iterator it2 = c1.end();   
    --it2;   
    std::cout << " [" << *it2 << "]";   
    --it2;   
    std::cout << " [" << *it2 << "]";   
    std::cout << std::endl;   
  
// inspect bucket containing 'a'   
    Myset::const_local_iterator lit = c1.end(c1.bucket('a'));   
    --lit;   
    std::cout << " [" << *lit << "]";   
  
    return (0);   
    }  
  
```  
  
```Output  
[c] [b] [a]  
[a] [b]  
[a]  
```  
  
##  <a name="a-nameunorderedmultisetequalrangea--unorderedmultisetequalrange"></a><a name="unordered_multiset__equal_range"></a>  unordered_multiset::equal_range  
 지정된 키와 일치하는 범위를 찾습니다.  
  
```  
std::pair<iterator, iterator>  
    equal_range(const Key& keyval);

std::pair<const_iterator, const_iterator>  
    equal_range(const Key& keyval) const;
```  
  
### <a name="parameters"></a>매개 변수  
 `keyval`  
 검색할 키 값입니다.  
  
### <a name="remarks"></a>설명  
 멤버 함수는 `X` 을 사용하여 동일하게 정렬된 제어되는 시퀀스의 요소만 `[X.first, X.second)` 로 구분되도록 한 쌍의 반복기 `keyval`를 반환합니다. 이러한 요소가 없는 경우 두 반복기는 `end()`입니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_equal_range.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
// display results of failed search   
    std::pair<Myset::iterator, Myset::iterator> pair1 =   
        c1.equal_range('x');   
    std::cout << "equal_range('x'):";   
    for (; pair1.first != pair1.second; ++pair1.first)   
        std::cout << " [" << *pair1.first << "]";   
    std::cout << std::endl;   
  
// display results of successful search   
    pair1 = c1.equal_range('b');   
    std::cout << "equal_range('b'):";   
    for (; pair1.first != pair1.second; ++pair1.first)   
        std::cout << " [" << *pair1.first << "]";   
    std::cout << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
 [c] [b] [a]  
equal_range('x'):  
equal_range('b'): [b]  
```  
  
##  <a name="a-nameunorderedmultiseterasea--unorderedmultiseterase"></a><a name="unordered_multiset__erase"></a>  unordered_multiset::erase  
 지정된 위치에서 unordered_multiset의 요소 또는 요소의 범위를 제거하거나 지정된 키와 일치하는 요소를 제거합니다.  
  
```  
iterator erase(
    const_iterator Where);

iterator erase(
    const_iterator First,  
    const_iterator Last);

size_type erase(
    const key_type& Key);
```  
  
### <a name="parameters"></a>매개 변수  
 `Where`  
 제거할 요소의 위치입니다.  
  
 `First`  
 제거할 첫 번째 요소의 위치입니다.  
  
 `Last`  
 제거할 마지막 요소 바로 다음 위치입니다.  
  
 `Key`  
 제거할 요소의 키 값입니다.  
  
### <a name="return-value"></a>반환 값  
 처음 두 구성원 함수의 경우 제거된 요소 뒤에 남은 첫 번째 요소 또는 이러한 요소가 없을 경우 unordered_multiset의 끝에 있는 요소를 지정하는 양방향 반복기입니다.  
  
 세 번째 구성원 함수의 경우 unordered_multiset에서 제거된 요소의 수를 반환합니다.  
  
### <a name="remarks"></a>설명  
 코드 예제를 보려면 [set::erase](../standard-library/set-class.md#set__erase)를 참조하세요.  
  
##  <a name="a-nameunorderedmultisetfinda--unorderedmultisetfind"></a><a name="unordered_multiset__find"></a>  unordered_multiset::find  
 지정된 키와 일치하는 요소를 찾습니다.  
  
```  
const_iterator find(const Key& keyval) const;
```  
  
### <a name="parameters"></a>매개 변수  
 `keyval`  
 검색할 키 값입니다.  
  
### <a name="remarks"></a>설명  
 구성원 함수는 [unordered_multiset::equal_range](#unordered_multiset__equal_range)`(keyval).first`를 반환합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_find.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
// try to find and fail   
    std::cout << "find('A') == "   
        << std::boolalpha << (c1.find('A') != c1.end()) << std::endl;   
  
// try to find and succeed   
    Myset::iterator it = c1.find('b');   
    std::cout << "find('b') == "   
        << std::boolalpha << (it != c1.end())   
        << ": [" << *it << "]" << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
 [c] [b] [a]  
find('A') == false  
find('b') == true: [b]  
```  
  
##  <a name="a-nameunorderedmultisetgetallocatora--unorderedmultisetgetallocator"></a><a name="unordered_multiset__get_allocator"></a>  unordered_multiset::get_allocator  
 저장된 할당자 개체를 가져옵니다.  
  
```  
Alloc get_allocator() const;
```  
  
### <a name="remarks"></a>설명  
 멤버 함수는 저장된 할당자 개체를 반환합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_get_allocator.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
typedef std::allocator<std::pair<const char, int> > Myalloc;   
int main()   
    {   
    Myset c1;   
  
    Myset::allocator_type al = c1.get_allocator();   
    std::cout << "al == std::allocator() is "   
        << std::boolalpha << (al == Myalloc()) << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
al == std::allocator() is true  
```  
  
##  <a name="a-nameunorderedmultisethashfunctiona--unorderedmultisethashfunction"></a><a name="unordered_multiset__hash_function"></a>  unordered_multiset::hash_function  
 저장된 해시 함수 개체를 가져옵니다.  
  
```  
Hash hash_function() const;
```  
  
### <a name="remarks"></a>설명  
 멤버 함수는 저장된 해시 함수 개체를 반환합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_hash_function.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    Myset::hasher hfn = c1.hash_function();   
    std::cout << "hfn('a') == " << hfn('a') << std::endl;   
    std::cout << "hfn('b') == " << hfn('b') << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
hfn('a') == 1630279  
hfn('b') == 1647086  
```  
  
##  <a name="a-nameunorderedmultisethashera--unorderedmultisethasher"></a><a name="unordered_multiset__hasher"></a>  unordered_multiset::hasher  
 해시 함수의 형식입니다.  
  
```  
typedef Hash hasher;  
```  
  
### <a name="remarks"></a>설명  
 이 형식은 템플릿 매개 변수 `Hash`의 동의어입니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_hasher.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    Myset::hasher hfn = c1.hash_function();   
    std::cout << "hfn('a') == " << hfn('a') << std::endl;   
    std::cout << "hfn('b') == " << hfn('b') << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
hfn('a') == 1630279  
hfn('b') == 1647086  
```  
  
##  <a name="a-nameunorderedmultisetinserta--unorderedmultisetinsert"></a><a name="unordered_multiset__insert"></a>  unordered_multiset::insert  
 unordered_multiset에 요소 또는 요소의 범위를 삽입합니다.  
  
```  
// (1) single element  
pair<iterator, bool> insert(
    const value_type& Val);

 
// (2) single element, perfect forwarded  
template <class ValTy>  
pair<iterator, bool>  
insert(
    ValTy&& Val);

 
// (3) single element with hint  
iterator insert(
    const_iterator Where,  
    const value_type& Val);

 
// (4) single element, perfect forwarded, with hint  
template <class ValTy>  
iterator insert(
    const_iterator Where,  
    ValTy&& Val);

 
// (5) range   
template <class InputIterator>   
void insert(
    InputIterator First,  
    InputIterator Last);

 
// (6) initializer list  
void insert(
    initializer_list<value_type>  
IList);
```  
  
### <a name="parameters"></a>매개 변수  
  
|||  
|-|-|  
|매개 변수|설명|  
|`Val`|unordered_multiset에 삽입할 요소의 값입니다.|  
|`Where`|올바른 삽입 지점 검색을 시작할 위치입니다.|  
|`ValTy`|unordered_multiset가 [value_type](../standard-library/map-class.md#map__value_type)의 요소를 생성하는 데 사용할 수 있는 인수 형식을 지정하고 `Val`을 인수로 완벽하게 전달하는 템플릿 매개 변수입니다.|  
|`First`|복사할 첫 번째 요소의 위치입니다.|  
|`Last`|복사할 마지막 요소 바로 다음 위치입니다.|  
|`InputIterator`|[value_type](../standard-library/map-class.md#map__value_type) 개체를 생성하는 데 사용할 수 있는 형식의 요소를 가리키는 [입력 반복기](../standard-library/input-iterator-tag-struct.md)의 요구 사항을 충족하는 템플릿 함수 인수입니다.|  
|`IList`|요소를 복사할 원본 [initializer_list](../standard-library/initializer-list.md)입니다.|  
  
### <a name="return-value"></a>반환 값  
 단일 요소 삽입 멤버 함수 (1) 및 (2)는 unordered_multiset에 새 요소를 삽입한 위치로 반복기를 반환합니다.  
  
 힌트가 있는 단일 요소 멤버 함수 (3) 및 (4)는 unordered_multiset에 새 요소를 삽입한 위치를 가리키는 반복기를 반환합니다.  
  
### <a name="remarks"></a>설명  
 이 함수는 어떠한 포인터 또는 참조를 무효화하지 않지만 컨테이너에 대한 모든 반복기를 무효화할 수 있습니다.  
  
 요소를 하나만 삽입하는 중 예외가 throw되었으나 컨테이너의 해시 함수에서 발생하지 않은 경우에는 컨테이너의 상태가 수정되지 않습니다. 예외가 해시 함수에서 throw된 경우 결과는 정의되어 있지 않습니다. 여러 요소를 삽입하는 중 예외가 throw되면 컨테이너는 지정되지 않았으나 유효한 상태로 남아 있습니다.  
  
 컨테이너의 [value_type](../standard-library/map-class.md#map__value_type)은 컨테이너에 속한 형식 정의이고 set의 경우 `unordered_multiset<V>::value_type`은 `const V`입니다.  
  
 범위 멤버 함수 (5)는 `[First, Last)` 범위에서 반복기가 주소를 지정하는 각 요소에 해당하는 unordered_multiset에 요소 값의 시퀀스를 입력하므로 `Last`는 삽입되지 않습니다. 컨테이너 멤버 함수 `end()`는 컨테이너의 마지막 요소 바로 뒤에 있는 위치를 참조합니다. 예를 들어 `m.insert(v.begin(), v.end());` 문은 `v`의 모든 요소를 `m`에 삽입합니다.  
  
 이니셜라이저 목록 구성원 함수 (6)은 [initializer_list](../standard-library/initializer-list.md)를 사용하여 요소를 unordered_multiset로 복사합니다.  
  
 생성된 요소를 제 위치에 삽입하려면, 즉 복사 또는 이동 작업을 수행하지 않으려면 [unordered_multiset::emplace](#unordered_multiset__emplace) 및 [unordered_multiset::emplace_hint](#unordered_multiset__emplace_hint)를 참조하세요.  
  
 코드 예제를 보려면 [multiset::insert](../standard-library/multiset-class.md#multiset__insert)를 참조하세요.  
  
##  <a name="a-nameunorderedmultisetiteratora--unorderedmultisetiterator"></a><a name="unordered_multiset__iterator"></a>  unordered_multiset::iterator  
 unordered_multiset의 요소를 읽을 수 있는 상수 [정방향 반복기](../standard-library/forward-iterator-tag-struct.md)를 제공하는 형식입니다.  
  
```  
typedef implementation-defined iterator;  
```  
  
### <a name="example"></a>예제  
  **반복기**를 선언하고 사용하는 방법의 예제는 [begin](../standard-library/multiset-class.md#multiset__begin)의 예제를 참조하세요.  
  
##  <a name="a-nameunorderedmultisetkeyeqa--unorderedmultisetkeyeq"></a><a name="unordered_multiset__key_eq"></a>  unordered_multiset::key_eq  
 저장된 비교 함수 개체를 가져옵니다.  
  
```  
Pred key_eq() const;
```  
  
### <a name="remarks"></a>설명  
 멤버 함수는 저장된 비교 함수 개체를 반환합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_key_eq.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    Myset::key_equal cmpfn = c1.key_eq();   
    std::cout << "cmpfn('a', 'a') == "   
        << std::boolalpha << cmpfn('a', 'a') << std::endl;   
    std::cout << "cmpfn('a', 'b') == "   
        << std::boolalpha << cmpfn('a', 'b') << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
cmpfn('a', 'a') == true  
cmpfn('a', 'b') == false  
```  
  
##  <a name="a-nameunorderedmultisetkeyequala--unorderedmultisetkeyequal"></a><a name="unordered_multiset__key_equal"></a>  unordered_multiset::key_equal  
 비교 함수의 형식입니다.  
  
```  
typedef Pred key_equal;  
```  
  
### <a name="remarks"></a>설명  
 이 형식은 템플릿 매개 변수 `Pred`의 동의어입니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_key_equal.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    Myset::key_equal cmpfn = c1.key_eq();   
    std::cout << "cmpfn('a', 'a') == "   
        << std::boolalpha << cmpfn('a', 'a') << std::endl;   
    std::cout << "cmpfn('a', 'b') == "   
        << std::boolalpha << cmpfn('a', 'b') << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
cmpfn('a', 'a') == true  
cmpfn('a', 'b') == false  
```  
  
##  <a name="a-nameunorderedmultisetkeytypea--unorderedmultisetkeytype"></a><a name="unordered_multiset__key_type"></a>  unordered_multiset::key_type  
 정렬 키의 형식입니다.  
  
```  
typedef Key key_type;  
```  
  
### <a name="remarks"></a>설명  
 이 형식은 템플릿 매개 변수 `Key`의 동의어입니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_key_type.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
// add a value and reinspect   
    Myset::key_type key = 'd';   
    Myset::value_type val = key;   
    c1.insert(val);   
  
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
[c] [b] [a]  
[d] [c] [b] [a]  
```  
  
##  <a name="a-nameunorderedmultisetloadfactora--unorderedmultisetloadfactor"></a><a name="unordered_multiset__load_factor"></a>  unordered_multiset::load_factor  
 버킷당 평균 요소 수를 계산합니다.  
  
```  
float load_factor() const;
```  
  
### <a name="remarks"></a>설명  
 구성원 함수는 `(float)`[unordered_multiset::size](#unordered_multiset__size)`() / (float)`[unordered_multiset::bucket_count](#unordered_multiset__bucket_count)`()`(버킷당 평균 요소 수)를 반환합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_load_factor.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
// inspect current parameters   
    std::cout << "bucket_count() == " << c1.bucket_count() << std::endl;   
    std::cout << "load_factor() == " << c1.load_factor() << std::endl;   
    std::cout << "max_bucket_count() == "   
        << c1.max_bucket_count() << std::endl;   
    std::cout << "max_load_factor() == "   
        << c1.max_load_factor() << std::endl;   
    std::cout << std::endl;   
  
// change max_load_factor and redisplay   
    c1.max_load_factor(0.10f);   
    std::cout << "bucket_count() == " << c1.bucket_count() << std::endl;   
    std::cout << "load_factor() == " << c1.load_factor() << std::endl;   
    std::cout << "max_bucket_count() == "   
        << c1.max_bucket_count() << std::endl;   
    std::cout << "max_load_factor() == "   
        << c1.max_load_factor() << std::endl;   
    std::cout << std::endl;   
  
// rehash and redisplay   
    c1.rehash(100);   
    std::cout << "bucket_count() == " << c1.bucket_count() << std::endl;   
    std::cout << "load_factor() == " << c1.load_factor() << std::endl;   
    std::cout << "max_bucket_count() == "   
        << c1.max_bucket_count() << std::endl;   
    std::cout << "max_load_factor() == "   
        << c1.max_load_factor() << std::endl;   
    std::cout << std::endl;   
  
    return (0);   
    }  
  
```  
  
##  <a name="a-nameunorderedmultisetlocaliteratora--unorderedmultisetlocaliterator"></a><a name="unordered_multiset__local_iterator"></a>  unordered_multiset::local_iterator  
 버킷 반복기의 형식입니다.  
  
```  
typedef T4 local_iterator;  
```  
  
### <a name="remarks"></a>설명  
 형식은 버킷의 정방향 반복기로 사용될 수 있는 개체를 설명합니다. 여기서는 구현에서 정의된 형식 `T4`의 동의어로 설명됩니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_local_iterator.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
// inspect bucket containing 'a'   
    Myset::local_iterator lit = c1.begin(c1.bucket('a'));   
    std::cout << " [" << *lit << "]";   
  
    return (0);   
    }  
  
```  
  
```Output  
[c] [b] [a]  
[a]  
```  
  
##  <a name="a-nameunorderedmultisetmaxbucketcounta--unorderedmultisetmaxbucketcount"></a><a name="unordered_multiset__max_bucket_count"></a>  unordered_multiset::max_bucket_count  
 최대 버킷 개수를 가져옵니다.  
  
```  
size_type max_bucket_count() const;
```  
  
### <a name="remarks"></a>설명  
 멤버 함수는 현재 허용된 최대 버킷 개수를 반환합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_max_bucket_count.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
// inspect current parameters   
    std::cout << "bucket_count() == " << c1.bucket_count() << std::endl;   
    std::cout << "load_factor() == " << c1.load_factor() << std::endl;   
    std::cout << "max_bucket_count() == "   
        << c1.max_bucket_count() << std::endl;   
    std::cout << "max_load_factor() == "   
        << c1.max_load_factor() << std::endl;   
    std::cout << std::endl;   
  
// change max_load_factor and redisplay   
    c1.max_load_factor(0.10f);   
    std::cout << "bucket_count() == " << c1.bucket_count() << std::endl;   
    std::cout << "load_factor() == " << c1.load_factor() << std::endl;   
    std::cout << "max_bucket_count() == "   
        << c1.max_bucket_count() << std::endl;   
    std::cout << "max_load_factor() == "   
        << c1.max_load_factor() << std::endl;   
    std::cout << std::endl;   
  
// rehash and redisplay   
    c1.rehash(100);   
    std::cout << "bucket_count() == " << c1.bucket_count() << std::endl;   
    std::cout << "load_factor() == " << c1.load_factor() << std::endl;   
    std::cout << "max_bucket_count() == "   
        << c1.max_bucket_count() << std::endl;   
    std::cout << "max_load_factor() == "   
        << c1.max_load_factor() << std::endl;   
    std::cout << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
 [c] [b] [a]  
bucket_count() == 8  
load_factor() == 0.375  
max_bucket_count() == 8  
max_load_factor() == 4  
  
bucket_count() == 8  
load_factor() == 0.375  
max_bucket_count() == 8  
max_load_factor() == 0.1  
  
bucket_count() == 128  
load_factor() == 0.0234375  
max_bucket_count() == 128  
max_load_factor() == 0.1  
  
```  
  
##  <a name="a-nameunorderedmultisetmaxloadfactora--unorderedmultisetmaxloadfactor"></a><a name="unordered_multiset__max_load_factor"></a>  unordered_multiset::max_load_factor  
 버킷당 최대 요소 수를 가져오거나 설정합니다.  
  
```  
float max_load_factor() const;

 
void max_load_factor(float factor);
```  
  
### <a name="parameters"></a>매개 변수  
 `factor`  
 새로운 최대 로드 비율입니다.  
  
### <a name="remarks"></a>설명  
 첫 번째 멤버 함수는 저장된 최대 로드 비율을 반환합니다. 두 번째 멤버 함수는 저장된 최대 로드 비율을 `factor`로 바꿉니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_max_load_factor.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
// inspect current parameters   
    std::cout << "bucket_count() == " << c1.bucket_count() << std::endl;   
    std::cout << "load_factor() == " << c1.load_factor() << std::endl;   
    std::cout << "max_bucket_count() == "   
        << c1.max_bucket_count() << std::endl;   
    std::cout << "max_load_factor() == "   
        << c1.max_load_factor() << std::endl;   
    std::cout << std::endl;   
  
// change max_load_factor and redisplay   
    c1.max_load_factor(0.10f);   
    std::cout << "bucket_count() == " << c1.bucket_count() << std::endl;   
    std::cout << "load_factor() == " << c1.load_factor() << std::endl;   
    std::cout << "max_bucket_count() == "   
        << c1.max_bucket_count() << std::endl;   
    std::cout << "max_load_factor() == "   
        << c1.max_load_factor() << std::endl;   
    std::cout << std::endl;   
  
// rehash and redisplay   
    c1.rehash(100);   
    std::cout << "bucket_count() == " << c1.bucket_count() << std::endl;   
    std::cout << "load_factor() == " << c1.load_factor() << std::endl;   
    std::cout << "max_bucket_count() == "   
        << c1.max_bucket_count() << std::endl;   
    std::cout << "max_load_factor() == "   
        << c1.max_load_factor() << std::endl;   
    std::cout << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
 [c] [b] [a]  
bucket_count() == 8  
load_factor() == 0.375  
max_bucket_count() == 8  
max_load_factor() == 4  
  
bucket_count() == 8  
load_factor() == 0.375  
max_bucket_count() == 8  
max_load_factor() == 0.1  
  
bucket_count() == 128  
load_factor() == 0.0234375  
max_bucket_count() == 128  
max_load_factor() == 0.1  
  
```  
  
##  <a name="a-nameunorderedmultisetmaxsizea--unorderedmultisetmaxsize"></a><a name="unordered_multiset__max_size"></a>  unordered_multiset::max_size  
 제어되는 시퀀스의 최대 크기를 가져옵니다.  
  
```  
size_type max_size() const;
```  
  
### <a name="remarks"></a>설명  
 멤버 함수는 개체가 제어할 수 있는 가장 긴 시퀀스의 길이를 반환합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_max_size.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    std::cout << "max_size() == " << c1.max_size() << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
max_size() == 4294967295  
```  
  
##  <a name="a-nameunorderedmultisetoperatoreqa--unorderedmultisetoperator"></a><a name="unordered_multiset__operator_eq"></a>  unordered_multiset::operator=  
 해시 테이블을 복사합니다.  
  
```  
unordered_multiset& operator=(const unordered_multiset& right);

unordered_multiset& operator=(unordered_multiset&& right);
```  
  
### <a name="parameters"></a>매개 변수  
  
|||  
|-|-|  
|매개 변수|설명|  
|` right`|`unordered_multiset`에 복사되는 [unordered_multiset](../standard-library/unordered-multiset-class.md)입니다.|  
  
### <a name="remarks"></a>설명  
 `operator=`는 `unordered_multiset`에서 기존 요소를 지운 후에 ` right`의 내용을 `unordered_multiset`로 복사하거나 이동합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// unordered_multiset_operator_as.cpp  
// compile with: /EHsc  
#include <unordered_set>  
#include <iostream>  
  
int main( )  
   {  
   using namespace std;  
   unordered_multiset<int> v1, v2, v3;  
   unordered_multiset<int>::iterator iter;  
  
   v1.insert(10);  
  
   cout << "v1 = " ;  
   for (iter = v1.begin(); iter != v1.end(); iter++)  
      cout << *iter << " ";  
   cout << endl;  
  
   v2 = v1;  
   cout << "v2 = ";  
   for (iter = v2.begin(); iter != v2.end(); iter++)  
      cout << *iter << " ";  
   cout << endl;  
  
// move v1 into v2  
   v2.clear();  
   v2 = move(v1);  
   cout << "v2 = ";  
   for (iter = v2.begin(); iter != v2.end(); iter++)  
      cout << *iter << " ";  
   cout << endl;  
   }  
```  
  
##  <a name="a-nameunorderedmultisetpointera--unorderedmultisetpointer"></a><a name="unordered_multiset__pointer"></a>  unordered_multiset::pointer  
 요소에 대한 포인터의 형식입니다.  
  
```  
typedef Alloc::pointer pointer;  
```  
  
### <a name="remarks"></a>설명  
 이 형식은 제어되는 시퀀스의 요소에 대한 포인터로 사용될 수 있는 개체를 설명합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_pointer.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::iterator it = c1.begin();   
        it != c1.end(); ++it)   
        {   
        Myset::key_type key = *it;   
        Myset::pointer p = &key;   
        std::cout << " [" << *p << "]";   
        }   
    std::cout << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
[c] [b] [a]  
```  
  
##  <a name="a-nameunorderedmultisetreferencea--unorderedmultisetreference"></a><a name="unordered_multiset__reference"></a>  unordered_multiset::reference  
 요소에 대한 참조의 형식입니다.  
  
```  
typedef Alloc::reference reference;  
```  
  
### <a name="remarks"></a>설명  
 이 형식은 제어되는 시퀀스의 요소에 대한 참조로 사용될 수 있는 개체를 설명합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_reference.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::iterator it = c1.begin();   
        it != c1.end(); ++it)   
        {   
        Myset::key_type key = *it;   
        Myset::reference ref = key;   
        std::cout << " [" << ref << "]";   
        }   
    std::cout << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
[c] [b] [a]  
```  
  
##  <a name="a-nameunorderedmultisetrehasha--unorderedmultisetrehash"></a><a name="unordered_multiset__rehash"></a>  unordered_multiset::rehash  
 해시 테이블을 다시 빌드합니다.  
  
```  
void rehash(size_type nbuckets);
```  
  
### <a name="parameters"></a>매개 변수  
 `nbuckets`  
 요청된 버킷 수입니다.  
  
### <a name="remarks"></a>설명  
 멤버 함수는 필요에 따라 버킷 수를 `nbuckets` 이상으로 변경하고 해시 테이블을 다시 빌드합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_rehash.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
// inspect current parameters   
    std::cout << "bucket_count() == " << c1.bucket_count() << std::endl;   
    std::cout << "load_factor() == " << c1.load_factor() << std::endl;   
    std::cout << "max_load_factor() == " << c1.max_load_factor() << std::endl;   
    std::cout << std::endl;   
  
// change max_load_factor and redisplay   
    c1.max_load_factor(0.10f);   
    std::cout << "bucket_count() == " << c1.bucket_count() << std::endl;   
    std::cout << "load_factor() == " << c1.load_factor() << std::endl;   
    std::cout << "max_load_factor() == " << c1.max_load_factor() << std::endl;   
    std::cout << std::endl;   
  
// rehash and redisplay   
    c1.rehash(100);   
    std::cout << "bucket_count() == " << c1.bucket_count() << std::endl;   
    std::cout << "load_factor() == " << c1.load_factor() << std::endl;   
    std::cout << "max_load_factor() == " << c1.max_load_factor() << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
 [c] [b] [a]  
bucket_count() == 8  
load_factor() == 0.375  
max_load_factor() == 4  
  
bucket_count() == 8  
load_factor() == 0.375  
max_load_factor() == 0.1  
  
bucket_count() == 128  
load_factor() == 0.0234375  
max_load_factor() == 0.1  
```  
  
##  <a name="a-nameunorderedmultisetsizea--unorderedmultisetsize"></a><a name="unordered_multiset__size"></a>  unordered_multiset::size  
 요소 수를 계산합니다.  
  
```  
size_type size() const;
```  
  
### <a name="remarks"></a>설명  
 멤버 함수는 제어되는 시퀀스의 길이를 반환합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_size.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
// clear the container and reinspect   
    c1.clear();   
    std::cout << "size == " << c1.size() << std::endl;   
    std::cout << "empty() == " << std::boolalpha << c1.empty() << std::endl;   
    std::cout << std::endl;   
  
    c1.insert('d');   
    c1.insert('e');   
  
// display contents " [e] [d]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
    std::cout << "size == " << c1.size() << std::endl;   
    std::cout << "empty() == " << std::boolalpha << c1.empty() << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
 [c] [b] [a]  
size == 0  
empty() == true  
  
 [e] [d]  
size == 2  
empty() == false  
```  
  
##  <a name="a-nameunorderedmultisetsizetypea--unorderedmultisetsizetype"></a><a name="unordered_multiset__size_type"></a>  unordered_multiset::size_type  
 두 요소 사이의 부호가 없는 거리의 형식입니다.  
  
```  
typedef T2 size_type;  
```  
  
### <a name="remarks"></a>설명  
 부호 없는 정수 형식은 제어되는 시퀀스의 길이를 나타낼 수 있는 개체를 설명합니다. 여기서는 구현에서 정의된 형식 `T2`의 동의어로 설명됩니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_size_type.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
    Myset::size_type sz = c1.size();   
  
    std::cout << "size == " << sz << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
size == 0  
```  
  
##  <a name="a-nameunorderedmultisetswapa--unorderedmultisetswap"></a><a name="unordered_multiset__swap"></a>  unordered_multiset::swap  
 두 컨테이너의 내용을 바꿉니다.  
  
```  
void swap(unordered_multiset& right);
```  
  
### <a name="parameters"></a>매개 변수  
 `right`  
 교환할 컨테이너입니다.  
  
### <a name="remarks"></a>설명  
 멤버 함수는 `*this` 와 `right`간에 제어되는 시퀀스를 교환합니다. [unordered_multiset::get_allocator](#unordered_multiset__get_allocator)`() == right.get_allocator()`인 경우 일정 시간에 이 작업을 수행하고 `Tr` 형식의 저장된 특성 개체를 복사한 결과로만 예외를 throw하며 두 개의 제어되는 시퀀스에서 요소를 지정하는 참조, 포인터 또는 반복기를 무효화하지 않습니다. 그렇지 않으면 두 개의 제어되는 시퀀스에 있는 요소 수에 비례하여 많은 요소 할당 및 생성자 호출을 수행합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_swap.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
    Myset c2;   
  
    c2.insert('d');   
    c2.insert('e');   
    c2.insert('f');   
  
    c1.swap(c2);   
  
// display contents " [f] [e] [d]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
    swap(c1, c2);   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
[c] [b] [a]  
[f] [e] [d]  
[c] [b] [a]  
```  
  
##  <a name="a-nameunorderedmultisetunorderedmultiseta--unorderedmultisetunorderedmultiset"></a><a name="unordered_multiset__unordered_multiset"></a>  unordered_multiset::unordered_multiset  
 컨테이너 개체를 만듭니다.  
  
```  
unordered_multiset(
    const unordered_multiset& Right);

explicit unordered_multiset(
    size_type Bucket_count = N0,  
    const Hash& Hash = Hash(),  
    const Comp& Comp = Comp(),  
    const Allocator& Al = Alloc());

unordered_multiset(
    unordered_multiset&& Right);

unordered_set(
    initializer_list<Type> IList);

unordered_set(
    initializer_list<Typ> IList,  
    size_type Bucket_count);

unordered_set(
    initializer_list<Type> IList,   
    size_type Bucket_count,   
    const Hash& Hash);

unordered_set(
    initializer_list<Type> IList,   
    size_type Bucket_count,   
    const Hash& Hash,   
    const Key& Key);

unordered_set(
    initializer_list<Type> IList,   
    size_type Bucket_count,   
    const Hash& Hash,   
    const Key& Key,   
    const Allocator& Al);

template <class InputIterator>  
unordered_multiset(
 InputIterator First,   
    InputIterator Last,  
    size_type Bucket_count = N0,  
    const Hash& Hash = Hash(),  
    const Comp& Comp = Comp(),  
    const Allocator& Al = Alloc());
```  
  
### <a name="parameters"></a>매개 변수  
  
|||  
|-|-|  
|매개 변수|설명|  
|`InputIterator`|반복기 형식입니다.|  
|`Al`|저장할 할당자 개체입니다.|  
|`Comp`|저장할 비교 함수 개체입니다.|  
|`Hash`|저장할 해시 함수 개체입니다.|  
|`Bucket_count`|최소 버킷 수입니다.|  
|`Right`|복사할 컨테이너입니다.|  
|`IList`|복사할 initializer_list입니다.|  
  
### <a name="remarks"></a>설명  
 첫 번째 생성자는 `Right`에 의해 제어되는 시퀀스의 복사본을 지정합니다. 두 번째 생성자는 빈 제어 시퀀스를 지정합니다. 세 번째 생성자는 `[First, Last)` 요소 값의 시퀀스를 삽입합니다. 네 번째 생성자는 `Right`를 이동하여 시퀀스의 복사본을 지정합니다.  
  
 모든 생성자는 또한 여러 개의 저장된 값을 초기화합니다. 복사 생성자의 값은 `Right`에서 가져옵니다. 그렇지 않은 경우는 다음과 같습니다.  
  
 버킷 최소 수는 인수 `Bucket_count`입니다(있는 경우). 그렇지 않으면 여기에 구현 정의 값 `N0`으로 설명된 기본값입니다.  
  
 해시 함수 개체는 인수 `Hash`입니다(있는 경우). 그렇지 않으면 `Hash()`입니다.  
  
 비교 함수 개체는 인수 `Comp`입니다(있는 경우). 그렇지 않으면 `Comp()`입니다.  
  
 할당자 개체는 인수 `Al`입니다(있는 경우). 그렇지 않으면 `Alloc()`입니다.  
  
##  <a name="a-nameunorderedmultisetvaluetypea--unorderedmultisetvaluetype"></a><a name="unordered_multiset__value_type"></a>  unordered_multiset::value_type  
 요소의 형식입니다.  
  
```  
typedef Key value_type;  
```  
  
### <a name="remarks"></a>설명  
 형식은 제어되는 시퀀스의 요소를 설명합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// std__unordered_set__unordered_multiset_value_type.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
// add a value and reinspect   
    Myset::key_type key = 'd';   
    Myset::value_type val = key;   
    c1.insert(val);   
  
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
    return (0);   
    }  
  
```  
  
```Output  
[c] [b] [a]  
[d] [c] [b] [a]  
```  
  
## <a name="see-also"></a>참고 항목  
 [<unordered_set>](../standard-library/unordered-set.md)   
 [컨테이너](../cpp/containers-modern-cpp.md)   
 [C++ 표준 라이브러리의 스레드 보안](../standard-library/thread-safety-in-the-cpp-standard-library.md)   
 [C++ 표준 라이브러리 참조](../standard-library/cpp-standard-library-reference.md)

