---
title: _com_error::Error | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- _com_error::Error
- Error
dev_langs:
- C++
helpviewer_keywords:
- Error method [C++]
ms.assetid: b53a15fd-198e-4276-afcd-13439c4807f7
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 9d56fcf7faaee9d3b0e02964163aa62372a30a78
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46109298"
---
# <a name="comerrorerror"></a>_com_error::Error

**Microsoft 전용**

생성자에 전달 된 HRESULT를 검색 합니다.

## <a name="syntax"></a>구문

```
HRESULT Error( ) const throw( );
```

## <a name="return-value"></a>반환 값

원시 HRESULT 항목 생성자에 전달 합니다.

## <a name="remarks"></a>설명

캡슐화 된 HRESULT 항목 검색을 `_com_error` 개체입니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[_com_error 클래스](../cpp/com-error-class.md)