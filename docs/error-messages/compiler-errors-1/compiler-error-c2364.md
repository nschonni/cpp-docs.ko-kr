---
title: 컴파일러 오류 C2364 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2364
dev_langs:
- C++
helpviewer_keywords:
- C2364
ms.assetid: 4f550571-94b5-42ca-84cb-663fecbead44
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6d35701eb47bdf633377652094b847ccdfb31e59
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46100632"
---
# <a name="compiler-error-c2364"></a>컴파일러 오류 C2364

'type': 사용자 지정 특성 형식이 잘못 되었습니다.

사용자 지정 특성에 대 한 명명 된 인수는 컴파일 시간 상수로 제한 합니다. 정수 계열 형식 예를 들어 (int, char 등), system:: type ^, 및 system:: object ^ 합니다.

## <a name="example"></a>예제

다음 샘플 C2364를 생성합니다.

```
// c2364.cpp
// compile with: /clr /c
using namespace System;

[attribute(AttributeTargets::All)]
public ref struct ABC {
public:
   // Delete the following line to resolve.
   ABC( Enum^ ) {}   // C2364
   ABC( int ) {}   // OK
};
```