---
title: 컴파일러 경고 (수준 3) C4641 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4641
dev_langs:
- C++
helpviewer_keywords:
- C4641
ms.assetid: 28fe5c3e-6039-42da-9100-1312b5b15aea
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f44e94868f6a7b379fb1a2f75bbd28ce011b54c9
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46112111"
---
# <a name="compiler-warning-level-3-c4641"></a>컴파일러 경고(수준 3) C4641

XML 문서 주석에 모호한 상호 참조가 있습니다.

컴파일러는 참조를 명확 하 게 확인할 수 없습니다. 이 경고를 해결 하려면 참조를 명확 하 게 하는 데 필요한 매개 변수 정보를 지정 합니다.

자세한 내용은 [XML Documentation](../../ide/xml-documentation-visual-cpp.md)을 참조하세요.

## <a name="example"></a>예제

다음 샘플에서는 C4641 오류가 발생 합니다.

```
// C4641.cpp
// compile with: /W3 /doc /clr /c

/// <see cref="f" />   // C4641
// try the following line instead
// /// <see cref="f(int)" />
public ref class GR {
public:
   void f( int ) {}
   void f( char ) {}
};
```