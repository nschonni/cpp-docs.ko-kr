---
title: 컴파일러 오류 C3624 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3624
dev_langs:
- C++
helpviewer_keywords:
- C3624
ms.assetid: eaac6a4f-eb11-4e4d-ab12-124ba995c5cf
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8f38aece68d3ca3adff03ec0512cb78afc2e5ffa
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46030042"
---
# <a name="compiler-error-c3624"></a>컴파일러 오류 C3624

'type':이 형식 사용 해야 ' assembly '어셈블리에 대 한 참조

코드를 컴파일하는 데 필요한 어셈블리 (참조)이 지정 되지 않았습니다. 어셈블리를 전달 합니다 [#using](../../preprocessor/hash-using-directive-cpp.md) 지시문입니다.

## <a name="example"></a>예제

다음 샘플에서는 C3624 오류가 생성 됩니다.

```
// C3624.cpp
// compile with: /clr /c
#using <System.Windows.Forms.dll>

// Uncomment the following 2 lines to resolve.
// #using <System.dll>
// #using <System.Drawing.dll>

using namespace System;

public ref class MyForm : public Windows::Forms::Form {};   // C3624
```
