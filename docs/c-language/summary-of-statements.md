---
title: 문 요약 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
ms.assetid: ce45d2fe-ec0e-459f-afb1-80ab6a7f0239
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: e83d4db17dd20a46ed2cbdd91598428e14748cf0
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46030315"
---
# <a name="summary-of-statements"></a>문 요약

*statement*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*labeled-statement*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*compound-statement*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*expression-statement*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*selection-statement*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*iteration-statement*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*jump-statement*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*try-except-statement* /\* Microsoft 전용 \*/<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*try-finally-statement* /\* Microsoft 전용 \*/

*점프 문*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**goto**  *identifier*  **;**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**continue ;**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**break ;**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**return** *expression*<sub>opt</sub> **;**

*compound-statement*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**{** *declaration-list*<sub>opt</sub> *statement-list*<sub>opt</sub> **}**

*declaration-list*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*declaration*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*declaration-list* *declaration*

*statement-list*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*statement*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*statement-list* *statement*

*expression-statement*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*expression*<sub>opt</sub> **;**

*iteration-statement*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**while (**  *expression*  **)**  *statement*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**do**  *statement*  **while (**  *expression*  **) ;**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**for (**  *expression*<sub>opt</sub> **;** *expression*<sub>opt</sub> **;** *expression*<sub>opt</sub> **)** *statement*

*selection-statement*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**if (**  *expression*  **)**  *statement*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**if (**  *expression*  **)**  *statement*  **else**  *statement*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**switch (**  *expression*  **)**  *statement*

*labeled-statement*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*identifier*  **:**  *statement*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**case**  *constant-expression*  **:**  *statement*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**default :**  *statement*

*try-except-statement*:   /\* Microsoft 전용 \*/<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**__try**  *compound-statement* **__except (**  *expression*  **)**  *compound-statement*

*try-finally-statement*:   /\* Microsoft 전용 \*/<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**__try**  *compound-statement* **__finally**  *compound-statement*

## <a name="see-also"></a>참고 항목

[구 구조 문법](../c-language/phrase-structure-grammar.md)