---
title: 식의 배열 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- expressions [C++], arrays in
- arrays [C++], in expressions
ms.assetid: 6e5a795b-d6bd-4e39-b313-6a20d47c4d4b
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 34f8a45dfa9de9a5a48e13cb6a38f667e5963f2d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46068548"
---
# <a name="arrays-in-expressions"></a>식의 배열

배열 형식의 식별자 표시 되 면 식 이외의 `sizeof`, 주소 (**&**), 초기화 또는 참조의 첫 번째 배열 요소에 대 한 포인터로 변환 됩니다. 예를 들어:

```cpp
char szError1[] = "Error: Disk drive not ready.";
char *psz = szError1;
```

`psz` 포인터는 `szError1` 배열의 첫 번째 요소를 가리킵니다. 포인터와 달리 배열은 수정할 수 있는 l-value가 아닙니다. 따라서 다음 대입은 올바르지 않습니다.

```cpp
szError1 = psz;
```

## <a name="see-also"></a>참고자료

[배열](../cpp/arrays-cpp.md)