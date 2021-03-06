---
title: enum 클래스 (C + + /cli 및 C + + /cli CX) | Microsoft Docs
ms.custom: ''
ms.date: 10/12/2018
ms.technology:
- cpp-windows
ms.topic: reference
dev_langs:
- C++
ms.assetid: 8010fa8c-bad6-45b4-8214-b4db64d7ffe1
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 7c63a043b8f1a91654c0b765632969b82725a3c0
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50066164"
---
# <a name="enum-class--ccli-and-ccx"></a>enum 클래스 (C + + /cli 및 C + + /cli CX)

열거자라는 명명된 상수 집합으로 구성된 사용자 정의 형식인 열거형을 네임스페이스 범위에서 선언합니다.

## <a name="all-runtimes"></a>모든 런타임

### <a name="remarks"></a>설명

C + + /CX 및 C + + 지원 **public enum 클래스** 하 고 **개인 enum 클래스** 표준 c + +와 비슷합니다 **enum 클래스** 하지만 액세스 가능성의 추가 지정자입니다. 아래 **/clr**, C + + 11 **enum 클래스** 형식은 허용 되지만 원하는 ISO 열거형 형식 및 하지 C + 확인 하기 위해 만들어진 경고 C4472를 생성 + /CX 및 C + + CLI 형식입니다. ISO 표준 c + +에 대 한 자세한 내용은 **enum** 키워드를 참조 하십시오 [열거형](../cpp/enumerations-cpp.md)합니다.

## <a name="windows-runtime"></a>Windows 런타임

### <a name="syntax"></a>구문

```cpp
      access
      enum class
      enumeration-identifier
      [:underlying-type] { enumerator-list } [var];
accessenum structenumeration-identifier[:underlying-type] { enumerator-list } [var];
```

### <a name="parameters"></a>매개 변수

*access*<br/>
해당 되는 열거형의 접근성 **공용** 하거나 **개인**합니다.

*enumeration-identifier*<br/>
열거형의 이름입니다.

*underlying-type*<br/>
(선택 사항) 열거형의 내부 형식입니다.

(선택 사항. Windows 런타임 전용) 수 있는 열거형의 내부 형식 **bool**, **char**를 `char16`를 `int16`를 `uint16`를 **int**, `uint32`하십시오 `int64`, 또는 `uint64`합니다.

*enumerator-list*<br/>
열거자 이름의 쉼표로 구분된 목록입니다.

각 열거자의 값은 컴파일러에 의해 암시적으로 정의되거나 *enumerator*`=`*constant-expression*을 참조하세요. 기본적으로 첫 번째 열거자의 값은 암시적으로 정의된 경우 0입니다. 암시적으로 정의된 각 후속 열거자의 값은 이전 열거자의 값 + 1입니다.

*var*<br/>
(선택 사항) 열거형 형식의 변수 이름입니다.

### <a name="remarks"></a>설명

자세한 내용과 예제는 [열거형](https://msdn.microsoft.com/%20library/windows/apps/hh755820.aspx)을 참조하세요.

컴파일러는 열거자의 값을 정의하는 상수 식을 *underlying-type*으로 표현할 수 없는 경우 오류 메시지를 내보냅니다.  그러나 컴파일러는 내부 형식에 적합하지 않은 값에 대해 오류를 보고하지 않습니다. 예를 들어:

- *underlying-type* 이 숫자이고, 열거자가 해당 형식의 최대값을 지정하는 경우, 그 다음에 암시적으로 정의되는 열거형 값은 표현할 수 없습니다.

- 경우 *기본 형식* 됩니다 **bool**, 고 세 개 이상의 열거자가 암시적 처음 두 개를 표현할 수 없는 후 열거자를 정의 합니다.

- *underlying-type* 이 `char16`이고 열거형 값이 0xD800에서 0xDFFF까지이면 값을 표현할 수 있습니다. 그러나 이 값은 유니코드 서로게이트 쌍의 절반을 나타내므로 논리적으로 잘못된 값이며 격리에 표시되면 안 됩니다.

### <a name="requirements"></a>요구 사항

컴파일러 옵션: `/ZW`

## <a name="common-language-runtime"></a>공용 언어 런타임

### <a name="syntax"></a>구문

```cpp
      access
      enum class
      name [:type] { enumerator-list } var;
accessenum structname [:type] { enumerator-list } var;
```

### <a name="parameters"></a>매개 변수

*access*<br/>
열거형의 접근성입니다. 일 수 있습니다 **공개** 하거나 **개인**합니다.

*enumerator-list*<br/>
열거형에서 식별자(열거자)의 쉼표로 구분된 목록입니다.

*name*<br/>
열거형의 이름입니다. 관리되는 익명 열거형은 허용되지 않습니다.

*type*<br/>
(선택 사항) 내부 형식의 합니다 *식별자*합니다. 서명 되거나 서명 되지 않은 버전의 같은 스칼라 형식일 수 **int**를 **짧은**, 또는 **긴**합니다.  **bool** 나 **char** 사용할 수 있습니다.

*var*<br/>
(선택 사항) 열거형 형식의 변수 이름입니다.

### <a name="remarks"></a>설명

**enum 클래스** 및 **enum 구조체** 는 동일한 선언입니다.

열거형에는 관리되거나 또는 C++/CX 및 표준이라는 두 가지 유형이 있습니다.

다음과 같이 관리되거나 C++/CX 열거형을 정의할 수 있습니다.

```cpp
public enum class day {sun, mon };
```

다음과 의미 체계가 같습니다.

```cpp
ref class day {
public:
   static const int sun = 0;
   static const int mon = 1;
};
```

표준 열거형은 다음과 같이 정의할 수 있습니다.

```cpp
enum day2 { sun, mon };
```

다음과 의미 체계가 같습니다.

```cpp
static const int sun = 0;
static const int mon = 1;
```

관리되는 열거자 이름(*식별자*)은 열거형이 정의되어 있는 범위에 삽입되지 않습니다. 열거자에 대한 모든 참조를 정규화해야 합니다(*이름*`::`*식별자*).  이러한 이유로, 관리되는 익명 열거형은 정의할 수 없습니다.

표준 열거형의 열거자는 바깥쪽 범위에 강력하게 삽입됩니다.  즉, 바깥쪽 범위에 열거자와 동일한 이름을 가진 다른 기호가 있을 경우 컴파일러에서 오류를 생성합니다.

Visual Studio 2002 및 Visual Studio 2003에서는 열거자가 약하게 삽입 됩니다 (표시 바깥쪽 범위에 동일한 이름 가진 다른 식별자가 없을 경우).

표준 c + + enum이 정의 된 경우 (없이 **클래스** 또는 **구조체**) 사용 하 여 컴파일하면 `/clr` 관리 되는 enum으로 컴파일됩니다 열거형에 발생 합니다.  열거형이 여전히 관리되지 않는 열거형의 의미 체계를 사용합니다.  컴파일러 특성을 삽입 `Microsoft::VisualC::NativeEnumAttribute` 열거형을 네이티브 열거형에 대 한 프로그래머의 의도 식별 합니다.  다른 컴파일러에는 표준 열거형이 관리되는 열거형으로 표시됩니다.

명명에 사용 하 여 컴파일된 표준 열거형 `/clr` 열거형을 관리 되는 어셈블리에 표시 되 고 다른 관리 되는 컴파일러에서 사용할 수 있습니다.   그러나 명명되지 않은 표준 열거형은 어셈블리에서 공개적으로 표시되지 않습니다.

Visual Studio 2002 및 Visual Studio 2003에서 함수 매개 변수에서 형식으로 사용 되는 표준 열거형:

```cpp
// mcppv2_enum.cpp
// compile with: /clr
enum E { a, b };
void f(E) {System::Console::WriteLine("hi");}

int main() {
   E myi = b;
   f(myi);
}
```

에 형식으로 사용된 표준 열거형은 함수 서명에 대해 MSIL에서 다음을 내보냅니다.

```cpp
void f(int32);
```

그러나 현재 버전의 컴파일러에서는 표준 열거형이 [NativeEnumAttribute] 및 함수 서명에 대해 MSIL에서 다음을 사용하여 관리되는 열거형으로 내보내집니다.

```cpp
void f(E)
```

네이티브 열거형에 대한 자세한 내용은 [C++ Enumeration Declarations](../cpp/enumerations-cpp.md)를 참조하십시오.

CLR 열거형에 대한 자세한 내용은 다음을 참조하세요.

- [열거형의 내부 형식](../dotnet/how-to-define-and-consume-enums-in-cpp-cli.md)

### <a name="requirements"></a>요구 사항

컴파일러 옵션: `/clr`

### <a name="examples"></a>예제

```cpp
// mcppv2_enum_2.cpp
// compile with: /clr
// managed enum
public enum class m { a, b };

// standard enum
public enum n { c, d };

// unnamed, standard enum
public enum { e, f } o;

int main()
{
   // consume managed enum
   m mym = m::b;
   System::Console::WriteLine("no automatic conversion to int: {0}", mym);
   System::Console::WriteLine("convert to int: {0}", (int)mym);

   // consume standard enum
   n myn = d;
   System::Console::WriteLine(myn);

   // consume standard, unnamed enum
   o = f;
   System::Console::WriteLine(o);
}
```

```Output
no automatic conversion to int: b

convert to int: 1

1

1
```

## <a name="see-also"></a>참고 항목

[.NET 및 UWP용 구성 요소 확장](../windows/component-extensions-for-runtime-platforms.md)