---
title: _variant_t::Detach | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- _variant_t::Detach
- _variant_t.Detach
dev_langs:
- C++
helpviewer_keywords:
- VARIANT object [C++], detatch
- Detach method [C++]
- VARIANT object
ms.assetid: c348ac08-62cf-4657-a16f-974a79c12158
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 4ab1e4f83025dcc3e4bc65274746e0617cf31b5b
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46065025"
---
# <a name="varianttdetach"></a>_variant_t::Detach

**Microsoft 전용**

캡슐화 된 분리 `VARIANT` 개체에서 `_variant_t` 개체입니다.

## <a name="syntax"></a>구문

```
VARIANT Detach( );
```

## <a name="return-value"></a>반환 값

캡슐화 된 `VARIANT`합니다.

## <a name="remarks"></a>설명

추출 하 고 캡슐화 된 반환 `VARIANT`, 그런 다음이 지우고 `_variant_t` 제거 하지 않고 개체입니다. 이 멤버 함수를 제거 합니다 `VARIANT` 캡슐화 및 집합에서 합니다 `VARTYPE` 이 `_variant_t` 개체 값을 vt_empty로 합니다. 반환 된 릴리스 하는 것 `VARIANT` 를 호출 하 여 합니다 [VariantClear](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear) 함수입니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[_variant_t 클래스](../cpp/variant-t-class.md)