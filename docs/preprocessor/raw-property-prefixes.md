---
title: raw_property_prefixes | Microsoft Docs
ms.custom: ''
ms.date: 10/18/2018
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- raw_property_prefixes
dev_langs:
- C++
helpviewer_keywords:
- raw_property_prefixes attribute
ms.assetid: 03a0f48c-c460-4175-a762-9f7f8d84b12f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1170440428a5c92e383152826827989d602e69fb
ms.sourcegitcommit: 0164af5615389ffb1452ccc432eb55f6dc931047
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49808747"
---
# <a name="rawpropertyprefixes"></a>raw_property_prefixes

**C + + 전용**

세 가지 속성 메서드의 대체 접두사를 지정합니다.

## <a name="syntax"></a>구문

```
raw_property_prefixes("GetPrefix","PutPrefix","PutRefPrefix")
```

### <a name="parameters"></a>매개 변수

*GetPrefix*<br/>
에 사용할 접두사를 `propget` 메서드.

*PutPrefix*<br/>
에 사용할 접두사를 `propput` 메서드.

*PutRefPrefix*<br/>
에 사용할 접두사를 `propputref` 메서드.

## <a name="remarks"></a>설명

기본적으로 낮은 수준의 `propget`, `propput`, 및 `propputref` 메서드는 접두사를 사용 하 여 명명 된 멤버 함수에 의해 노출 됩니다 **get_** 를 **put_**, 및 **putref_** 각각. 이 접두사는 MIDL로 생성한 헤더 파일에 사용되는 이름과 호환됩니다.

**C + + 전용 종료**

## <a name="see-also"></a>참고 항목

[#import 특성](../preprocessor/hash-import-attributes-cpp.md)<br/>
[#import 지시문](../preprocessor/hash-import-directive-cpp.md)