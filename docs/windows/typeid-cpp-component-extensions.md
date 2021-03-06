---
title: typeid (C + + /cli 및 C + + /cli CX) | Microsoft Docs
ms.custom: ''
ms.date: 10/12/2018
ms.technology:
- cpp-windows
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- typeid keyword [C++]
ms.assetid: e9706cae-e7c4-4d6d-b474-646d73df3e70
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 1196956208d490674d4705a8d1e61ea3381d94a2
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50065189"
---
# <a name="typeid--ccli-and-ccx"></a>typeid (C + + /cli 및 C + + /cli CX)

개체의 유형을 나타내는 값을 가져옵니다.

> [!NOTE]
> 이 항목은 TypeId의 C++ 구성 요소 확장명 버전을 참조합니다. 이 키워드의 ISO c + + 버전을 참조 하세요 [typeid 연산자](../cpp/typeid-operator.md)합니다.

## <a name="all-runtimes"></a>모든 런타임

### <a name="syntax"></a>구문

```cpp
T::typeid
```

### <a name="parameters"></a>매개 변수

*T*<br/>
형식 이름.

## <a name="windows-runtime"></a>Windows 런타임

### <a name="syntax"></a>구문

```cpp
Platform::Type^ type = T::typeid;
```

### <a name="parameters"></a>매개 변수

*T*<br/>
형식 이름.

### <a name="remarks"></a>설명

C + + /CX에서는 typeid 반환을 [platform:: type](../cppcx/platform-type-class.md) 런타임 형식 정보에서 생성 된 합니다.

### <a name="requirements"></a>요구 사항

컴파일러 옵션: `/ZW`

## <a name="common-language-runtime"></a>공용 언어 런타임

### <a name="syntax"></a>구문

```
type::typeid
```

### <a name="parameters"></a>매개 변수

*type*<br/>
이름을 검색할 형식 (추상 선언 자)를 `System::Type` 개체입니다.

### <a name="remarks"></a>설명

`typeid` 가져오는 데 사용 되는 <xref:System.Type> 컴파일 타임 형식에 대 한 합니다.

`typeid` 사용 하 여 런타임 형식에 대 한 system 가져오는 비슷합니다 <xref:System.Type.GetType%2A> 또는 <xref:System.Object.GetType%2A>합니다. 그러나 typeid는 매개 변수로 형식 이름을 허용 했습니다.  System:: type 이름을 가져오려고 형식의 인스턴스를 사용 하려는 경우에 GetType 사용 합니다.

`typeid` GetType 런타임에 반환할 형식을 평가 하는 반면 형식 이름 (입력) 컴파일 타임에 평가할 수 있어야 합니다.

`typeid` 네이티브 형식 이름 또는 네이티브 형식 이름;에 대 한 공용 언어 런타임 별칭 참조 [c + + 네이티브 형식에.NET Framework 해당 하는 (C + + /cli CLI)](../dotnet/dotnet-framework-equivalents-to-cpp-native-types-cpp-cli.md) 자세한 내용은 합니다.

`typeid` 또한을 system:: type 여전히 반환 하지만 원시 형식을 사용 하 여 작동 합니다.  Type_info 구조를 가져오려면 [typeid 연산자](../cpp/typeid-operator.md)합니다.

### <a name="requirements"></a>요구 사항

컴파일러 옵션: `/clr`

### <a name="examples"></a>예제

다음 예제에서는 typeid 키워드를 비교 합니다 `GetType()` 멤버입니다.

```cpp
// keyword__typeid.cpp
// compile with: /clr
using namespace System;

ref struct G {
   int i;
};

int main() {
   G ^ pG = gcnew G;
   Type ^ pType = pG->GetType();
   Type ^ pType2 = G::typeid;

   if (pType == pType2)
      Console::WriteLine("typeid and GetType returned the same System::Type");
   Console::WriteLine(G::typeid);

   typedef float* FloatPtr;
   Console::WriteLine(FloatPtr::typeid);
}
```

```Output
typeid and GetType returned the same System::Type
G

System.Single*
```

다음 샘플 system:: type 형식에 특성을 가져오는 데 사용할 수 있습니다 형식의 변수를 보여 줍니다.  또한는 일부 형식의 해야 사용에 대 한 typedef를 만들려면 표시 `typeid`합니다.

```cpp
// keyword__typeid_2.cpp
// compile with: /clr
using namespace System;
using namespace System::Security;
using namespace System::Security::Permissions;

typedef int ^ handle_to_int;
typedef int * pointer_to_int;

public ref class MyClass {};

class MyClass2 {};

[attribute(AttributeTargets::All)]
ref class AtClass {
public:
   AtClass(Type ^) {
      Console::WriteLine("in AtClass Type ^ constructor");
   }
};

[attribute(AttributeTargets::All)]
ref class AtClass2 {
public:
   AtClass2() {
      Console::WriteLine("in AtClass2 constructor");
   }
};

// Apply the AtClass and AtClass2 attributes to class B
[AtClass(MyClass::typeid), AtClass2]
[AttributeUsage(AttributeTargets::All)]
ref class B : Attribute {};

int main() {
   Type ^ MyType = B::typeid;

   Console::WriteLine(MyType->IsClass);

   array<Object^>^ MyArray = MyType -> GetCustomAttributes(true);
   for (int i = 0 ; i < MyArray->Length ; i++ )
      Console::WriteLine(MyArray[i]);

   if (int::typeid != pointer_to_int::typeid)
      Console::WriteLine("int::typeid != pointer_to_int::typeid, as expected");

   if (int::typeid == handle_to_int::typeid)
      Console::WriteLine("int::typeid == handle_to_int::typeid, as expected");
}
```

```Output
True

in AtClass2 constructor

in AtClass Type ^ constructor

AtClass2

System.AttributeUsageAttribute

AtClass

int::typeid != pointer_to_int::typeid, as expected

int::typeid == handle_to_int::typeid, as expected
```

## <a name="see-also"></a>참고 항목

[.NET 및 UWP용 구성 요소 확장](../windows/component-extensions-for-runtime-platforms.md)