---
title: 컴파일러 오류 C3351 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3351
dev_langs:
- C++
helpviewer_keywords:
- C3351
ms.assetid: c021bbbe-1067-4f51-af4f-940d2b792eb5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 31ab5843e6dec00755f3b4d671487da9eb87c5b7
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46085344"
---
# <a name="compiler-error-c3351"></a>컴파일러 오류 C3351

'object': 대리자 생성자: 두 번째 인수는 정적 멤버 함수 또는 전역 함수의 주소여야 합니다.

컴파일러에서 `static`으로 선언된 함수의 주소가 필요합니다.

다음 샘플에서는 C3351을 생성합니다.

```
// C3351a.cpp
// compile with: /clr
delegate int D(int, int);

ref class C {
public:
   int mf(int, int) {
      return 1;
   }

   static int mf2(int, int) {
      return 1;
   }
};

int main() {
   System::Delegate ^pD = gcnew D(nullptr, &C::mf);   // C3351
   System::Delegate ^pD2 = gcnew D(&C::mf2);
}
```
