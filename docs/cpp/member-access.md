---
title: 멤버 액세스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- member-selection operators [C++]
- pointers, smart
- member access, overloaded operators
- operator overloading [C++], member access operators
- smart pointers, definition
- smart pointers
ms.assetid: 8c7b2c43-eb92-4d42-9a8e-61aa37d71333
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 2aadccd883738fe2e6e9f57cc63f67cde6d6a6c4
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46099943"
---
# <a name="member-access"></a>멤버 액세스

멤버 액세스 연산자를 오버 로드 하 여 클래스 멤버 액세스를 제어할 수 있습니다 (**->**). 이 연산자는 이 사용법에서 단항 연산자로 간주되며 오버로드된 연산자 함수가 클래스 멤버 함수여야 합니다. 따라서 이러한 함수의 선언은 다음과 같습니다.

## <a name="syntax"></a>구문

```
class-type *operator->()
```

## <a name="remarks"></a>설명

여기서 *클래스 형식* 이 연산자가 속해 있는 클래스의 이름입니다. 멤버 액세스 연산자 함수는 비정적 멤버 함수여야 합니다.

이 연산자는 역참조나 개수 사용법에 앞서 포인터의 유효성을 검사하는 "스마트 포인터"를 구현하는 데 사용되며 종종 포인터 역참조 연산자와 함께 사용됩니다.

**.** 멤버 액세스 연산자를 오버 로드할 수 없습니다.

## <a name="see-also"></a>참고자료

[연산자 오버로드](../cpp/operator-overloading.md)