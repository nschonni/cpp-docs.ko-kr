---
title: 컴파일러 오류 C2083 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2083
dev_langs:
- C++
helpviewer_keywords:
- C2083
ms.assetid: 5fc4f931-eab6-4d8d-a3ee-3b8e11e64b18
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: adf2787f8aea3611abd9eeac054df6bb054d802a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46103284"
---
# <a name="compiler-error-c2083"></a>컴파일러 오류 C2083

struct/union 비교가 잘못되었습니다.

구조체 또는 공용 구조체는 다른 사용자 정의 형식과 직접 비교됩니다. 이는 비교 연산자를 정의했거나 스칼라 형식에 대한 변환이 존재하지 않는 한 허용되지 않습니다.