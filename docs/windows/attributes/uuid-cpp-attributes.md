---
title: uuid (c + + 특성) | Microsoft Docs
ms.custom: ''
ms.date: 10/02/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- vc-attr.uuid
dev_langs:
- C++
helpviewer_keywords:
- uuid attribute
ms.assetid: 90562a94-5e28-451b-a4b0-cadda7f66efe
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 3eddf1981aba8babcb87562ed546ce4086499fd7
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50071341"
---
# <a name="uuid-c-attributes"></a>uuid(C++ 특성)

클래스 또는 인터페이스에 대 한 고유 ID를 지정 합니다.

## <a name="syntax"></a>구문

```cpp
[ uuid(
   "uuid"
) ]
```

### <a name="parameters"></a>매개 변수

*uuid*<br/>
128 비트 고유 식별자입니다.

## <a name="remarks"></a>설명

인터페이스 또는 클래스의 정의 지정 하지 않은 경우는 **uuid** c + + 특성을 Visual c + + 컴파일러 제공 됩니다. 지정 하는 경우는 **uuid**, 따옴표를 포함 해야 합니다.

지정 하지 않는 경우 **uuid**, 컴파일러에서 컴퓨터에서 다른 특성 프로젝트에서 같은 이름의 클래스 또는 인터페이스에 대 한 동일한 GUID를 생성 합니다.

자체 고유 Id를 생성 하려면 Uuidgen.exe 또는 Guidgen.exe를 사용할 수 있습니다. (이러한 도구 중 하나를 실행 하려면 클릭 **시작** 누릅니다 **실행** 메뉴. 필요한 도구를의 이름을 입력 합니다.)

또한 ATL을 사용 하지 않는 프로젝트를 사용 하는 경우를 지정 하는 **uuid** 특성이 지정 하는 것과 [uuid](../../cpp/uuid-cpp.md) **__declspec** 한정자입니다. 검색 하는 **uuid** 클래스의 사용할 수 있습니다 [__uuidof](../../cpp/uuidof-operator.md)

## <a name="example"></a>예제

참조를 [bindable](bindable.md) 의 샘플 사용에 대 한 예제 **uuid**합니다.

## <a name="requirements"></a>요구 사항

### <a name="attribute-context"></a>특성 컨텍스트

|||
|-|-|
|**적용 대상**|**클래스**, **구조체**합니다 **인터페이스**를 **union**, **열거형**|
|**반복 가능**|아니요|
|**필수 특성**|없음|
|**잘못된 특성**|없음|

특성 컨텍스트에 대한 자세한 내용은 [특성 컨텍스트](cpp-attributes-com-net.md#contexts)를 참조하세요.

## <a name="see-also"></a>참고 항목

[IDL 특성](idl-attributes.md)<br/>
[인터페이스 특성](interface-attributes.md)<br/>
[클래스 특성](class-attributes.md)<br/>
[Typedef, Enum, Union 및 Struct 특성](typedef-enum-union-and-struct-attributes.md)<br/>
[uuid](/windows/desktop/Midl/uuid)