---
title: 원본 (c + + COM 특성) | Microsoft Docs
ms.custom: ''
ms.date: 10/02/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- vc-attr.source
dev_langs:
- C++
helpviewer_keywords:
- source attribute
ms.assetid: 1878d05d-7709-4e97-b114-c62f38f5140e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: f7bc10b89df58dc72c35855fea43c2a0387f9efd
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50058468"
---
# <a name="source-c"></a>source(C++)

클래스에서 연결 지점에 대 한 COM 개체의 소스 인터페이스를 지정합니다. 속성 또는 메서드, 개체 또는 VARIANT는 이벤트의 소스인 멤버 반환 됨을 나타냅니다.

## <a name="syntax"></a>구문

```cpp
[ source(interfaces) ]
```

### <a name="parameters"></a>매개 변수

*interfaces*<br/>
하나 이상의 인터페이스 소스를 적용 하는 경우 지정 하는 특성 클래스입니다. 원본 속성 또는 메서드에 적용 될 때이 매개 변수 사용 되지 않습니다.

## <a name="remarks"></a>설명

합니다 **원본** c + + 특성에 동일한 기능을 합니다 [원본](/windows/desktop/Midl/source) MIDL 특성입니다.

사용할 수는 [기본](default-cpp.md) 개체에 대 한 기본 소스 인터페이스를 지정 하는 특성입니다.

## <a name="example"></a>예제

```cpp
// cpp_attr_ref_source.cpp
// compile with: /LD
#include "windows.h"
#include "unknwn.h"
[module(name="MyLib")];

[object, uuid(11111111-1111-1111-1111-111111111111)]
__interface b
{
   [id(0), propget, bindable, displaybind, defaultbind, requestedit]
   HRESULT get_I([out, retval]long *i);
};

[object, uuid(11111111-1111-1111-1111-111111111131)]
__interface c
{
   [id(0), propget, bindable, displaybind, defaultbind, requestedit]
   HRESULT et_I([out, retval]long *i);
};

[coclass, default(c), uuid(11111111-1111-1111-1111-111111111132)]
class N : public b
{
};

[coclass, source(c), default(b, c), uuid(11111111-1111-1111-1111-111111111133)]
class NN : public b
{
};
```

## <a name="requirements"></a>요구 사항

### <a name="attribute-context"></a>특성 컨텍스트

|||
|-|-|
|**적용 대상**|**클래스**하십시오 **구조체**, **인터페이스**|
|**반복 가능**|아니요|
|**필수 특성**|`coclass` (클래스 또는 구조체에 적용 됨) 하는 경우|
|**잘못된 특성**|없음|

특성 컨텍스트에 대한 자세한 내용은 [특성 컨텍스트](cpp-attributes-com-net.md#contexts)를 참조하세요.

## <a name="see-also"></a>참고 항목

[IDL 특성](idl-attributes.md)<br/>
[클래스 특성](class-attributes.md)<br/>
[메서드 특성](method-attributes.md)<br/>
[coclass](coclass.md)