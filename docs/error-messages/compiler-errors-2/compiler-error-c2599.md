---
title: 컴파일러 오류 C2599 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2599
dev_langs:
- C++
helpviewer_keywords:
- C2599
ms.assetid: 88515f36-7589-47e2-862e-0de8b18d6668
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 515e380ea87b8ea648a00644ce8bca6428903f18
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46044485"
---
# <a name="compiler-error-c2599"></a>컴파일러 오류 C2599

'enum': 열거형의 정방향 선언은 허용 되지 않습니다

컴파일러는 더 이상 관리 되는 열거형의 정방향 선언을 지원합니다.

열거형의 정방향 선언은 허용 되지 않습니다 [/Za](../../build/reference/za-ze-disable-language-extensions.md)합니다.

다음 샘플에서는 C2599를 생성합니다.

```
// C2599.cpp
// compile with: /clr /c
enum class Status;   // C2599

enum class Status2 { stop2, hold2, go2};

ref struct MyStruct {
   // Delete the following line to resolve.
   Status m_status;

   Status2 m_status2;   // OK
};

enum class Status { stop, hold, go };
```