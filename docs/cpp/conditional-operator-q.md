---
title: '조건부 연산자:? : | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- '?:'
- '?'
dev_langs:
- C++
helpviewer_keywords:
- conditional operators [C++]
- '? : operator'
ms.assetid: 88643ee8-7100-4f86-880a-705ec22b6271
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 982b03ae1785aba03dd96ef3b1423a93c74efdf2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46075698"
---
# <a name="conditional-operator--"></a>조건부 연산자:? :

## <a name="syntax"></a>구문

```
expression ? expression : expression
```

## <a name="remarks"></a>설명

조건부 연산자 (**?:**)는 삼항 연산자 (걸리는 피연산자 3 개). 조건 연산자는 다음과 같이 사용됩니다.

- 첫 번째 피연산자는 암시적으로 변환할 **bool**합니다. 계속하기 전에 피연산자가 계산되고 의도하지 않은 모든 결과가 완료됩니다.

- 첫 번째 피연산자가 **true** (1), 두 번째 피연산자는 평가 합니다.

- 첫 번째 피연산자가 **false** (0), 세 번째 피연산자는 평가 합니다.

조건 연산자의 결과는 두 번째 또는 세 번째 피연산자가 계산된 결과입니다. 마지막 피연산자 2개 중 1개만 조건식에서 계산됩니다.

조건식은 오른쪽과 왼쪽이 연결되어 있습니다. 첫 번째 피연산자는 정수 계열 또는 포인터 형식이어야 합니다. 다음 규칙이 두 번째 피연산자와 세 번째 피연산자에 적용됩니다.

- 두 피연산자의 형식이 동일할 경우 결과도 해당 형식입니다.

- 피연산자가 모두 일반적인 산술 변환은 산술 또는 열거형 형식일 경우 (에서 다루는 [표준 변환](standard-conversions.md)) 공용 형식으로 변환 하기 위해 수행 됩니다.

- 두 피연산자가 모두 포인터 형식이거나 하나는 포인터 형식이고 나머지 하나는 0으로 계산된 상수 식일 경우 공용 형식으로 변환하기 위해 포인터 변환이 수행됩니다.

- 두 피연산자가 모두 참조 형식일 경우 공용 형식으로 변환하기 위해 참조 변환이 수행됩니다.

- 두 피연산자가 모두 void 형식일 경우 공용 형식이 void 형식입니다.

- 두 피연산자의 형식이 동일한 사용자 정의 형식인 경우 공통 형식이 해당 형식입니다.

- 피연산자의 형식이 다르고 피연산자 중 하나 이상의 형식이 사용자 지정 형식인 경우 공통 형식을 결정하기 위한 언어 규칙이 사용됩니다. 아래의 경고를 참조하세요.

위의 목록에 없는 두 번째 피연산자와 세 번째 피연산자의 조합은 부적합합니다. 결과의 형식은 공용 형식이며, 두 번째 피연산자와 세 번째 피연산자가 같은 형식이고 둘 다 l-value일 경우 l-value입니다.

> [!WARNING]
>  두 번째와 세 번째 피연산자의 형식이 같지 않으면 C++ 표준에 지정된 복합 형식 변환 규칙이 호출됩니다. 이러한 변환이 수행되면 임시 개체 생성 및 제거를 비롯한 예기치 않은 동작이 발생할 수 있습니다. 그러므로 조건부 연산자와 함께 사용자 정의 형식을 피연산자로 사용하지 않거나, 사용자 정의 형식을 사용하는 경우에는 명시적으로 각 피연산자를 공용 형식으로 캐스팅하는 것이 좋습니다.

## <a name="example"></a>예제

```cpp
// expre_Expressions_with_the_Conditional_Operator.cpp
// compile with: /EHsc
// Demonstrate conditional operator
#include <iostream>
using namespace std;
int main() {
   int i = 1, j = 2;
   cout << ( i > j ? i : j ) << " is greater." << endl;
}
```

## <a name="see-also"></a>참고자료

[C++ 기본 제공 연산자, 우선 순위 및 결합성](../cpp/cpp-built-in-operators-precedence-and-associativity.md)<br/>
[조건식 연산자](../c-language/conditional-expression-operator.md)