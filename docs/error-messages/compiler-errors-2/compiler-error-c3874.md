---
title: 컴파일러 오류 C3874 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3874
dev_langs:
- C++
helpviewer_keywords:
- C3874
ms.assetid: fd55fc05-69a7-4237-b3b7-dca1d5400b4f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 70f6773e65c167b980a4fd9967b910a3f760d58f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46059272"
---
# <a name="compiler-error-c3874"></a>컴파일러 오류 C3874

'function'의 반환 형식 'type' 대신 ' int' 해야 합니다.

함수에는 컴파일러에서 예상 된 반환 형식이 없습니다.

다음 샘플에서는 C3874 오류가 생성 됩니다.

```
// C3874b.cpp
double main()
{   // C3874
}
```