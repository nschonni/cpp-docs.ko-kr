---
title: 심각한 오류 C1055 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1055
dev_langs:
- C++
helpviewer_keywords:
- C1055
ms.assetid: a9fb9190-d7eb-4d5f-b1a2-a41e584a28c1
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6960d8168bd818e4d1baa30e5e54940e6e4dc2e9
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46115452"
---
# <a name="fatal-error-c1055"></a>심각한 오류 C1055

컴파일러 한계: 키가 부족

소스 파일에는 너무 많은 기호가 포함 되어 있습니다. 컴파일러 기호 테이블에 대 한 해시 키 부족합니다.

### <a name="to-fix-by-using-the-following-possible-solutions"></a>아래의 해결 방법 따라 수정합니다.

1. 소스 파일을 더 작은 파일로 분할 합니다.

1. 불필요 한 헤더 파일을 제거 합니다.

1. 새로 만드는 대신 임시 및 전역 변수를 다시 사용 합니다.