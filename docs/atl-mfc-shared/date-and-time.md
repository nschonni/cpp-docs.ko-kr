﻿---
title: 날짜 및 시간 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- time, MFC programming
- time
- MFC, date and time
- dates, MFC
ms.assetid: ecf56dc5-d418-4603-ad3e-af7e205a6403
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 90317405f09695c57c907e94306623d5b3e2386d
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46419966"
---
# <a name="date-and-time"></a>날짜 및 시간

MFC는 여러 가지 날짜 및 시간을 사용 하 여 작업을 지원합니다. 여기에는 다음이 포함됩니다.

- 시간 범용 클래스입니다. [CTime](../atl-mfc-shared/reference/ctime-class.md) 및 [CTimeSpan](../atl-mfc-shared/reference/ctimespan-class.md) 클래스는 TIME.H에 선언된 ANSI 표준 시간 라이브러리와 관련된 대부분의 기능을 캡슐화합니다.

- 시스템 클록을 지원합니다. MFC 버전 3.0 지원에 추가 되었습니다 `CTime` 는 win32 `SYSTEMTIME` 및 `FILETIME` 데이터 형식입니다.

- [DATE 데이터 형식](../atl-mfc-shared/date-type.md)에 대한 자동화를 지원합니다. 날짜 지원 날짜, 시간 및 날짜/시간 값입니다. [COleDateTime](../atl-mfc-shared/reference/coledatetime-class.md) 및 [COleDateTimeSpan](../atl-mfc-shared/reference/coledatetimespan-class.md)는 이 기능을 캡슐화하는 클래스입니다. 이 클래스들은 자동화 지원을 사용한 [COleVariant](../mfc/reference/colevariant-class.md) 클래스로 작업합니다.

## <a name="what-do-you-want-to-know-more-about"></a>자세히 알아보려는 항목

- [날짜 및 시간: SYSTEMTIME 지원](../atl-mfc-shared/date-and-time-systemtime-support.md)

- [날짜 및 시간: 자동화 지원](../atl-mfc-shared/date-and-time-automation-support.md)

- [날짜 및 시간: 데이터베이스 지원](../atl-mfc-shared/date-and-time-database-support.md)

## <a name="see-also"></a>참고 항목

[개념](../mfc/mfc-concepts.md)<br/>
[일반 MFC 항목](../mfc/general-mfc-topics.md)

