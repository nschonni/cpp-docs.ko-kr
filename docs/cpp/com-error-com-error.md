---
title: _com_error::_com_error | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- _com_error::_com_error
dev_langs:
- C++
helpviewer_keywords:
- _com_error method [C++]
ms.assetid: 0a69e46c-caab-49ef-b091-eee401253ce6
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 89377e33e56b0796fc850c050c8e79eac86ee07d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46040468"
---
# <a name="comerrorcomerror"></a>_com_error::_com_error

**Microsoft 전용**

생성 된 **_com_error** 개체입니다.

## <a name="syntax"></a>구문

```
_com_error(
   HRESULT hr,
   IErrorInfo* perrinfo = NULL,
   bool fAddRef=false) throw( );

_com_error( const _com_error& that ) throw( );
```

#### <a name="parameters"></a>매개 변수

*hr*<br/>
HRESULT 정보입니다.

*perrinfo*<br/>
`IErrorInfo` 개체

*fAddRef*<br/>
기본 생성자에 null이 아닌에서 AddRef를 호출 하면 `IErrorInfo` 인터페이스입니다. 상식적으로 인터페이스의 소유권 전달 되는 위치를 계산 하는 올바른 참조를 제공 합니다 **_com_error** 개체:

```cpp
throw _com_error(hr, perrinfo);
```

경우 원하지 않는 소유권을 전송 하는 코드를 **_com_error** 개체 및 `AddRef` 오프셋 하는 데 필요한 합니다 `Release` 에 **_com_error** 소멸자도 개체를 생성 다음과 같습니다.

```cpp
_com_error err(hr, perrinfo, true);
```

*는*<br/>
기존 **_com_error** 개체입니다.

## <a name="remarks"></a>설명

첫 번째 생성자는 지정 된 HRESULT를 및 선택적 새 개체를 만들고 `IErrorInfo` 개체입니다. 두 번째 기존 복사본을 만듭니다 **_com_error** 개체입니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[_com_error 클래스](../cpp/com-error-class.md)