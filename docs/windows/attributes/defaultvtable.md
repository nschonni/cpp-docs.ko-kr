---
title: defaultvtable (c + + COM 특성) | Microsoft Docs
ms.custom: ''
ms.date: 10/02/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- vc-attr.defaultvtable
dev_langs:
- C++
helpviewer_keywords:
- defaultvtable attribute
ms.assetid: 5b3ed483-f69e-44dd-80fc-952028eb9d73
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 003123036b8ae0e6bc39660ff7f2d98394dcad83
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50057779"
---
# <a name="defaultvtable"></a>defaultvtable

COM 개체에 대 한 기본 vtable 인터페이스와 인터페이스를 정의합니다.

## <a name="syntax"></a>구문

```cpp
[ defaultvtable(interface) ]
```

### <a name="parameters"></a>매개 변수

*interface*<br/>
지정 된 인터페이스를 COM 개체에 대 한 기본 vtable 하려는입니다.

## <a name="remarks"></a>설명

합니다 **defaultvtable** c + + 특성에 동일한 기능을 합니다 [defaultvtable](/windows/desktop/Midl/defaultvtable) MIDL 특성입니다.

## <a name="example"></a>예제

다음 코드를 사용 하는 클래스에 특성을 보여 줍니다 **defaultvtable** 기본 인터페이스를 지정 합니다.

```cpp
// cpp_attr_ref_defaultvtable.cpp
// compile with: /LD
#include <unknwn.h>
[module(name="MyLib")];

[object, uuid("00000000-0000-0000-0000-000000000001")]
__interface IMyI1 {
   HRESULT x();
};

[object, uuid("00000000-0000-0000-0000-000000000002")]
__interface IMyI2 {
   HRESULT x();
};

[object, uuid("00000000-0000-0000-0000-000000000003")]
__interface IMyI3 {
   HRESULT x();
};

[coclass, source(IMyI3, IMyI1), default(IMyI3, IMyI2), defaultvtable(IMyI1),
uuid("00000000-0000-0000-0000-000000000004")]
class CMyC3 : public IMyI3 {};
```

## <a name="requirements"></a>요구 사항

### <a name="attribute-context"></a>특성 컨텍스트

|||
|-|-|
|**적용 대상**|**클래스**, **구조체**|
|**반복 가능**|아니요|
|**필수 특성**|**coclass**|
|**잘못된 특성**|없음|

자세한 내용은 [특성 컨텍스트](cpp-attributes-com-net.md#contexts)를 참조하세요.

## <a name="see-also"></a>참고 항목

[IDL 특성](idl-attributes.md)<br/>
[클래스 특성](class-attributes.md)