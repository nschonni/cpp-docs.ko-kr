---
title: "&lt;codecvt&gt; 열거형 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 46a8b073-01bc-46d3-b3d3-a8540f9422c1
caps.latest.revision: 10
manager: ghogen
translationtype: Machine Translation
ms.sourcegitcommit: 3168772cbb7e8127523bc2fc2da5cc9b4f59beb8
ms.openlocfilehash: 21162b7c25e09f2f77d2da1f4ee7797e68ec1e94
ms.lasthandoff: 02/24/2017

---
# <a name="ltcodecvtgt-enums"></a>&lt;codecvt&gt; 열거형
  
##  <a name="a-namecodecvtmodeenumerationa--codecvtmode-enumeration"></a><a name="codecvt_mode_enumeration"></a>  codecvt_mode 열거형  
 [로캘](../standard-library/locale-class.md) 패싯에 대한 구성 정보를 지정합니다.  
  
```  
enum codecvt_mode {  
    consume_header = 4,  
    generate_header = 2,  
    little_endian = 1  
 };  
```  
  
### <a name="remarks"></a>설명  
 열거형은 [\<codecvt>](../standard-library/codecvt.md)에 선언된 로캘 패싯에 구성 정보를 제공하는 세 개의 상수를 정의합니다. 고유 값은 다음과 같습니다.  
  
- `consume_header` - 멀티바이트 시퀀스를 읽을 때 초기 헤더 시퀀스를 사용하고, 읽을 후속 멀티바이트 시퀀스의 엔디언(Endianness)을 결정할 경우  
  
- `generate_header` - 멀티바이트 시퀀스를 작성할 때 초기 헤더 시퀀스를 생성하고, 작성할 후속 멀티바이트 시퀀스의 엔디언(Endianness)을 보급할 경우  
  
- `little_endian` - 기본 big endian 순서와는 대조적으로 little endian 순서로 멀티바이트 시퀀스를 생성할 경우  
  
 이러한 상수는 임의 조합에서 함께 OR 처리될 수 있습니다.  
  
## <a name="see-also"></a>참고 항목  
 [\<codecvt>](../standard-library/codecvt.md)

