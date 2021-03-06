---
title: '데이터 소스: 데이터 원본 (ODBC)의 스키마 확인 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-data
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- ODBC data sources [C++], schema
- schemas [C++], data sources
- data sources [C++], determining schema
ms.assetid: 17284acb-eb10-4f27-9944-ad1d973c0b05
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: b5ba9789226e54c9607e85caaa5e8af3f157f02d
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50052640"
---
# <a name="data-source-determining-the-schema-of-the-data-source-odbc"></a>데이터 소스: 데이터 소스의 스키마 확인(ODBC)

이 항목에서는 MFC ODBC 클래스에 적용 됩니다.

데이터 멤버를 설정 하 여 `CRecordset` 개체에 연결 되어 있는 데이터 원본의 스키마를 알아야 합니다. 데이터 원본의 스키마를 결정 하는 데이터 원본의 테이블 목록에서 모든 인덱스의 존재 여부 및 각 테이블의 열, 각 열의 데이터 형식 목록을 가져오는 포함 됩니다.

## <a name="see-also"></a>참고 항목

[데이터 소스(ODBC)](../../data/odbc/data-source-odbc.md)<br/>
[데이터 소스: 연결 관리(ODBC)](../../data/odbc/data-source-managing-connections-odbc.md)