---
title: 컴파일러 오류 C2170 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2170
dev_langs:
- C++
helpviewer_keywords:
- C2170
ms.assetid: d5c663f0-2459-4e11-a8bf-a52b62f3c71d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b75d4c54bc6ec24cb182f3b6fb37ff4b8cd1ddfc
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46055730"
---
# <a name="compiler-error-c2170"></a>컴파일러 오류 C2170

'identifier': 함수로 선언 되지 내장 함수 일 수 없습니다

### <a name="to-fix-by-checking-the-following-possible-causes"></a>다음과 같은 가능한 원인을 확인하여 수정하려면

1. Pragma `intrinsic` 함수 이외의 항목에 사용 됩니다.

1. Pragma `intrinsic` 내장 형식이 없는 함수의 사용 됩니다.