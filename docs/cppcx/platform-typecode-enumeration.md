---
title: 'Platform:: typecode 열거형 | Microsoft Docs'
ms.custom: ''
ms.date: 12/30/2016
ms.technology: cpp-windows
ms.topic: reference
f1_keywords:
- VCCORLIB/Platform::TypeCode
dev_langs:
- C++
helpviewer_keywords:
- Platform::TypeCode Enumeration
ms.assetid: 93c1305f-eb16-4bec-aead-f88d9518b4cf
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: cb19a922655a77a2f7a2b5806c9b721f17e028f8
ms.sourcegitcommit: 761c5f7c506915f5a62ef3847714f43e9b815352
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44104175"
---
# <a name="platformtypecode-enumeration"></a>Platform::TypeCode 열거형

기본 제공 형식을 나타내는 숫자 범주를 지정합니다.

## <a name="syntax"></a>구문

```cpp
enum class TypeCode {};
```

### <a name="members"></a>멤버

|형식 코드|설명|
|---------------|-----------------|
|부울|Platform::Boolean 형식입니다.|
|Char16|default::char16 형식입니다.|
|DateTime|DateTime 형식입니다.|
|Decimal|숫자 형식입니다.|
|Double|default::float64 형식입니다.|
|Empty|Void|
|Int16|default::int16 형식입니다.|
|Int32|default::int32 형식입니다.|
|Int64|default::int64 형식입니다.|
|Int8|default::int8 형식입니다.|
|Object|Platform::Object 형식입니다.|
|Single|default::float32 형식입니다.|
|문자열|Platform::String 형식입니다.|
|UInt16|default::uint16 형식입니다.|
|UInt32|default::uint32 형식입니다.|
|UInt64|default::uint64 형식입니다.|
|UInt8|default::uint8 형식입니다.|

### <a name="requirements"></a>요구 사항

**지원 되는 최소 클라이언트:** Windows 8

**지원 되는 최소 서버:** Windows Server 2012

**네임스페이스:** Platform

**메타데이터:** platform.winmd