---
title: TMP_MAX, L_tmpnam | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: conceptual
f1_keywords:
- TMP_MAX
- L_tmpnam
dev_langs:
- C++
helpviewer_keywords:
- temporary files, length
- L_tmpnam constant
- TMP_MAX constant
ms.assetid: ab19fd0c-b5b7-49f7-b23d-da9dfbcf0c1f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: cee175eb7f12952dfe7e30ef79842ee03a96fbb1
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46019681"
---
# <a name="tmpmax-ltmpnam"></a>TMP_MAX, L_tmpnam

## <a name="syntax"></a>구문

```
#include <stdio.h>
```

## <a name="remarks"></a>설명

`TMP_MAX`는 `tmpnam` 함수가 생성할 수 있는 고유한 파일 이름의 최대 수입니다. `L_tmpnam`은 `tmpnam`에 의해 생성되는 임시 파일 이름의 길이입니다.

## <a name="see-also"></a>참고 항목

[전역 상수](../c-runtime-library/global-constants.md)