---
title: 심각한 오류 C1091 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1091
dev_langs:
- C++
helpviewer_keywords:
- C1091
ms.assetid: 812d4201-9154-48b0-b9af-5959c082ca33
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e93c2e6c26f8704e700465fb706867129847a460
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46104254"
---
# <a name="fatal-error-c1091"></a>심각한 오류 C1091

컴파일러 한계: 문자열 길이가 'length'바이트를 초과합니다.

문자열 상수가 문자열 길이의 현재 한계를 초과했습니다.

정적 문자열을 둘 이상의 변수로 분할한 다음 선언의 일부로 또는 런타임 중에 [strcpy_s](../../c-runtime-library/reference/strcpy-s-wcscpy-s-mbscpy-s.md) 를 사용하여 결과를 결합하는 것이 좋습니다.