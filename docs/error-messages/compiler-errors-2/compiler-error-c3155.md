---
title: 컴파일러 오류 C3155 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3155
dev_langs:
- C++
helpviewer_keywords:
- C3155
ms.assetid: b04a42e1-64e7-40f8-81fe-c7945348b2cf
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1b4000c9e7d3f175c243d4d3761216f4acface8f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46076478"
---
# <a name="compiler-error-c3155"></a>컴파일러 오류 C3155

속성 인덱서에 특성이 허용 되지 않습니다.

인덱싱된 속성을 잘못 선언 되었습니다. 자세한 내용은 [방법: 사용 하 여 속성 C + + CLI](../../dotnet/how-to-use-properties-in-cpp-cli.md)합니다.

## <a name="example"></a>예제

다음 샘플에서는 C3155 오류가 발생 합니다.

```
// C3155.cpp
// compile with: /clr /c
using namespace System;
ref struct R {
   property int F[[ParamArray] int] {   // C3155
   // try the following line instead
   // property int F[ int] {   // OK
      int get(int i) {
         return 0;
      }
   }
};
```