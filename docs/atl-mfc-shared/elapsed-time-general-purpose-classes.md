---
title: '경과 시간: 범용 클래스 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- adding dates
- calculating dates and times
- dates, calculating intervals
- elapsed time, calculating
- elapsed time
- time, elapsed
- intervals, date and time
- calculations, date and time
ms.assetid: e5c5d3d2-ce1d-409e-875c-98848434e716
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 54c3061ac0d081d04834ba4a8b7336732d854199
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50055868"
---
# <a name="elapsed-time-general-purpose-classes"></a>경과 시간: 범용 클래스

다음 절차에 간 차이 계산 하는 방법을 보여 줍니다 `CTime` 개체 및 get을 `CTimeSpan` 결과입니다. 사용 된 `CTime` 및 `CTimeSpan` 경과 된 시간을 다음과 같이 계산 하는 개체:

   [!code-cpp[NVC_ATLMFC_Utilities#174](../atl-mfc-shared/codesnippet/cpp/elapsed-time-general-purpose-classes_1.cpp)]

계산 있을 `elapsedTime`의 멤버 함수를 사용할 수 있습니다 `CTimeSpan` 경과 된 시간 값의 구성 요소를 추출 하 합니다.

