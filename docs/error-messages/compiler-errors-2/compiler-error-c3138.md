---
title: 컴파일러 오류 C3138 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3138
dev_langs:
- C++
helpviewer_keywords:
- C3138
ms.assetid: 364ee9e8-9358-410e-bd35-9c4a226a3753
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d66ee7cad3b1514d75fedc968f6bf51554695c79
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46046909"
---
# <a name="compiler-error-c3138"></a>컴파일러 오류 C3138

'interface': 'attribute' 인터페이스는 IDispatch에서 상속 하는 인터페이스 또는 IDispatch에서 상속 해야 합니다

사용 하 여 인터페이스를 [이중](../../windows/dual.md) 또는 [dispinterface](../../windows/dispinterface.md) 특성이 없는 `IDispatch` 직접 또는 간접 기본 인터페이스로 합니다.

다음 예제에서는 C3138를 생성합니다.

```
// C3138.cpp
#include <unknwn.h>

[ object, uuid("77ac9240-6e9a-11d2-97de-0000f805d73b") ]
__interface IMyCustomInterface
{
   HRESULT mf1(void);
};

[ dispinterface, uuid("3536f8a0-6e9a-11d2-97de-0000f805d73b") ]
__interface IMyDispInterface : IUnknown
{
   [id(1)] HRESULT mf2(void);
};

[ object, dual, uuid("34e90a10-6e9a-11d2-97de-0000f805d73b") ]
__interface IMyDualInterface : IMyCustomInterface  // C3138 expected
{
   HRESULT mf3(void);
};
```