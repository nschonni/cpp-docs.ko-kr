---
title: 컴파일러 오류 C3392 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3392
dev_langs:
- C++
helpviewer_keywords:
- C3392
ms.assetid: e4757596-e2aa-4314-b01e-5c4bfd2110e9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 04c69220cf9b6bf10a6bae8f9557f83d1e004752
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46112813"
---
# <a name="compiler-error-c3392"></a>컴파일러 오류 C3392

'type_arg': 제네릭 'generic_type'의 제네릭 매개 변수 'param'에 대한 형식 인수가 잘못되었습니다. 매개 변수가 없는 public 생성자가 있어야 합니다.

제네릭 형식이 잘못 인스턴스화되었습니다. 형식 정의를 확인하세요. 자세한 내용은 [제네릭](../../windows/generics-cpp-component-extensions.md)합니다.

## <a name="example"></a>예제

C +의 제네릭 형식을 제작 하는 경우 지원 되지 않는 특정 제약 조건이 있는 제네릭 형식을 포함 하는 구성 요소를 만들려면 다음 샘플에서는 C# + CLI입니다. 자세한 내용은 [형식 매개 변수에 대한 제약 조건](/dotnet/csharp/programming-guide/generics/constraints-on-type-parameters)을 참조하세요.

```cs
// C3392.cs
// Compile by using: csc /target:library C3392.cs
// a C# program
public class GR<C, V, N>
where C : class
where V : struct
where N : new() {}
```

C3392.dll 구성 요소를 사용할 수 있는 경우 다음 샘플에서는 C3392를 생성 합니다.

```cpp
// C3392_b.cpp
// Compile by using: cl /clr C3392_b.cpp
#using <C3392.dll>

ref class R { R(int) {} };
ref class N { N() {} };

value class V {};

ref class N2 { public: N2() {} };
ref class R2 { public: R2() {} };

int main () {
   GR<R^, V, N^>^ gr1;   // C3392
   GR<R^, V, N2^>^ gr1a; // OK

   GR<R^, N^, N^>^ gr3;  // C3392
   GR<R^, V, N2^>^ gr3a; // OK

   GR<R^, V, R^>^ gr4;   // C3392
   GR<R^, V, R2^>^ gr4a; // OK
}
```