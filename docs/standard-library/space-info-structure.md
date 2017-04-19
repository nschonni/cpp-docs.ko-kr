---
title: "space_info 구조체 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- filesystem/std::tr2::sys::space_info
dev_langs:
- C++
ms.assetid: f2b35b42-06ff-45bd-8617-39a0f5358a54
caps.latest.revision: 13
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
ms.sourcegitcommit: 3168772cbb7e8127523bc2fc2da5cc9b4f59beb8
ms.openlocfilehash: 77314d99a34f109e556b8583b06ce51acce288bc
ms.lasthandoff: 02/24/2017

---
# <a name="spaceinfo-structure"></a>space_info 구조체
볼륨에 대한 정보를 보관합니다.  
  
## <a name="syntax"></a>구문  
  
```  
struct space_info    {
    uintmax_t capacity;
    uintmax_t free;
    uintmax_t available;
    };  
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-data-members"></a>공용 데이터 멤버  
  
|이름|설명|  
|----------|-----------------|  
|`unsigned long long available`|볼륨의 데이터를 나타내는 데 사용할 수 있는 바이트 수를 나타냅니다.|  
|`unsigned long long capacity`|볼륨이 나타낼 수 있는 총 바이트 수를 나타냅니다.|  
|`unsigned long long free`|볼륨의 데이터를 나타내는 데 사용되지 않는 바이트 수를 나타냅니다.|  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** filesystem  
  
 **네임스페이스:** std::experimental::filesystem  
  
## <a name="see-also"></a>참고 항목  
 [헤더 파일 참조](../standard-library/cpp-standard-library-header-files.md)   
 [\<filesystem>](../standard-library/filesystem.md)   
 [space 함수](http://msdn.microsoft.com/en-us/7fce0b0e-523b-4598-b218-47245d0204ca)   
 [파일 시스템 탐색(C++)](../standard-library/file-system-navigation.md)

