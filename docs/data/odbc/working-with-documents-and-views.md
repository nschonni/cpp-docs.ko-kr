---
title: 문서 및 뷰를 사용 하 여 작업 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-data
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- MFC [C++], documents
- MFC [C++], views
- views [C++], MFC
- documents [C++], MFC
ms.assetid: 349b142d-1c5a-4b99-9de4-241e41d3d2f1
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: c3879c6a29f95cc908d12c0b899214b521f46686
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50060445"
---
# <a name="working-with-documents-and-views"></a>문서 및 뷰 작업

Microsoft Foundation 클래스 (MFC) 라이브러리는 다양 한 기능에 대 한 문서/뷰 아키텍처를 사용합니다. 일반적으로 문서에 데이터를 저장 및 보기 프레임 창의 클라이언트 영역 내에서 표시 하 고 데이터를 사용 하 여 사용자 상호 작용을 관리 합니다. 뷰를 가져오고 데이터를 업데이트 하는 문서와 통신 합니다. 프레임 워크를 사용 하 여 또는 없으면 데이터베이스 클래스를 사용할 수 있습니다.

데이터베이스 클래스를 사용 하 여 프레임 워크에 대 한 자세한 내용은 참조 하세요. [MFC: 문서 및 뷰를 이용한 데이터베이스 클래스를 사용 하 여](../../data/mfc-using-database-classes-with-documents-and-views.md)입니다.

기본적으로 MFC 응용 프로그램 마법사를 지원 하지 않는 데이터베이스는 기본 응용 프로그램을 만듭니다. 그러나 최소 데이터베이스 지원 또는 전체 폼 기반 지원을 포함 하는 옵션을 선택할 수 있습니다. 응용 프로그램 마법사 옵션에 대 한 자세한 내용은 참조 하세요. [MFC 응용 프로그램 마법사, 데이터베이스 지원](../../mfc/reference/database-support-mfc-application-wizard.md)합니다.

또한 전체 문서/뷰 아키텍처를 사용 하지 않고 데이터베이스 클래스를 사용할 수 있습니다. 자세한 내용은 [MFC: 문서 데이터베이스 클래스를 사용 하 여 뷰와](../../data/mfc-using-database-classes-without-documents-and-views.md)합니다.

## <a name="see-also"></a>참고 항목

[ODBC 및 MFC](../../data/odbc/odbc-and-mfc.md)