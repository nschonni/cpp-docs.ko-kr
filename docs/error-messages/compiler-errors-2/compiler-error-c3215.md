---
title: 컴파일러 오류 C3215 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3215
dev_langs:
- C++
helpviewer_keywords:
- C3215
ms.assetid: d0d16007-8885-42e0-b086-2d3a61f348c5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8ea9b7cb22f5a3d61a661d7344673bf567f7d629
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46093898"
---
# <a name="compiler-error-c3215"></a>컴파일러 오류 C3215

'type1': 제네릭 형식 매개 변수가 이미 'type2'의 제약을 받습니다.

제약 조건을 두 번 이상 지정했습니다.

제네릭에 대한 자세한 내용은 [Generics](../../windows/generics-cpp-component-extensions.md)을 참조하세요.

다음 샘플에서는 C3215를 생성합니다.

```
// C3215.cpp
// compile with: /clr
interface struct A {};

generic <class T>
where T : A,A
ref class C {};   // C3215
```

해결 방법:

```
// C3215b.cpp
// compile with: /clr /c
interface struct A {};

generic <class T>
where T : A
ref class C {};
```