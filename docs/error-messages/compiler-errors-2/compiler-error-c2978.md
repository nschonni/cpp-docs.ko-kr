---
title: 컴파일러 오류 C2978 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2978
dev_langs:
- C++
helpviewer_keywords:
- C2978
ms.assetid: 5e7bee82-e266-4ccd-ad2e-ee89606ec5bf
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 40d7569a250812d6807c4723366b88e2f290be85
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46045187"
---
# <a name="compiler-error-c2978"></a>컴파일러 오류 C2978

구문 오류: 'keyword1' 또는 'keyword2'가 필요한데 'keyword3' 형식이 있습니다. 제네릭에서는 비형식 매개 변수를 사용할 수 없습니다.

제네릭 클래스가 잘못 선언되었습니다. 참조 [제네릭](../../windows/generics-cpp-component-extensions.md)자세한 내용은 합니다.

## <a name="example"></a>예제

다음 샘플에서는 C2978을 생성합니다.

```
// C2978.cpp
// compile with: /clr /c
generic <ref class T>   // C2978
// try the following line instead
// generic <typename T>   // OK
ref class Utils {
   static void sort(T elems, size_t size);
};

generic <int>
// try the following line instead
// generic <class T>
ref class Utils2 {
   static void sort(T elems, size_t size);
};
```