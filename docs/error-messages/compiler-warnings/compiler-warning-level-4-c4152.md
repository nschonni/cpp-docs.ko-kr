---
title: 컴파일러 경고 (수준 4) C4152 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4152
dev_langs:
- C++
helpviewer_keywords:
- C4152
ms.assetid: 6025ab70-d7cf-4730-913a-3ca0b1186a3a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: cab4d812c91239f277dbacede6db43f669908b0a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46099631"
---
# <a name="compiler-warning-level-4-c4152"></a>컴파일러 경고(수준 4) C4152

비표준 확장입니다. 식에서 함수/데이터 포인터 변환이 있습니다.

함수 포인터가 데이터 포인터로 변환되거나 그 반대로 변환됩니다. 이 변환은 Microsoft 확장(/Ze)에서는 허용되지만 ANSI C에서는 허용되지 않습니다.