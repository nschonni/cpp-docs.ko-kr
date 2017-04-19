---
title: "allocator 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- std::allocator
- allocator
- memory/std::allocator
- std.allocator
dev_langs:
- C++
helpviewer_keywords:
- allocator class
ms.assetid: 3fd58076-56cc-43bb-ad58-b4b7c9c6b410
caps.latest.revision: 20
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.mt:
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
ms.sourcegitcommit: 3f69f0c3176d2fbe19e11ce08c071691a72d858d
ms.openlocfilehash: 4c9e2c1acffd7286644ca61a4ef782e7b3a11eef
ms.lasthandoff: 02/24/2017

---
# <a name="allocator-class"></a>allocator 클래스
템플릿 클래스는 **형식** 형식의 개체 배열에 대한 저장소 할당 및 해제를 관리하는 개체를 설명합니다. 클래스 **allocator**의 개체는 C++ 표준 라이브러리의 여러 컨테이너 템플릿 클래스에 대한 생성자에 지정된 기본 할당자 개체입니다.  
  
## <a name="syntax"></a>구문  
  
```  
template <class Type>  
class allocator  
```  
  
#### <a name="parameters"></a>매개 변수  
 *Type*  
 저장소를 할당하거나 할당 취소할 개체의 형식입니다.  
  
## <a name="remarks"></a>설명  
 모든 C++ 표준 템플릿 라이브러리 컨테이너에는 **allocator**로 기본 설정되는 템플릿 매개 변수가 있습니다. 사용자 지정 할당자로 컨테이너를 생성하면 해당 컨테이너 요소의 할당 및 해제를 제어할 수 있습니다.  
  
 예를 들어 할당자 개체에서 전용 힙 또는 공유 메모리에 저장소를 할당하거나, 작거나 큰 개체 크기에 맞게 최적화할 수 있습니다. 또한 제공된 형식 정의를 사용하여 공유 메모리를 관리하는 특수 접근자 개체를 통해 요소에 액세스하거나 자동 가비지 컬렉션을 수행하도록 지정할 수 있습니다. 따라서 할당자 개체를 사용하여 저장소를 할당하는 클래스는 C++ 표준 라이브러리의 컨테이너처럼 이러한 형식을 사용하여 포인터 및 참조 개체를 선언해야 합니다.  
  
 **(C_++98/03만 해당)**할당자 클래스에서 파생시키는 경우 `_Other` typedef에서 새로 파생 클래스를 참조하는 [rebind](#allocator__rebind) 구조체를 제공해야 합니다.  
  
 따라서 할당자는 다음과 같은 형식을 정의합니다.  
  
- [pointer](#allocator__pointer)는 **형식**에 대한 포인터처럼 동작합니다.  
  
- [const_pointer](#allocator__const_pointer)는 **형식**에 대한 const 포인터처럼 동작합니다.  
  
- [reference](#allocator__reference)는 **형식**에 대한 참조처럼 동작합니다.  
  
- [const_reference](#allocator__const_reference)는 **형식**에 대한 const 참조처럼 동작합니다.  
  
 이러한 **형식**은 할당된 요소에 대해 포인터 및 참조를 사용해야 하는 폼을 지정합니다. ([allocator::pointer](#allocator__pointer)는 클래스 **allocator**에 대한 명확한 정의가 있는 경우에도 모든 할당자 개체에 대한 **형식**\*과 동일할 필요가 없습니다.)  
  
 **C++11 이상:** 할당자에서 이동 작업을 사용하려면 최소 할당자 인터페이스를 사용하고 복사 생성자, == 및 != 연산자, 할당 및 할당 취소를 구현하세요. 자세한 내용 및 예제는 [할당자](../standard-library/allocators.md)를 참조하세요.  
  
## <a name="members"></a>멤버  
  
### <a name="constructors"></a>생성자  
  
|||  
|-|-|  
|[allocator](#allocator__allocator)|`allocator` 개체를 만드는 데 사용되는 생성자입니다.|  
  
### <a name="typedefs"></a>Typedefs  
  
|||  
|-|-|  
|[const_pointer](#allocator__const_pointer)|할당자에 의해 관리되는 개체 형식에 대한 상수 포인터를 제공하는 형식입니다.|  
|[const_reference](#allocator__const_reference)|할당자에 의해 관리되는 개체 형식에 대한 상수 참조를 제공하는 형식입니다.|  
|[difference_type](#allocator__difference_type)|할당자에 의해 관리되는 개체 형식에 대한 포인터 값의 차이를 나타낼 수 있는 부호 있는 정수 형식입니다.|  
|[pointer](#allocator__pointer)|할당자에 의해 관리되는 개체 형식에 대한 포인터를 제공하는 형식입니다.|  
|[reference](#allocator__reference)|할당자에 의해 관리되는 개체 형식에 대한 참조를 제공하는 형식입니다.|  
|[size_type](#allocator__size_type)|템플릿 클래스 `allocator`의 개체가 할당할 수 있는 시퀀스의 길이를 나타내는 부호 없는 정수 형식입니다.|  
|[value_type](#allocator__value_type)|할당자에 의해 관리되는 형식입니다.|  
  
### <a name="member-functions"></a>멤버 함수  
  
|||  
|-|-|  
|[address](#allocator__address)|값이 지정된 개체의 주소를 찾습니다.|  
|[allocate](#allocator__allocate)|적어도 지정된 개수의 요소를 저장할 수 있을 만큼 큰 메모리 블록을 할당합니다.|  
|[construct](#allocator__construct)|지정된 값으로 초기화된 특정 형식의 개체를 지정된 주소에 생성합니다.|  
|[deallocate](#allocator__deallocate)|지정된 위치부터 시작하여 저장소에서 지정된 개수의 개체를 해제합니다.|  
|[destroy](#allocator__destroy)|개체가 저장된 메모리 할당을 취소하지 않고 개체 소멸자를 호출합니다.|  
|[max_size](#allocator__max_size)|사용 가능한 메모리를 사용하기 전에 클래스 `allocator`의 개체에서 할당할 수 있는 `Type` 형식의 요소 수를 반환합니다.|  
|[rebind](#allocator__rebind)|한 형식의 개체에 할당자를 사용하여 다른 형식의 개체에 저장소를 할당할 수 있는 구조체입니다.|  
  
### <a name="operators"></a>연산자  
  
|||  
|-|-|  
|[operator=](#allocator__operator_eq)|`allocator` 개체를 다른 `allocator` 개체에 할당합니다.|  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<memory>  
  
 **네임스페이스:** std  
  
##  <a name="a-nameallocatoraddressa--allocatoraddress"></a><a name="allocator__address"></a>  allocator::address  
 값이 지정된 개체의 주소를 찾습니다.  
  
```  
pointer address(reference val) const;
const_pointer address(const_reference val) const;
```  
  
### <a name="parameters"></a>매개 변수  
 ` val`  
 주소를 검색하는 개체의 const 또는 nonconst 값입니다.  
  
### <a name="return-value"></a>반환 값  
 각각 const 또는 nonconst 값으로 발견된 개체에 대한 const 또는 nonconst 포인터입니다.  
  
### <a name="remarks"></a>설명  
 멤버 함수는 할당된 요소에 대해 포인터가 가져야 하는 형식으로 ` val`의 주소를 반환합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// allocator_address.cpp  
// compile with: /EHsc  
#include <memory>  
#include <algorithm>  
#include <iostream>  
#include <vector>  
  
using namespace std;  
  
int main( )   
{  
   vector <int> v1;  
   vector <int>::iterator v1Iter;  
   vector <int>:: allocator_type v1Alloc;  
  
   int i;  
   for ( i = 1 ; i <= 7 ; i++ )  
   {  
      v1.push_back( 2 * i );  
   }  
  
   cout << "The original vector v1 is:\n ( " ;  
   for ( v1Iter = v1.begin( ) ; v1Iter != v1.end( ) ; v1Iter++ )  
      cout << *v1Iter << " ";  
   cout << ")." << endl;  
  
   allocator<int>::const_pointer v1Ptr;  
   const int k = 8;  
   v1Ptr = v1Alloc.address( *find(v1.begin( ), v1.end( ), k) );  
   // v1Ptr = v1Alloc.address( k );  
   cout << "The integer addressed by v1Ptr has a value of: "  
        << "*v1Ptr = " << *v1Ptr << "." << endl;  
}  
```  
  
```Output  
The original vector v1 is:  
 ( 2 4 6 8 10 12 14 ).  
The integer addressed by v1Ptr has a value of: *v1Ptr = 8.  
```  
  
##  <a name="a-nameallocatorallocatea--allocatorallocate"></a><a name="allocator__allocate"></a>  allocator::allocate  
 적어도 지정된 개수의 요소를 저장할 수 있을 만큼 큰 메모리 블록을 할당합니다.  
  
```  
pointer allocate(size_type count, const void* _Hint);
```  
  
### <a name="parameters"></a>매개 변수  
 ` count`  
 충분한 저장소를 할당해야 할 요소의 수입니다.  
  
 *_Hint*  
 할당자 개체를 지원할 수 있는 const 포인터는 요청 이전에 할당된 개체의 주소를 찾음으로써 저장소의 요청을 충족시킵니다.  
  
### <a name="return-value"></a>반환 값  
 할당된 개체에 대한 포인터이거나, 메모리가 할당되지 않은 경우 null입니다.  
  
### <a name="remarks"></a>설명  
 멤버 함수는 연산자 new(` count`)를 호출함으로써 **Type** 형식의 count 요소 배열에 대한 저장소를 할당합니다. 할당된 개체에 대한 포인터를 반환합니다. 힌트 인수는 일부 할당자의 참조 지역성 개선에 도움이 됩니다. 동일한 할당자 개체에 의해 이미 할당되었지만 아직 할당 취소되지 않은 개체의 주소가 유효한 선택입니다. 힌트를 제공하지 않으려면 null 포인터 인수를 대신 사용합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// allocator_allocate.cpp  
// compile with: /EHsc  
#include <memory>  
#include <iostream>  
#include <vector>  
  
using namespace std;  
  
int main( )   
{  
   allocator<int> v1Alloc;    
   allocator<int>::pointer v1aPtr;    
   v1aPtr = v1Alloc.allocate ( 10 );  
  
   int i;  
   for ( i = 0 ; i < 10 ; i++ )  
   {  
      v1aPtr[ i ] = i;  
   }  
  
   for ( i = 0 ; i < 10 ; i++ )  
   {  
      cout << v1aPtr[ i ] << " ";  
   }  
   cout << endl;    
   v1Alloc.deallocate( v1aPtr, 10 );  
}  
```  
  
```Output  
0 1 2 3 4 5 6 7 8 9   
```  
  
##  <a name="a-nameallocatorallocatora--allocatorallocator"></a><a name="allocator__allocator"></a>  allocator::allocator  
 할당자 개체를 만드는 데 사용되는 생성자입니다.  
  
```  
allocator();
allocator(const allocator<Type>& right);
template <class Other>  
allocator(const allocator<Other>& right);
```  
  
### <a name="parameters"></a>매개 변수  
 ` right`  
 복사할 할당자 개체입니다.  
  
### <a name="remarks"></a>설명  
 생성자는 아무 작업도 수행하지 않습니다. 그러나 일반적으로 다른 할당자 개체로부터 구성된 할당자 개체는 비교 시 같아야 하며, 두 할당자 개체 간에 개체 할당 및 해제를 서로 혼합할 수 있어야 합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// allocator_allocator.cpp  
// compile with: /EHsc  
#include <memory>  
#include <iostream>  
#include <vector>  
  
using namespace std;  
  
class Int {  
public:  
   Int( int i )   
   {  
      cout << "Constructing " << ( void* )this  << endl;   
      x = i;  
      bIsConstructed = true;  
   };  
   ~Int( )   
   {  
      cout << "Destructing " << ( void* )this << endl;   
      bIsConstructed = false;  
   };  
   Int &operator++( )   
   {  
      x++;  
      return *this;  
   };  
   int x;  
private:  
   bool bIsConstructed;  
};  
  
int main( )   
{  
   allocator<double> Alloc;  
   vector <Int>:: allocator_type v1Alloc;  
  
   allocator<double> cAlloc(Alloc);   
   allocator<Int> cv1Alloc(v1Alloc);  
  
   if ( cv1Alloc == v1Alloc )  
      cout << "The allocator objects cv1Alloc & v1Alloc are equal."  
           << endl;  
   else  
      cout << "The allocator objects cv1Alloc & v1Alloc are not equal."  
           << endl;  
  
   if ( cAlloc == Alloc )  
      cout << "The allocator objects cAlloc & Alloc are equal."  
           << endl;  
   else  
      cout << "The allocator objects cAlloc & Alloc are not equal."  
           << endl;  
}  
```  
  
```Output  
The allocator objects cv1Alloc & v1Alloc are equal.  
The allocator objects cAlloc & Alloc are equal.  
```  
  
##  <a name="a-nameallocatorconstpointera--allocatorconstpointer"></a><a name="allocator__const_pointer"></a>  allocator::const_pointer  
 할당자에 의해 관리되는 개체 형식에 대한 상수 포인터를 제공하는 형식입니다.  
  
```  
typedef const value_type *const_pointer;  
```  
  
### <a name="remarks"></a>설명  
 포인터 형식은 템플릿 클래스 할당자의 개체가 할당할 수 있는 const 개체를 **\*ptr** 식을 통해 지정할 수 있는 **ptr** 개체를 설명합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// allocator_const_ptr.cpp  
// compile with: /EHsc  
#include <memory>  
#include <iostream>  
#include <vector>  
  
using namespace std;  
  
int main( )   
{  
   vector <int> v1;  
   vector <int>::iterator v1Iter;  
   vector <int>:: allocator_type v1Alloc;  
  
   int i;  
   for ( i = 1 ; i <= 7 ; i++ )  
   {  
      v1.push_back( i * 2 );  
   }  
  
   cout << "The original vector v1 is:\n ( " ;  
   for ( v1Iter = v1.begin( ) ; v1Iter != v1.end( ) ; v1Iter++ )  
      cout << *v1Iter << " ";  
   cout << ")." << endl;  
  
   allocator<int>::const_pointer v1Ptr;  
   const int k = 10;  
   v1Ptr = v1Alloc.address( k );  
  
   cout << "The integer's address found has a value of: "  
        << *v1Ptr << "." << endl;  
}  
```  
  
```Output  
The original vector v1 is:  
 ( 2 4 6 8 10 12 14 ).  
The integer's address found has a value of: 10.  
```  
  
##  <a name="a-nameallocatorconstreferencea--allocatorconstreference"></a><a name="allocator__const_reference"></a>  allocator::const_reference  
 할당자에 의해 관리되는 개체 형식에 대한 상수 참조를 제공하는 형식입니다.  
  
```  
typedef const value_type& const_reference;  
```  
  
### <a name="remarks"></a>설명  
 참조 형식은 템플릿 클래스 할당자의 개체가 할당할 수 있는 const 개체를 지정할 수 있는 개체를 설명합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// allocator_const_ref.cpp  
// compile with: /EHsc  
#include <memory>  
#include <iostream>  
#include <vector>  
  
using namespace std;  
  
int main( )   
{  
   vector <double> v;  
   vector <double> ::iterator vIter, vfIter;  
   vector <double> :: allocator_type vAlloc;  
  
   int j;  
   for ( j = 1 ; j <= 7 ; j++ )  
   {  
      v.push_back( 100.0 * j );  
   }  
  
   cout << "The original vector v is:\n ( " ;  
   for ( vIter = v.begin( ) ; vIter != v.end( ) ; vIter++ )  
      cout << *vIter << " ";  
   cout << ")." << endl;  
  
   vfIter = v.begin( );  
   allocator<double>::const_reference vcref =*vfIter;  
   cout << "The value of the element referred to by vref is: "  
        << vcref << ",\n the first element in the vector." << endl;  
  
   // const references can have their elements modified,  
   // so the following would generate an error:  
   // vcref = 150;  
   // but the value of the first element could be modified through  
   // its nonconst iterator and the const reference would remain valid  
 *vfIter = 175;  
   cout << "The value of the element referred to by vcref,"  
        <<"\n after nofication through its nonconst iterator, is: "  
        << vcref << "." << endl;  
}  
```  
  
```Output  
The original vector v is:  
 ( 100 200 300 400 500 600 700 ).  
The value of the element referred to by vref is: 100,  
 the first element in the vector.  
The value of the element referred to by vcref,  
 after nofication through its nonconst iterator, is: 175.  
```  
  
##  <a name="a-nameallocatorconstructa--allocatorconstruct"></a><a name="allocator__construct"></a>  allocator::construct  
 지정된 값으로 초기화된 특정 형식의 개체를 지정된 주소에 생성합니다.  
  
```  
void construct(pointer ptr, const Type& val);
void construct(pointer ptr, Type&& val);
template <class _Other>  
void construct(pointer ptr, _Other&&...   val);
```  
  
### <a name="parameters"></a>매개 변수  
 ` ptr`  
 개체를 생성할 위치에 대한 포인터입니다.  
  
 ` val`  
 생성되는 개체를 초기화할 값입니다.  
  
### <a name="remarks"></a>설명  
 첫 번째 멤버 함수는 **new** ( ( `void` \*) ` ptr` ) **Type** ( ` val` )과 등가입니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// allocator_construct.cpp  
// compile with: /EHsc  
#include <memory>  
#include <iostream>  
#include <algorithm>  
#include <vector>  
  
using namespace std;  
  
int main( )   
{  
   vector <int> v1;  
   vector <int>::iterator v1Iter;  
   vector <int>:: allocator_type v1Alloc;  
  
   int i;  
   for ( i = 1 ; i <= 7 ; i++ )  
   {  
      v1.push_back( 3 * i );  
   }  
  
   cout << "The original vector v1 is:\n ( " ;  
   for ( v1Iter = v1.begin( ) ; v1Iter != v1.end( ) ; v1Iter++ )  
      cout << *v1Iter << " ";  
   cout << ")." << endl;  
  
   allocator<int>::pointer v1PtrA;  
   int kA = 6, kB = 7;  
   v1PtrA = v1Alloc.address( *find( v1.begin( ), v1.end( ), kA ) );  
   v1Alloc.destroy ( v1PtrA );  
   v1Alloc.construct ( v1PtrA , kB );  
  
   cout << "The modified vector v1 is:\n ( " ;  
   for ( v1Iter = v1.begin( ) ; v1Iter != v1.end( ) ; v1Iter++ )  
      cout << *v1Iter << " ";  
   cout << ")." << endl;  
}  
```  
  
```Output  
The original vector v1 is:  
 ( 3 6 9 12 15 18 21 ).  
The modified vector v1 is:  
 ( 3 7 9 12 15 18 21 ).  
```  
  
##  <a name="a-nameallocatordeallocatea--allocatordeallocate"></a><a name="allocator__deallocate"></a>  allocator::deallocate  
 지정된 위치부터 시작하여 저장소에서 지정된 개수의 개체를 해제합니다.  
  
```  
void deallocate(pointer ptr, size_type count);
```  
  
### <a name="parameters"></a>매개 변수  
 ` ptr`  
 저장소에서 할당을 취소할 첫 번째 개체에 대한 포인터입니다.  
  
 ` count`  
 저장소에서 할당을 취소할 개체의 수입니다.  
  
### <a name="remarks"></a>설명  
 멤버 함수는 `operator delete`(` ptr`)를 호출하여 ` ptr`에서 시작하는 **Type** 형식의 count 개체 배열에 대한 저장소를 해제합니다. **\*이것**과 같은지를 비교하는 할당자 개체에 대해 [allocate](#allocator__allocate)를 호출하고 같은 크기와 형식의 배열 개체를 할당하여 ` ptr` 포인터가 이미 반환된 상태여야 합니다. `deallocate`은 예외를 throw할 수 없습니다.  
  
### <a name="example"></a>예제  
  멤버 함수 사용의 예제를 보려면 [allocator::allocate](#allocator__allocate)를 참조하세요.  
  
##  <a name="a-nameallocatordestroya--allocatordestroy"></a><a name="allocator__destroy"></a>  allocator::destroy  
 개체가 저장된 메모리 할당을 취소하지 않고 개체 소멸자를 호출합니다.  
  
```  
void destroy(pointer ptr);
```  
  
### <a name="parameters"></a>매개 변수  
 ` ptr`  
 소멸될 개체의 주소를 지정하는 포인터입니다.  
  
### <a name="remarks"></a>설명  
 멤버 함수는 ` ptr` -> **Type**:: **~Type** 소멸자를 호출함으로써 ` ptr`에 의해 지정된 개체를 소멸시킵니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// allocator_destroy.cpp  
// compile with: /EHsc  
#include <memory>  
#include <iostream>  
#include <algorithm>  
#include <vector>  
  
using namespace std;  
  
int main( )   
{  
   vector <int> v1;  
   vector <int>::iterator v1Iter;  
   vector <int>:: allocator_type v1Alloc;  
  
   int i;  
   for ( i = 1 ; i <= 7 ; i++ )  
   {  
      v1.push_back( 2 * i );  
   }  
  
   cout << "The original vector v1 is:\n ( " ;  
   for ( v1Iter = v1.begin( ) ; v1Iter != v1.end( ) ; v1Iter++ )  
      cout << *v1Iter << " ";  
   cout << ")." << endl;  
  
   allocator<int>::pointer v1PtrA;  
   int kA = 12, kB = -99;  
   v1PtrA = v1Alloc.address( *find(v1.begin( ), v1.end( ), kA) );  
   v1Alloc.destroy ( v1PtrA );  
   v1Alloc.construct ( v1PtrA , kB );  
  
   cout << "The modified vector v1 is:\n ( " ;  
   for ( v1Iter = v1.begin( ) ; v1Iter != v1.end( ) ; v1Iter++ )  
      cout << *v1Iter << " ";  
   cout << ")." << endl;  
}  
```  
  
```Output  
The original vector v1 is:  
 ( 2 4 6 8 10 12 14 ).  
The modified vector v1 is:  
 ( 2 4 6 8 10 -99 14 ).  
```  
  
##  <a name="a-nameallocatordifferencetypea--allocatordifferencetype"></a><a name="allocator__difference_type"></a>  allocator::difference_type  
 할당자에 의해 관리되는 개체 형식에 대한 포인터 값의 차이를 나타낼 수 있는 부호 있는 정수 형식입니다.  
  
```  
typedef ptrdiff_t difference_type;  
```  
  
### <a name="remarks"></a>설명  
 부호 있는 정수 형식은 템플릿 클래스 할당자의 개체가 할당할 수 있는 시퀀스에서 두 요소의 주소 간 차이점을 나타낼 수 있는 개체를 설명합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// allocator_diff_type.cpp  
// compile with: /EHsc  
#include <memory>  
#include <iostream>  
#include <vector>  
  
using namespace std;  
  
int main( )   
{  
   vector <int> v1;  
   vector <int>::iterator v1Iter;  
   vector <int>:: allocator_type v1Alloc;  
  
   int i;  
   for ( i = 0 ; i <= 7 ; i++ )  
   {  
      v1.push_back( i * 2 );  
   }  
  
   cout << "The original vector v1 is:\n ( " ;  
   for ( v1Iter = v1.begin( ) ; v1Iter != v1.end( ) ; v1Iter++ )  
      cout << *v1Iter << " ";  
   cout << ")." << endl;  
  
   allocator<int>::const_pointer v1PtrA, v1PtrB;  
   const int kA = 4, kB =12;  
   v1PtrA = v1Alloc.address( kA );  
   v1PtrB = v1Alloc.address( kB );  
   allocator<int>::difference_type v1diff = *v1PtrB - *v1PtrA;  
  
   cout << "Pointer v1PtrA addresses " << *v1PtrA << "." << endl;  
   cout << "Pointer v1PtrB addresses " << *v1PtrB <<  "." << endl;  
   cout << "The difference between the integer's addresses is: "  
        << v1diff << "." << endl;  
}  
```  
  
```Output  
The original vector v1 is:  
 ( 0 2 4 6 8 10 12 14 ).  
Pointer v1PtrA addresses 4.  
Pointer v1PtrB addresses 12.  
The difference between the integer's addresses is: 8.  
```  
  
##  <a name="a-nameallocatormaxsizea--allocatormaxsize"></a><a name="allocator__max_size"></a>  allocator::max_size  
 사용 가능한 메모리가 모두 사용되기 전에 allocator 클래스의 개체가 할당할 수 있는 **Type** 형식의 요소 수를 반환합니다.  
  
```  
size_type max_size() const;
```  
  
### <a name="return-value"></a>반환 값  
 할당할 수 있는 요소의 수입니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// allocator_max_size.cpp  
// compile with: /EHsc  
#include <memory>  
#include <iostream>  
#include <vector>  
  
using namespace std;  
  
int main( )   
{  
   vector <int> v1;  
   vector <int>::iterator v1Iter;  
   vector <int>:: allocator_type v1Alloc;  
  
   int i;  
   for ( i = 1 ; i <= 7 ; i++ )  
   {  
      v1.push_back( i );  
   }  
  
   cout << "The original vector v1 is:\n ( " ;  
   for ( v1Iter = v1.begin( ) ; v1Iter != v1.end( ) ; v1Iter++ )  
      cout << *v1Iter << " ";  
   cout << ")." << endl;  
  
   vector <double> v2;  
   vector <double> ::iterator v2Iter;  
   vector <double> :: allocator_type v2Alloc;  
   allocator<int>::size_type v1size;  
   v1size = v1Alloc.max_size( );  
  
   cout << "The number of integers that can be allocated before\n"  
        << " the free memory in the vector v1 is used up is: "  
        << v1size << "." << endl;  
  
   int ii;  
   for ( ii = 1 ; ii <= 7 ; ii++ )  
   {  
      v2.push_back( ii * 10.0 );  
   }  
  
   cout << "The original vector v2 is:\n ( " ;  
   for ( v2Iter = v2.begin( ) ; v2Iter != v2.end( ) ; v2Iter++ )  
      cout << *v2Iter << " ";  
   cout << ")." << endl;  
   allocator<double>::size_type v2size;  
   v2size = v2Alloc.max_size( );  
  
   cout << "The number of doubles that can be allocated before\n"  
        << " the free memory in the vector v2 is used up is: "  
        << v2size << "." << endl;  
}  
```  
  
##  <a name="a-nameallocatoroperatoreqa--allocatoroperator"></a><a name="allocator__operator_eq"></a>  allocator::operator=  
 한 할당자 개체를 다른 할당자 개체에 할당합니다.  
  
```  
template <class Other>  
allocator<Type>& operator=(const allocator<Other>& right);
```  
  
### <a name="parameters"></a>매개 변수  
 ` right`  
 다른 할당자 개체에 할당할 할당자 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 할당자 개체에 대한 참조  
  
### <a name="remarks"></a>설명  
 템플릿 대입 연산자는 아무것도 수행하지 않습니다. 그러나 일반적으로 다른 할당자 개체에 할당된 할당자 개체는 비교 시 같아야 하며, 두 할당자 개체 간에 개체 할당 및 해제를 서로 혼합할 수 있어야 합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// allocator_op_assign.cpp  
// compile with: /EHsc  
#include <memory>  
#include <iostream>  
#include <vector>  
  
using namespace std;  
  
class Int {  
public:  
   Int(int i)   
   {  
      cout << "Constructing " << ( void* )this  << endl;   
      x = i;  
      bIsConstructed = true;  
   };  
   ~Int( ) {  
      cout << "Destructing " << ( void* )this << endl;   
      bIsConstructed = false;  
   };  
   Int &operator++( )   
   {  
      x++;  
      return *this;  
   };  
   int x;  
private:  
   bool bIsConstructed;  
};  
  
int main( )   
{  
   allocator<Int> Alloc;  
   allocator<Int> cAlloc ;  
   cAlloc = Alloc;      
}  
```  
  
##  <a name="a-nameallocatorpointera--allocatorpointer"></a><a name="allocator__pointer"></a>  allocator::pointer  
 할당자에 의해 관리되는 개체 형식에 대한 포인터를 제공하는 형식입니다.  
  
```  
typedef value_type *pointer;  
```  
  
### <a name="remarks"></a>설명  
 포인터 형식은 템플릿 클래스 할당자의 개체가 할당할 수 있는 개체를 **\*ptr** 식을 통해 지정할 수 있는 **ptr** 개체를 설명합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// allocator_ptr.cpp  
// compile with: /EHsc  
#include <memory>  
#include <iostream>  
#include <vector>  
  
using namespace std;  
  
int main( )   
{  
   vector <int> v1;  
   vector <int>::iterator v1Iter;  
   vector <int>:: allocator_type v1Alloc;  
  
   int i;  
   for ( i = 1 ; i <= 7 ; i++ )  
   {  
      v1.push_back( 3 * i );  
   }  
  
   cout << "The original vector v1 is:\n ( " ;  
   for ( v1Iter = v1.begin( ) ; v1Iter != v1.end( ) ; v1Iter++ )  
      cout << *v1Iter << " ";  
   cout << ")." << endl;  
  
   allocator<int>::const_pointer v1Ptr;  
   const int k = 12;  
   v1Ptr = v1Alloc.address( k );  
  
   cout << "The integer addressed by v1Ptr has a value of: "  
        << "*v1Ptr = " << *v1Ptr << "." << endl;     
}  
```  
  
```Output  
The original vector v1 is:  
 ( 3 6 9 12 15 18 21 ).  
The integer addressed by v1Ptr has a value of: *v1Ptr = 12.  
```  
  
##  <a name="a-nameallocatorrebinda--allocatorrebind"></a><a name="allocator__rebind"></a>  allocator::rebind  
 한 형식의 개체에 할당자를 사용하여 다른 형식의 개체에 저장소를 할당할 수 있는 구조체입니다.  
```  
struct rebind {    typedef allocator<_Other> other ;    };  
```  
### <a name="parameters"></a>매개 변수  
 *other*  
 메모리를 할당 중인 요소의 형식입니다.  
  
### <a name="remarks"></a>설명  
 이 구조체는 구현 중인 컨테이너의 요소 형식과는 다른 형식의 메모리를 할당하는 데 유용합니다.  
  
 멤버 템플릿 클래스는 other 형식을 정의합니다. 형식 이름 **allocator**\< **Type**>이 지정되면 형식 이름 **allocator**\<_ **Other**>를 제공하는 것이 유일한 목적입니다.  
  
 예를 들어 형식 **A**의 할당자 개체 **al**이 지정되면 다음 식으로 형식 **_Other**의 개체를 할당할 수 있습니다.  
  
```  
A::rebind<Other>::other(al).allocate(1, (Other *)0)  
```  
  
 또는 다음과 같은 형식을 작성하여 포인터 형식의 이름을 지정할 수 있습니다.  
  
```  
A::rebind<Other>::other::pointer  
```  
  
### <a name="example"></a>예제  
  
```cpp  
// allocator_rebind.cpp  
// compile with: /EHsc  
#include <memory>  
#include <iostream>  
#include <algorithm>  
#include <vector>  
  
using namespace std;  
  
typedef vector<int>::allocator_type IntAlloc;  
int main( )   
{  
   IntAlloc v1Iter;  
   vector<int> v1;  
  
   IntAlloc::rebind<char>::other::pointer pszC =  
      IntAlloc::rebind<char>::other(v1.get_allocator()).allocate(1, (void *)0);  
  
   int * pInt = v1Iter.allocate(10);  
}  
```  
  
##  <a name="a-nameallocatorreferencea--allocatorreference"></a><a name="allocator__reference"></a>  allocator::reference  
 할당자에 의해 관리되는 개체 형식에 대한 참조를 제공하는 형식입니다.  
  
```  
typedef value_type& reference;  
```  
  
### <a name="remarks"></a>설명  
 참조 형식은 템플릿 클래스 할당자의 개체가 할당할 수 있는 개체를 지정할 수 있는 개체를 설명합니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// allocator_reference.cpp  
// compile with: /EHsc  
#include <memory>  
#include <iostream>  
#include <vector>  
  
using namespace std;  
  
int main( )   
{  
   vector <double> v;  
   vector <double> ::iterator vIter, vfIter;  
   vector <double> :: allocator_type vAlloc;  
  
   int j;  
   for ( j = 1 ; j <= 7 ; j++ )  
   {  
      v.push_back( 100.0 * j );  
   }  
  
   cout << "The original vector v is:\n ( " ;  
   for ( vIter = v.begin( ) ; vIter != v.end( ) ; vIter++ )  
      cout << *vIter << " ";  
   cout << ")." << endl;  
  
   vfIter = v.begin( );  
   allocator<double>::reference vref =*vfIter;  
   cout << "The value of the element referred to by vref is: "  
        << vref << ",\n the first element in the vector." << endl;  
  
   // nonconst references can have their elements modified  
   vref = 150;  
   cout << "The element referred to by vref after being modified is: "  
        << vref << "." << endl;  
}  
```  
  
```Output  
The original vector v is:  
 ( 100 200 300 400 500 600 700 ).  
The value of the element referred to by vref is: 100,  
 the first element in the vector.  
The element referred to by vref after being modified is: 150.  
```  
  
##  <a name="a-nameallocatorsizetypea--allocatorsizetype"></a><a name="allocator__size_type"></a>  allocator::size_type  
 템플릿 클래스 할당자의 개체가 할당할 수 있는 시퀀스의 길이를 나타내는 부호 없는 정수 형식입니다.  
  
```  
typedef size_t size_type;  
```  
  
### <a name="example"></a>예제  
  
```cpp  
// allocator_size_type.cpp  
// compile with: /EHsc  
#include <memory>  
#include <iostream>  
#include <vector>  
  
using namespace std;  
  
int main( )  
{  
   vector <double> v;  
   vector <double> ::iterator vIter;  
   vector <double> :: allocator_type vAlloc;  
  
   int j;  
   for ( j = 1 ; j <= 7 ; j++ )  
   {  
      v.push_back( 100.0 * j );  
   }  
  
   cout << "The original vector v is:\n ( " ;  
   for ( vIter = v.begin( ) ; vIter != v.end( ) ; vIter++ )  
      cout << *vIter << " ";  
   cout << ")." << endl;  
  
   allocator<double>::size_type vsize;  
   vsize = vAlloc.max_size( );  
  
   cout << "The number of doubles that can be allocated before\n"  
        << " the free memory in the vector v is used up is: "  
        << vsize << "." << endl;  
}  
```  
  
##  <a name="a-nameallocatorvaluetypea--allocatorvaluetype"></a><a name="allocator__value_type"></a>  allocator::value_type  
 할당자에 의해 관리되는 형식입니다.  
  
```  
typedef Type value_type;  
```  
  
### <a name="remarks"></a>설명  
 이 형식은 템플릿 매개 변수 **Type**과 동일한 의미입니다.  
  
### <a name="example"></a>예제  
  
```cpp  
// allocator_value_type.cpp  
// compile with: /EHsc  
#include <memory>  
#include <iostream>  
#include <vector>  
using namespace std;  
  
int main( )   
{  
   vector <double> v;  
   vector <double> ::iterator vIter, vfIter;  
   vector <double> :: allocator_type vAlloc;  
  
   int j;  
   for ( j = 1 ; j <= 7 ; j++ )  
   {  
      v.push_back( 100.0 * j );  
   }  
  
   cout << "The original vector v is:\n ( " ;  
   for ( vIter = v.begin( ) ; vIter != v.end( ) ; vIter++ )  
      cout << *vIter << " ";  
   cout << ")." << endl;  
  
   vfIter = v.begin( );  
   allocator<double>::value_type vecVal = 150.0;  
 *vfIter = vecVal;  
   cout << "The value of the element addressed by vfIter is: "  
        << *vfIter << ",\n the first element in the vector." << endl;  
  
   cout << "The modified vector v is:\n ( " ;  
   for ( vIter = v.begin( ) ; vIter != v.end( ) ; vIter++ )  
      cout << *vIter << " ";  
   cout << ")." << endl;  
}  
```  
  
```Output  
The original vector v is:  
 ( 100 200 300 400 500 600 700 ).  
The value of the element addressed by vfIter is: 150,  
 the first element in the vector.  
The modified vector v is:  
 ( 150 200 300 400 500 600 700 ).  
```  
  
## <a name="see-also"></a>참고 항목  
 [C++ 표준 라이브러리의 스레드 보안](../standard-library/thread-safety-in-the-cpp-standard-library.md)

