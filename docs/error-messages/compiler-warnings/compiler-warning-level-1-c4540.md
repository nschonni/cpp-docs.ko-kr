---
title: 컴파일러 경고 (수준 1) C4540 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4540
dev_langs:
- C++
helpviewer_keywords:
- C4540
ms.assetid: 8085e748-5f4d-43c2-b06d-eaf794edbf72
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4e3f553bd1f910c7b17e079dc1f03664c78383e3
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46042769"
---
# <a name="compiler-warning-level-1-c4540"></a>컴파일러 경고(수준 1) C4540

dynamic_cast 액세스할 수 없거나 모호한 기본; 변환 하는 데 사용 실행 시간 테스트 실패 ('type2'에 ' type1')

사용한 `dynamic_cast` 다른 형식으로 변환할 수 있습니다. 컴파일러에서 캐스팅 항상 실패 하 게 있는지 확인 (반환 **NULL**) 기본 클래스에 액세스할 수 없기 때문에 (`private`예를 들어) 모호한 (한 번에 표시 클래스 계층 구조, 예를 들어).

다음이 경고의 예를 보여 줍니다. 클래스 **B** 클래스에서 파생 된 **는**합니다. 프로그램을 사용 하 여 `dynamic_cast` 클래스에서 캐스팅 **B** (파생된 클래스) 클래스 **는**에 항상 실패 클래스 **B** 는 `private` 이므로 액세스할 수 없습니다. 액세스를 변경 **A** 하 **공용** 하면 경고가 해결 됩니다.

```
// C4540.cpp
// compile with: /W1

struct A {
   virtual void g() {}
};

struct B : private A {
   virtual void g() {}
};

int main() {
   B b;
   A * ap = dynamic_cast<A*>(&b);   // C4540
}
```