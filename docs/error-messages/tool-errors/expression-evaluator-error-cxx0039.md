---
title: 식 계산기 오류 CXX0039 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- CXX0039
dev_langs:
- C++
helpviewer_keywords:
- CXX0039
- CAN0039
ms.assetid: 8bf698d2-e015-4595-944f-72b81aa43d22
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b5397426618c5dfcbaa6307105781ff2e6f2eb97
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46048333"
---
# <a name="expression-evaluator-error-cxx0039"></a>식 계산기 오류 CXX0039

기호 모호합니다.

C 식 계산기는 식에서 사용할 기호를 인스턴스를 확인할 수 없습니다. 기호는 상속 트리에서 한 번 이상 발생합니다.

범위 결정 연산자를 사용 해야 합니다 (`::`) 식에 사용할 인스턴스를 명시적으로 지정 합니다.

이 오류는 can0039와 동일 합니다.