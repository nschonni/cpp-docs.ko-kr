---
title: 컴파일러 오류 C3298 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3298
dev_langs:
- C++
helpviewer_keywords:
- C3298
ms.assetid: 458c2680-95bb-4d5e-895f-ce4115844193
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 06296fed3f33b56cb53cf3bc4531205638f0a204
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46053690"
---
# <a name="compiler-error-c3298"></a>컴파일러 오류 C3298

'constraint_1': 'constraint_2'에 ref 제약 조건이 있고 'constraint_1'에 값 제약 조건이 있으므로 'constraint_2'를 제약 조건으로 사용할 수 없습니다.

제약 조건에 대해 함께 사용할 수 없는 특성을 지정할 수 없습니다. 예를 들어 제네릭 형식 매개 변수를 값 형식과 참조 형식 둘 다로 제한할 수 없습니다.

자세한 내용은 [제네릭 형식 매개 변수에 대 한 제약 조건 (C + + CLI)](../../windows/constraints-on-generic-type-parameters-cpp-cli.md)합니다.

## <a name="example"></a>예제

다음 샘플에서는 C3298을 생성합니다.

```
// C3298.cpp
// compile with: /clr /c
generic<class T, class U>
where T : ref class
where U : T, value class   // C3298
public ref struct R {};
```