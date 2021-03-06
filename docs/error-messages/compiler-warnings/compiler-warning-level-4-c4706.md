---
title: 컴파일러 경고 (수준 4) C4706 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4706
dev_langs:
- C++
helpviewer_keywords:
- C4706
ms.assetid: 89cd3f4f-812c-4a4b-9426-65a5a6d1b99c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 843edeaf490f27475003e9303f7929b818e2b104
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46036958"
---
# <a name="compiler-warning-level-4-c4706"></a>컴파일러 경고(수준 4) C4706

조건식 내 할당

조건식에서 테스트 값이 할당의 결과입니다.

할당은 테스트 식을 포함 하 여 다른 식에 합법적으로 사용할 수 있는 값 (할당의 왼쪽에 있는 값)이 있습니다.

다음 샘플에서는 C4706 오류가 생성 됩니다.

```
// C4706a.cpp
// compile with: /W4
int main()
{
   int a = 0, b = 0;
   if ( a  = b ) // C4706
   {
   }
}
```

테스트 조건 주위에 괄호를 두 번 하는 경우에 경고가 발생 합니다.

```
// C4706b.cpp
// compile with: /W4
int main()
{
   int a = 0, b = 0;
   if ( ( a  =  b ) ) // C4706
   {
   }
}
```

의도 라면 관계를 테스트 하 고 할당을 사용 하 여 `==` 연산자입니다. 예를 들어 다음 줄은 테스트 하는지 여부를 고 b가 같은 경우:

```
// C4706c.cpp
// compile with: /W4
int main()
{
   int a = 0, b = 0;
   if ( a == b )
   {
   }
}
```

값 할당의 결과 테스트 하려는 경우 0 또는 null이 아닌 할당 되었는지 확인 하려면 테스트 합니다. 예를 들어, 다음 코드는이 경고를 발생 하지 않습니다.

```
// C4706d.cpp
// compile with: /W4
int main()
{
   int a = 0, b = 0;
   if ( ( a = b ) != 0 )
   {
   }
}
```