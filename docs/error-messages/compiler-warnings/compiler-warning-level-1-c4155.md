---
title: 컴파일러 경고 (수준 1) C4155 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4155
dev_langs:
- C++
helpviewer_keywords:
- C4155
ms.assetid: ba233353-09e3-4195-8127-13a27ddd8d70
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: dc6620b788a550e26bedca4df0749feaf2f3a9fd
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46074748"
---
# <a name="compiler-warning-level-1-c4155"></a>컴파일러 경고(수준 1) C4155

'delete' 배열 형식을 사용하지 않고 배열 식을 삭제했습니다.

배열을 삭제하려면 **삭제** 의 배열 형식을 사용해야 합니다. 이 경고는 ANSI 호환성(/Za)에서만 발생합니다.

## <a name="example"></a>예제

다음 샘플에서는 C4155를 생성합니다.

```
// C4155.cpp
// compile with: /Za /W1
#include <stdio.h>

int main(void)
{
    int (*array)[ 10 ] = new int[ 5 ] [ 10 ];
    array[0][0] = 8;

    printf_s("%d\n", array[0][0]);

   delete array;   // C4155
    // try the following line instead
    // delete [] array;   // C4155
}
```