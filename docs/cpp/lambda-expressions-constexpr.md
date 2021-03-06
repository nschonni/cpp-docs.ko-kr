---
title: c + +에서 constexpr 람다 식 | Microsoft Docs
ms.custom: ''
ms.date: 07/19/2017
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- lambda expressions [C++], constexpr
ms.assetid: b56346cd-fbff-475f-aeaa-ed2010c6d6f7
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 71c28ab1531c2af19f2b8f594db457d0272b0664
ms.sourcegitcommit: a738519aa491a493a8f213971354356c0e6a5f3a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/05/2018
ms.locfileid: "48820362"
---
# <a name="constexpr-lambda-expressions-in-c"></a>c + +에서 constexpr 람다 식

**Visual Studio 2017 버전 15.3 이상** (사용할 수 있습니다 [/std: c + + 17](../build/reference/std-specify-language-standard-version.md)): 람다 식으로 선언할 수 있습니다 **constexpr** 상수 식에서 사용할 때 각 초기화 캡처하거나 소개 하는 데이터 멤버는 상수 식 내에서 허용 됩니다.

```cpp
    int y = 32;
    auto answer = [y]() constexpr
    {
        int x = 10;
        return y + x;
    };

    constexpr int Increment(int n)
    {
        return [n] { return n + 1; }();
    }
```

람다는 암시적으로 **constexpr** 결과의 요구 사항을 충족 하는 경우를 **constexpr** 함수:

```cpp
    auto answer = [](int n)
    {
        return 32 + n;
    };

    constexpr int response = answer(10);
```

람다는 암시적 또는 명시적으로 하는 경우 **constexpr**, 및 함수 포인터로 변환할 결과 함수가 이기도 **constexpr**:

```cpp
    auto Increment = [](int n)
    {
        return n + 1;
    };

    constexpr int(*inc)(int) = Increment;
```

## <a name="see-also"></a>참고자료

[C++ 언어 참조](../cpp/cpp-language-reference.md)<br/>
[C++ 표준 라이브러리의 함수 개체](../standard-library/function-objects-in-the-stl.md)<br/>
[함수 호출](../cpp/function-call-cpp.md)<br/>
[for_each](../standard-library/algorithm-functions.md#for_each)