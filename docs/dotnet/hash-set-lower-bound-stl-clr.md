---
title: "hash_set::lower_bound(STL/CLR) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "cliext::hash_set::lower_bound"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "lower_bound 멤버[STL/CLR]"
ms.assetid: 54fe8ee5-1977-4192-9cc6-b51e84b03a16
caps.latest.revision: 16
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 14
---
# hash_set::lower_bound(STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Finds beginning of range that matches a specified key.  
  
## 구문  
  
```  
iterator lower_bound(key_type key);  
```  
  
#### 매개 변수  
 key  
 Key value to search for.  
  
## 설명  
 The member function determines the first element `X` in the controlled sequence that hashes to the same bucket as `key` and has equivalent ordering to `key`.  If no such element exists, it returns [hash\_set::end](../dotnet/hash-set-end-stl-clr.md)`()`; otherwise it returns an iterator that designates `X`.  You use it to locate the beginning of a sequence of elements currently in the controlled sequence that match a specified key.  
  
## 예제  
  
```  
// cliext_hash_set_lower_bound.cpp   
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
  
    System::Console::WriteLine("lower_bound(L'x')==end() = {0}",   
        c1.lower_bound(L'x') == c1.end());   
  
    System::Console::WriteLine("*lower_bound(L'a') = {0}",   
        *c1.lower_bound(L'a'));   
    System::Console::WriteLine("*lower_bound(L'b') = {0}",   
        *c1.lower_bound(L'b'));   
    return (0);   
    }  
  
```  
  
  **a b c**  
**lower\_bound\(L'x'\)\=\=end\(\) \= True**  
**\*lower\_bound\(L'a'\) \= a**  
**\*lower\_bound\(L'b'\) \= b**   
## 요구 사항  
 **Header:** \<cliext\/hash\_set\>  
  
 **Namespace:** cliext  
  
## 참고 항목  
 [hash\_set](../dotnet/hash-set-stl-clr.md)   
 [hash\_set::count](../dotnet/hash-set-count-stl-clr.md)   
 [hash\_set::equal\_range](../dotnet/hash-set-equal-range-stl-clr.md)   
 [hash\_set::find](../dotnet/hash-set-find-stl-clr.md)   
 [hash\_set::upper\_bound](../dotnet/hash-set-upper-bound-stl-clr.md)