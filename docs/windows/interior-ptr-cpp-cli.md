---
title: interior_ptr (C + + /cli CLI) | Microsoft Docs
ms.custom: ''
ms.date: 10/12/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- stdcli::language::interior_ptr
- interior_ptr_cpp
- interior_ptr
dev_langs:
- C++
helpviewer_keywords:
- interior_ptr keyword [C++]
ms.assetid: 25160f74-569e-492d-9e3c-67ece7486baa
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: d47539c9d7d8e51a061aba35e6b2f3b8f7049951
ms.sourcegitcommit: 3f4e92266737ecb70507871e87dc8e2965ad7e04
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/15/2018
ms.locfileid: "49328053"
---
# <a name="interiorptr-ccli"></a>interior_ptr(C++/CLI)

*내부 포인터* 개체 자체가 아니라 참조 형식 내부에 포인터를 선언 합니다. 내부 포인터는 참조 핸들, 값 형식, boxed 형식 핸들, 관리되는 형식의 멤버 또는 관리되는 배열의 요소를 가리킬 수 있습니다.

## <a name="all-runtimes"></a>모든 런타임

(이 언어 기능에는 모든 런타임에 적용되는 설명이 없습니다.)

## <a name="windows-runtime"></a>Windows 런타임

(이 언어 기능에는 Windows 런타임에만 적용되는 설명이 없습니다.)

### <a name="requirements"></a>요구 사항

컴파일러 옵션: `/ZW`

## <a name="common-language-runtime"></a>공용 언어 런타임

다음 구문 예제는 내부 포인터를 보여 줍니다.

### <a name="syntax"></a>구문

```cpp
cli::interior_ptr<cv_qualifier type> var = &initializer;
```

### <a name="parameters"></a>매개 변수

*cv_qualifier*<br/>
**const** 나 **volatile** 한정자입니다.

*type*<br/>
유형의 *이니셜라이저*합니다.

*var*<br/>
이름을 합니다 **interior_ptr** 변수입니다.

*initializer*<br/>
참조 형식의 멤버, 관리되는 배열의 요소 또는 네이티브 포인터에 할당할 수 있는 다른 모든 개체입니다.

### <a name="remarks"></a>설명

네이티브 포인터는 개체의 인스턴스를 이동시키는 가비지 수집기로부터 도출되는 관리되는 힙에서 위치를 변경하는 항목을 추적할 수 없습니다. 포인터가 인스턴스를 제대로 참조하려면 런타임은 포인터를 새로 위치가 지정된 개체로 업데이트해야 합니다.

**interior_ptr** 네이티브 포인터 기능의 상위 집합을 나타냅니다.  따라서 네이티브 포인터에 할당할 수 있는 것도 할당할 수는 **interior_ptr**합니다.  내부 포인터는 네이티브 포인터로서 비교 및 포인터 산술을 포함한 동일한 일련의 작업을 수행할 수 있습니다.

내부 포인터를 스택에만 선언할 수 있습니다.  내부 포인터를 클래스의 멤버로 선언할 수 없습니다.

내부 포인터가 스택에만 존재하므로 내부 포인터의 주소는 관리되지 않는 포인터를 생성합니다.

**interior_ptr** 에 암시적으로 변환 **bool**를 조건문에 사용할 수 있습니다.

가비지 수집 힙에서 이동할 수 없는 개체를 가리키는 내부 포인터를 선언 하는 방법에 대 한 자세한 내용은 [pin_ptr](../windows/pin-ptr-cpp-cli.md)합니다.

**interior_ptr** cli 네임 스페이스입니다.  참조 [Platform, default 및 cli 네임 스페이스](../windows/platform-default-and-cli-namespaces-cpp-component-extensions.md) 자세한 내용은 합니다.

내부 포인터에 대한 자세한 내용은 다음을 참조하십시오.

- [방법: 내부 포인터 및 관리되는 배열 선언 및 사용(C++/CLI)](../windows/how-to-declare-and-use-interior-pointers-and-managed-arrays-cpp-cli.md)

- [방법: interior_ptr 키워드를 사용하여 값 형식 선언(C++/CLI)](../windows/how-to-declare-value-types-with-the-interior-ptr-keyword-cpp-cli.md)

- [방법: 내부 포인터 및 네이티브 포인터를 사용하여 함수 오버로드(C++/CLI)](../windows/how-to-overload-functions-with-interior-pointers-and-native-pointers-cpp-cli.md)

- [방법: const 키워드를 사용하여 내부 포인터 선언(C++/CLI)](../windows/how-to-declare-interior-pointers-with-the-const-keyword-cpp-cli.md)

### <a name="requirements"></a>요구 사항

컴파일러 옵션: `/clr`

### <a name="examples"></a>예제

다음 샘플에서는 참조 형식으로 내부 포인터를 선언하고 사용하는 방법을 보여 줍니다.

```cpp
// interior_ptr.cpp
// compile with: /clr
using namespace System;

ref class MyClass {
public:
   int data;
};

int main() {
   MyClass ^ h_MyClass = gcnew MyClass;
   h_MyClass->data = 1;
   Console::WriteLine(h_MyClass->data);

   interior_ptr<int> p = &(h_MyClass->data);
   *p = 2;
   Console::WriteLine(h_MyClass->data);

   // alternatively
   interior_ptr<MyClass ^> p2 = &h_MyClass;
   (*p2)->data = 3;
   Console::WriteLine((*p2)->data);
}
```

```Output
1
2
3
```

## <a name="see-also"></a>참고 항목

[.NET 및 UWP 용 구성 요소 확장](../windows/component-extensions-for-runtime-platforms.md)