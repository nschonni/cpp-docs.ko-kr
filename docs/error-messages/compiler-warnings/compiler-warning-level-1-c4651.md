---
title: 컴파일러 경고 (수준 1) C4651 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4651
dev_langs:
- C++
helpviewer_keywords:
- C4651
ms.assetid: f1ea82aa-4dc1-4972-b55a-57fdb962f0dd
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b516ef86372901d00dd20d94ed10d5e361bbab8d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46099473"
---
# <a name="compiler-warning-level-1-c4651"></a>컴파일러 경고(수준 1) C4651

' 정의 ' 현재 컴파일 아니라 미리 컴파일된 헤더를 지정 합니다.

미리 컴파일된 헤더를 생성할 때 아니라이 컴파일에 정의 지정 합니다.

정의 코드 나머지 아니라 미리 컴파일된 헤더에 적용 됩니다.

미리 컴파일된 헤더 /DSYMBOL을 사용 하 여 빌드된 /Yu 컴파일 /DSYMBOL 없는 경우 컴파일러에서이 경고를 생성 합니다.  이 경고를 해결 /DSYMBOL /Yu 명령줄에 추가 합니다.