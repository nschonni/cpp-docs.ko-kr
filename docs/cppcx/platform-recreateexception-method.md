---
title: 'Platform:: recreateexception 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 12/30/2016
ms.technology: cpp-windows
ms.topic: reference
f1_keywords:
- VCCORLIB/Platform::Exception
dev_langs:
- C++
helpviewer_keywords:
- Platform::Exception Class
ms.assetid: fa73d1ab-86e4-4d26-a7d9-81938c1c7e77
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 28434f6c8c35f2cd4cfc15953f761d28037626e6
ms.sourcegitcommit: 761c5f7c506915f5a62ef3847714f43e9b815352
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44109721"
---
# <a name="platformrecreateexception-method"></a>Platform::ReCreateException 메서드

이 메서드는 내부 전용이며 사용자 코드에서는 사용되지 않습니다. Exception:: createexception 메서드를 대신 사용 합니다.

## <a name="syntax"></a>구문

```cpp
static Exception^ ReCreateException(int hr)
```

### <a name="parameters"></a>매개 변수

*hr*

### <a name="property-valuereturn-value"></a>속성 값/반환 값

지정된 HRESULT에 따라 새 Platform::Exception^을 반환합니다.
