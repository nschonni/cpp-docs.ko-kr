---
title: Abort 사용 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- Abort
dev_langs:
- C++
helpviewer_keywords:
- abort function
ms.assetid: 3ba39b78-ef74-4a8d-8dee-2d62442de174
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 3edc24b2b8dc869022039d4aaaea73af06eac16b
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46092543"
---
# <a name="using-abort"></a>abort 사용

호출 된 [중단](../c-runtime-library/reference/abort.md) 함수 즉시 종료 됩니다. 이 함수는 초기화된 전역 정적 개체에 대한 일반적인 소멸 프로세스를 건너뜁니다. 또한 이 함수는 `atexit` 함수를 사용하여 지정된 모든 특수 처리를 건너뜁니다.

## <a name="see-also"></a>참고자료

[추가 종료 고려 사항](../cpp/additional-termination-considerations.md)