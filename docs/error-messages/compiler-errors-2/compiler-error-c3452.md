---
title: 컴파일러 오류 C3452 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3452
dev_langs:
- C++
helpviewer_keywords:
- C3452
ms.assetid: e5293dcf-cb70-4133-ae2a-0bb496950ba0
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 392bddb57b90892bc867bcd201a99fdfc1e3f226
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46118104"
---
# <a name="compiler-error-c3452"></a>컴파일러 오류 C3452

목록 인수 멤버가 상수가 아닙니다.

인수가 컴파일 시간에 계산할 수 있는 값인 상수가 필요한 특성에 전달되었습니다.

## <a name="example"></a>예제

다음 샘플에서는 C3452를 생성합니다.

```
// C3452.cpp
// compile with: /c
int i;
[module( name="mod", type=dll, custom={i} ) ];   // C3452
// try the following line instead
// [module( name="mod", type=dll, custom={"a"} ) ];
```