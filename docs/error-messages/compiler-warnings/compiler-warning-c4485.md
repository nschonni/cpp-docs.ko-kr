---
title: 컴파일러 경고 C4485 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4485
dev_langs:
- C++
helpviewer_keywords:
- C4485
ms.assetid: a6f2b437-ca93-4dcd-b9cb-df415e10df86
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: cb83700bf8ca79960599d85ed3d335f80c9fc7f2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46117753"
---
# <a name="compiler-warning-c4485"></a>컴파일러 경고 C4485

'override_function': 기본 ref 클래스 메서드 'base_class_function'와 일치 하지 않으면이 '표시 된 new' 또는 'override'; 'new' ('virtual')는 가정

접근자를 재정의 하거나 사용 하지 않고 합니다 `virtual` 키워드, 기본 클래스 접근자 함수를 하지만 `override` 또는 `new` 지정자 재정의 함수 서명의 일부가 없습니다. 추가 된 `new` 또는 `override` 이 경고를 해결 하려면 지정자입니다.

참조 [재정의](../../windows/override-cpp-component-extensions.md) 하 고 [new (의 new 슬롯 vtable)](../../windows/new-new-slot-in-vtable-cpp-component-extensions.md) 자세한 내용은 합니다.

C4485은 항상 오류로 실행 됩니다. 사용 된 [경고](../../preprocessor/warning.md) C4485 표시 하지 않으려면 pragma입니다.

## <a name="example"></a>예제

다음 샘플에서는 C4485

```
// C4485.cpp
// compile with: /clr
delegate void Del();

ref struct A {
   virtual event Del ^E;
};

ref struct B : A {
   virtual event Del ^E;   // C4485
};

ref struct C : B {
   virtual event Del ^E {
      void raise() override {}
      void add(Del ^) override {}
      void remove(Del^) override {}
   }
};
```