---
title: 컴파일러 경고 (수준 1) C4377 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4377
dev_langs:
- C++
helpviewer_keywords:
- C4377
ms.assetid: a1c797b8-cd5e-4a56-b430-d07932e811cf
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 613ebe183b61c6b9894ed3b726f90061e2b24ef6
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46047176"
---
# <a name="compiler-warning-level-1-c4377"></a>컴파일러 경고(수준 1) C4377

네이티브 형식은 기본적으로 private입니다. -d1PrivateNativeTypes는 사용 되지 않습니다.

어셈블리의 네이티브 형식 이전 릴리스에서 문서화 되지 않은 내부 컴파일러 옵션을 기본적으로 공용 되었습니다 (**/d1PrivateNativeTypes**) 비공개로 설정 하는 해당 하는 데 사용 되었습니다.

모든 형식에 네이티브 및 CLR 어셈블리에서 기본적으로 private 됩니다 있도록 **/d1PrivateNativeTypes** 더 이상 필요 합니다.

## <a name="example"></a>예제

다음 샘플에서는 C4377 오류가 발생 합니다.

```
// C4377.cpp
// compile with: /clr /d1PrivateNativeTypes /W1
// C4377 warning expected
int main() {}
```