---
title: "initializer_list 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- C++
ms.assetid: 1f2c0ff4-5636-4f79-b008-e75426e3d2ab
caps.latest.revision: 17
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
ms.sourcegitcommit: 51fbd09793071631985720550007dddbe16f598f
ms.openlocfilehash: 2ac3e7fa456e5d3ff04bc5d974c87a9cbb055fea
ms.lasthandoff: 02/24/2017

---
# <a name="initializerlist-class"></a>initializer_list 클래스
각 멤버가 지정된 형식인 요소 배열에 대한 액세스를 제공합니다.  
  
## <a name="syntax"></a>구문  
  
```  
template <class Type>  
class initializer_list
```  
  
#### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|`Type`|`initializer_list`에 저장되는 요소 데이터 형식입니다.|  

  
## <a name="remarks"></a>설명  
 중괄호로 묶인 이니셜라이저 목록을 사용하여 `initializer_list`를 생성할 수 있습니다.  
  
```cpp  
initializer_list<int> i1{ 1, 2, 3, 4 };  
```  
  
 컴파일러는 함수 서명에 `initializer_list`가 필요할 때마다 같은 요소가 포함된 중괄호로 묶인 이니셜라이저 목록을 `initializer_list`로 변환합니다. `initializer_list` 사용에 대한 자세한 내용은 [균일 초기화 및 생성자 위임](../cpp/uniform-initialization-and-delegating-constructors.md)을 참조하세요.  
  
### <a name="constructors"></a>생성자  
  
|||  
|-|-|  
|[initializer_list](../standard-library/forward-list-class.md#forward_list__forward_list)|`initializer_list` 형식의 개체를 생성합니다.|  
  
### <a name="typedefs"></a>Typedefs  
  
|||  
|-|-|  
|value_type|`initializer_list` 요소의 형식입니다.|  
|참조|`initializer_list`의 요소에 대한 참조를 제공하는 형식입니다.|  
|const_reference|`initializer_list`의 요소에 대한 상수 참조를 제공하는 형식입니다.|  
|size_type|`initializer_list`의 요소 수를 나타내는 형식입니다.|  
|iterator|`initializer_list`에 대한 반복기를 제공하는 형식입니다.|  
|const_iterator|`initializer_list`에 대한 상수 반복기를 제공하는 형식입니다.|  
  
### <a name="member-functions"></a>멤버 함수  
  
|||  
|-|-|  
|[begin](#initializer_list__begin)|`initializer_list`의 첫 번째 요소에 대한 포인터를 반환합니다.|  
|[end](#initializer_list__end)|`initializer_list`의 마지막 요소를 지난 다음 요소에 대한 포인터를 반환합니다.|  
|[size](#initializer_list__size)|`initializer_list`에 있는 요소 수를 반환합니다.|  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<initializer_list>  
  
 **네임스페이스:** std  
  
##  <a name="a-nameinitializerlistbegina--initializerlistbegin"></a><a name="initializer_list__begin"></a>  initializer_list::begin  
 `initializer_list`의 첫 번째 요소에 대한 포인터를 반환합니다.  
  
```  
constexpr const InputIterator* begin() const noexcept;  
```  
  
### <a name="return-value"></a>반환 값  
 `initializer_list`의 첫 번째 요소에 대한 포인터입니다. 목록이 비어 있는 경우 목록의 시작과 끝에 대한 포인터가 동일합니다.  
  
### <a name="remarks"></a>설명  
  
##  <a name="a-nameinitializerlistenda--initializerlistend"></a><a name="initializer_list__end"></a>  initializer_list::end  
 `initializer list`의 마지막 요소를 지난 다음 요소에 대한 포인터를 반환합니다.  
  
```  
constexpr const InputIterator* end() const noexcept;  
```  
  
### <a name="return-value"></a>반환 값  
 목록의 마지막 요소를 지난 다음 요소에 대한 포인터입니다. 목록이 비어 있는 경우 목록의 첫 번째 요소에 대한 포인터와 동일합니다.  
  
##  <a name="a-nameinitializerlistinitializerlista--initializerlistinitializerlist"></a><a name="initializer_list__initializer_list"></a>  initializer_list::initializer_list  
 `initializer_list` 형식의 개체를 생성합니다.  
  
```  
constexpr initializer_list() noexcept;
initializer_list(const InputIterator First, const InputIterator Last);
```  
  
### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|`First`|복사할 요소의 범위에서 첫 번째 요소의 위치입니다.|  
|`Last`|복사할 요소의 범위를 벗어나는 첫 번째 요소의 위치입니다.|  
  
### <a name="remarks"></a>설명  
 `initializer_list`는 지정된 형식의 개체 배열을 기반으로 합니다. `initializer_list`를 복사하면 동일한 개체를 가리키는 목록의 두 번째 인스턴스가 생성되고 기본 개체는 복사되지 않습니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// initializer_list_class.cpp  
// compile with: /EHsc  
#include <initializer_list>  
#include <iostream>  
  
int main()  
{  
    using namespace std;  
    // Create an empty initializer_list c0  
    initializer_list <int> c0;  
  
    // Create an initializer_list c1 with 1 element  
    initializer_list <int> c1{ 3 };  
  
    // Create an initializer_list c2 with 5 elements   
    initializer_list <int> c2{ 5, 4, 3, 2, 1 };  
  
    // Create a copy, initializer_list c3, of initializer_list c2  
    initializer_list <int> c3(c2);  
  
    // Create a initializer_list c4 by copying the range c3[ first,  last)  
    const int* c3_ptr = c3.begin();  
    c3_ptr++;  
    c3_ptr++;  
    initializer_list <int> c4(c3.begin(), c3_ptr);  
  
    // Move initializer_list c4 to initializer_list c5  
    initializer_list <int> c5(move(c4));  
  
    cout << "c1 =";  
    for (auto c : c1)  
        cout << " " << c;  
    cout << endl;  
  
    cout << "c2 =";  
    for (auto c : c2)  
        cout << " " << c;  
    cout << endl;  
  
    cout << "c3 =";  
    for (auto c : c3)  
        cout << " " << c;  
    cout << endl;  
  
    cout << "c4 =";  
    for (auto c : c4)  
        cout << " " << c;  
    cout << endl;  
  
    cout << "c5 =";  
    for (auto c : c5)  
        cout << " " << c;  
    cout << endl;  
}  
```  
  
```Output  
c1 = 3c2 = 5 4 3 2 1c3 = 5 4 3 2 1c4 = 5 4c5 = 5 4  
```  
  
##  <a name="a-nameinitializerlistsizea--initializerlistsize"></a><a name="initializer_list__size"></a>  initializer_list::size  
 목록에 있는 요소 수를 반환합니다.  
  
```  
constexpr size_t size() const noexcept;  
```  
  
### <a name="return-value"></a>반환 값  
 목록에 있는 요소의 수입니다.  
  
### <a name="remarks"></a>설명  
  
## <a name="see-also"></a>참고 항목  
 [<forward_list>](../standard-library/forward-list.md)

