---
title: "hash_set::erase(STL/CLR) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "cliext::hash_set::erase"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "erase 멤버[STL/CLR]"
ms.assetid: 620998a0-00c9-4be6-899b-2d71661375b6
caps.latest.revision: 16
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 14
---
# hash_set::erase(STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

지정된 위치에 있는 요소를 제거합니다.  
  
## 구문  
  
```  
iterator erase(iterator where);  
iterator erase(iterator first, iterator last);  
bool erase(key_type key)  
```  
  
#### 매개 변수  
 first  
 Beginning of range to erase.  
  
 key  
 Key value to erase.  
  
 last  
 End of range to erase.  
  
 where  
 Element to erase.  
  
## 설명  
 The first member function removes the element of the controlled sequence pointed to by `where`, and returns an iterator that designates the first element remaining beyond the element removed, or [hash\_set::end](../dotnet/hash-set-end-stl-clr.md)`()` if no such element exists.  You use it to remove a single element.  
  
 The second member function removes the elements of the controlled sequence in the range `[``first``,` `last``)`, and returns an iterator that designates the first element remaining beyond any elements removed, or `end()` if no such element exists..  You use it to remove zero or more contiguous elements.  
  
 The third member function removes any element of the controlled sequence whose key has equivalent ordering to `key`, and returns a count of the number of elements removed.  You use it to remove and count all elements that match a specified key.  
  
 Each element erasure takes time proportional to the logarithm of the number of elements in the controlled sequence.  
  
## 예제  
  
```  
// cliext_hash_set_erase.cpp   
// compile with: /clr   
#include <cliext/hash_set>   
  
typedef cliext::hash_set<wchar_t> Myhash_set;   
int main()   
    {   
    Myhash_set c1;   
    c1.insert(L'a');   
    c1.insert(L'b');   
    c1.insert(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// erase an element and reinspect   
    System::Console::WriteLine("erase(begin()) = {0}",   
        *c1.erase(c1.begin()));   
  
// add elements and display " b c d e"   
    c1.insert(L'd');   
    c1.insert(L'e');   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// erase all but end   
    Myhash_set::iterator it = c1.end();   
    System::Console::WriteLine("erase(begin(), end()-1) = {0}",   
        *c1.erase(c1.begin(), --it));   
    System::Console::WriteLine("size() = {0}", c1.size());   
    return (0);   
    }  
  
```  
  
  **a b c**  
**erase\(begin\(\)\) \= b**  
 **b c d e**  
**erase\(begin\(\), end\(\)\-1\) \= e**  
**size\(\) \= 1**   
## 요구 사항  
 **Header:** \<cliext\/hash\_set\>  
  
 **Namespace:** cliext  
  
## 참고 항목  
 [hash\_set](../dotnet/hash-set-stl-clr.md)   
 [hash\_set::clear](../dotnet/hash-set-clear-stl-clr.md)