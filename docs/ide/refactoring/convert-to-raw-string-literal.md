---
title: 원시 문자열 리터럴로 변환 | Microsoft Docs
ms.custom: ''
ms.date: 11/16/2016
ms.technology:
- cpp-ide
ms.topic: conceptual
ms.assetid: fffbfee4-66ee-42ba-aeb9-df07fb702c51
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 75037ea542a5bd2160d9a89138b12f82867002a5
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46388448"
---
# <a name="convert-to-raw-string-literal"></a>원시 문자열 리터럴로 변환
**대상:** 모든 문자열을 C++ 원시 문자열 리터럴로 변환할 수 있습니다.

**시기:** 이스케이프된 문자로 처리되지 않아야 하는 이스케이프된 문자가 포함된 문자열이 있는 경우.

**이유:** 문자를 이중 이스케이프 처리할 수 있지만 그러면 혼동을 주거나 읽을 수 없는 문자열이 되는 경우가 많습니다.  원시 문자열 리터럴을 사용하면 문자열을 훨씬 더 쉽게 읽을 수 있습니다.

**방법:**

1. 변환할 이스케이프된 문자열 위에 텍스트 또는 마우스 커서를 놓습니다.

   ![강조 표시된 코드](images/stringliteral_highlight.png)

1. 다음 작업 중 하나를 수행합니다.
   * **키보드**
     * **Ctrl+.** 를 눌러 **빠른 작업 및 리팩터링** 메뉴를 트리거하고 상황에 맞는 메뉴에서 **원시 문자열 리터럴로 변환**을 선택합니다.
   * **마우스**
     * 코드를 마우스 오른쪽 단추로 클릭하고, **빠른 작업 및 리팩터링** 메뉴를 선택하고, 상황에 맞는 메뉴에서 **원시 문자열 리터럴로 변환**을 선택합니다.
     * 왼쪽 여백에 나타나는 ![Lightbulb](images/bulb.png) 아이콘을 클릭하고 상황에 맞는 메뉴에서 **원시 문자열 리터럴로 변환**을 선택합니다.

1. 문자열은 즉시 원시 문자열 리터럴로 변환됩니다.

   ![원시 문자열 리터럴 결과](images/stringliteral_result.png)