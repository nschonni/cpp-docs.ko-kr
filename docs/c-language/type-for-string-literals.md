---
title: 문자열 리터럴의 형식 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- string literals, type
- types [C], string literals
ms.assetid: f50a28af-20c1-4440-bdc6-564c86a309c8
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 7773882d6fb04341a6f6d3a2cbcfda1d05f85d17
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46063283"
---
# <a name="type-for-string-literals"></a>문자열 리터럴의 형식

문자열 리터럴은 `char` 배열(즉, **char[ ]**) 형식입니다. 와이드 문자 문자열은 `wchar_t` 배열(즉, **wchar_t[ ]**) 형식입니다. 즉, 문자열은 `char` 형식의 요소가 포함된 배열입니다. 배열에 있는 요소의 수는 문자열의 문자 개수에 null 종결 문자에 해당하는 1을 더한 값입니다.

## <a name="see-also"></a>참고 항목

[C 문자열 리터럴](../c-language/c-string-literals.md)