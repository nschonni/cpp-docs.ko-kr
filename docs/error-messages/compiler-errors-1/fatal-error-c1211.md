---
title: 심각한 오류 C1211 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1211
dev_langs:
- C++
helpviewer_keywords:
- C1211
ms.assetid: df0ca70d-ec6e-4400-926a-b877e2599978
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 444d2bc25c2eddd5ea9a0170272bd3e71b61f94f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46018530"
---
# <a name="fatal-error-c1211"></a>심각한 오류 C1211

설치된 런타임 버전에서는 TypeForwardedTo 사용자 지정 특성이 지원되지 않습니다.

현재 릴리스에 대한 컴파일러가 있지만 이전 릴리스의 공용 언어 런타임을 사용하는 경우 C1211이 발생합니다.

컴파일러의 일부 기능은 이전 버전의 런타임에서 작동하지 않을 수 있습니다.

C1211을 해결하려면 사용 중인 컴파일러와 함께 제공되는 공용 언어 런타임을 설치합니다.

자세한 내용은 [형식 전달 (C + + /cli CLI)](../../windows/type-forwarding-cpp-cli.md)합니다.