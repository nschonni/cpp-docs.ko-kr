---
title: _bstr_t::GetBSTR | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- _bstr_t::GetBSTR
dev_langs:
- C++
helpviewer_keywords:
- GetBSTR method [C++]
ms.assetid: 0c62ff16-4433-4183-a03c-d5a0a9b731ef
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 3a62cd1c08409fb5915ebf42fa118c1e6124e29f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46071863"
---
# <a name="bstrtgetbstr"></a>_bstr_t::GetBSTR

**Microsoft 전용**

`BSTR`에 의해 래핑되는 `_bstr_t`의 시작 부분을 가리킵니다.

## <a name="syntax"></a>구문

```
BSTR& GetBSTR( );
```

## <a name="return-value"></a>반환 값

`BSTR`에 의해 래핑되는 `_bstr_t`의 시작 부분입니다.

## <a name="remarks"></a>설명

**GetBSTR** 모두에 영향을 줍니다 `_bstr_t` 공유 하는 개체는 `BSTR`합니다. 둘 이상의 `_bstr_t` 공유할 수는 `BSTR` 복사 생성자를 사용 하 여 및 **연산자 =** 합니다.

## <a name="example"></a>예제

참조 [_bstr_t:: assign](../cpp/bstr-t-assign.md) 사용 하는 예제 **GetBSTR**합니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[_bstr_t 클래스](../cpp/bstr-t-class.md)