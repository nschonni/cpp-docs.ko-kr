---
title: 컴파일러 오류 C3707 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3707
dev_langs:
- C++
helpviewer_keywords:
- C3707
ms.assetid: ac63a5dd-7a4b-48d2-9f2a-be9cb090134c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d18d4a82d06018cdba6147ba6756b1718648847a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46052787"
---
# <a name="compiler-error-c3707"></a>컴파일러 오류 C3707

'function': dispinterface 메서드에 dispid가 있어야 합니다.

사용 하는 경우는 `dispinterface` 메서드를 할당 해야 하는 `dispid`합니다. 이 오류를 해결 하려면 할당을 `dispid` 에 `dispinterface` 등의 주석 처리를 제거 하는 방법에 대 한 메서드를는 `id` 아래 샘플의 메서드에 대 한 특성입니다. 자세한 내용은 특성을 참조 하세요 [dispinterface](../../windows/dispinterface.md) 하 고 [id](../../windows/id.md)합니다.

다음 샘플에서는 C3707를 생성합니다.

```
// C3707.cpp
#include <atlbase.h>
#include <atlcom.h>
#include <atlctl.h>

[module(name="xx")];
[dispinterface]
__interface IEvents : IDispatch
{
   HRESULT event1([in] int i);   // C3707
   // try the following line instead
   // [id(1)] HRESULT event1([in] int i);
};

int main() {
}
```