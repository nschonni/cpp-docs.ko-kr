---
title: 컴파일러 오류 C3273 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3273
dev_langs:
- C++
helpviewer_keywords:
- C3273
ms.assetid: 1d2ce9d9-222b-4cab-94e2-d2c1a9f5ebe0
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a23e9643dd302836b00c18c0c44c87ee1cfd2cfe
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46118403"
---
# <a name="compiler-error-c3273"></a>컴파일러 오류 C3273

__finally는 비관리 코드의 예외 블록에서 사용할 수 없습니다.

다음 샘플에서는 C3273을 생성합니다.

```
// C3273.cpp
// compile with: /GX
int main()
{
   try
   {
   }
   catch (int)
   {
   }
   __finally   // C3273, remove __finally clause
   {
   }
}
```