---
title: 호출 규칙 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- calling conventions
ms.assetid: 11b1e45c-8fd1-420b-bca0-a19e294c1d85
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 97a03e8c73f75e51a955805cd4ad76b902b0373c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46071486"
---
# <a name="calling-conventions"></a>호출 규칙

Visual C/C++ 컴파일러는 내부 및 외부 함수 호출에 몇 가지 다양한 규칙을 제공합니다. 이러한 다양한 접근 방법에 대한 이해는 프로그램을 디버깅하고 어셈블리 언어 루틴에 코드를 연결하는 데 도움이 됩니다.

이 주제의 항목에서는 호출 규칙간의 차이점, 인수를 전달하는 방식, 함수가 값을 반환하는 방식에 대해 설명합니다. 또한 고급 기능인 naked 함수 호출에 대한 설명을 통해 사용자 지정 프롤로그 및 에필로그 코드를 작성할 수 있도록 합니다.

X64 호출 규칙에 대 한 정보에 대 한 프로세서를 참조 하세요 [호출 규칙](../build/calling-convention.md)합니다.

## <a name="topics-in-this-section"></a>이 단원의 항목

- [인수 전달 및 명명 규칙](../cpp/argument-passing-and-naming-conventions.md) (`__cdecl`하십시오 `__stdcall`, `__fastcall`, 등)

- [호출 예제: 함수 프로토타입 및 호출](../cpp/calling-example-function-prototype-and-call.md)

- [Naked 함수 호출을 사용 하 여 사용자 지정 프롤로그/에필로그 코드 작성](../cpp/naked-function-calls.md)

- [부동 소수점 보조 프로세서 및 호출 규칙](../cpp/floating-point-coprocessor-and-calling-conventions.md)

- [사용 되지 않는 호출 규칙](../cpp/obsolete-calling-conventions.md)

## <a name="see-also"></a>참고자료

[Microsoft 전용 한정자](../cpp/microsoft-specific-modifiers.md)