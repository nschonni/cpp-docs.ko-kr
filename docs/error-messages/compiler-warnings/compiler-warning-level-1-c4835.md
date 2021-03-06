---
title: 컴파일러 경고 (수준 1) C4835 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4835
dev_langs:
- C++
helpviewer_keywords:
- C4835
ms.assetid: d2e44c62-7b0e-4a45-943d-97903e27ed9d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 70492be13d312c5d167990cfa0b6c0d741e1055f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46080105"
---
# <a name="compiler-warning-level-1-c4835"></a>컴파일러 경고(수준 1) C4835

'variable': 내보낸된 데이터에 대 한 이니셜라이저는 관리 되는 코드가 호스트 어셈블리에서 먼저 실행 될 때까지 실행 되지 것입니다

관리 되는 구성 요소 간 데이터에 액세스할 때 하지 네이티브 c + + 가져오기를 사용 하는 메커니즘을 내보내기는 것이 좋습니다. 대신 관리 되는 형식 내에서 데이터 멤버를 선언 하 고 사용 하 여 메타 데이터 참조 `#using` 클라이언트에서입니다. 자세한 내용은 [#using 지시문](../../preprocessor/hash-using-directive-cpp.md)을 참조하세요.

## <a name="example"></a>예제

다음 샘플에서는 C4835 오류가 발생 합니다.

```
// C4835.cpp
// compile with: /W1 /clr /LD
int f() { return 1; }
int n = 9;

__declspec(dllexport) int m = f();   // C4835
__declspec(dllexport) int *p = &n;   // C4835
```

## <a name="example"></a>예제

다음 샘플은 변수의 값이 잘못 되었습니다. 표시 이전 샘플에서 빌드한 구성 요소를 사용 합니다.

```
// C4835_b.cpp
// compile with: /clr C4835.lib
#include <stdio.h>
__declspec(dllimport) int m;
__declspec(dllimport) int *p;

int main() {
   printf("%d\n", m);
   printf("%d\n", p);
}
```

```Output
0
268456008
```