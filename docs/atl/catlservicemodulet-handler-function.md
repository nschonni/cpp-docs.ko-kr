---
title: 'Catlservicemodulet:: Handler 함수 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-atl
ms.topic: conceptual
f1_keywords:
- CServiceModule::Handler
- CServiceModule.Handler
- Handler
dev_langs:
- C++
helpviewer_keywords:
- Handler method
ms.assetid: 14db5f2a-be87-4774-a296-445cb6fc7b2e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 7c8dc0b0d41a18c775258e1eacddd8e4dbebdb3d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46039220"
---
# <a name="catlservicemodulethandler-function"></a>Catlservicemodulet:: Handler 함수

`CAtlServiceModuleT::Handler` 서비스 제어 관리자 (SCM) 서비스의 상태를 검색 하 고 다양 한 지침 (예: 중지 또는 일시 중지)를 호출 하는 루틴입니다. SCM 전달 하기 위한 작업 코드 `Handler` 서비스가 수행할 동작을 나타냅니다. 기본 ATL 생성 서비스 중지 명령을 처리합니다. 중지 명령이 SCM를 통과 하면 서비스 인지 여부를 SCM는 프로그램을 중지 하려고 합니다. 서비스 호출 `PostThreadMessage` 자신에 게 종료 메시지를 게시 합니다. 메시지 루프를 종료 하 고 서비스를 궁극적으로 닫힙니다.

자세한 지침을 처리 하려면 변경 해야 합니다 `m_status` 데이터 멤버의 초기화를 `CAtlServiceModuleT` 생성자입니다. 이 데이터 멤버 서비스 제어판 응용 프로그램에서 서비스를 선택한 경우 사용할 수 있도록 단추를 SCM에 지시 합니다.

## <a name="see-also"></a>참고 항목

[서비스](../atl/atl-services.md)<br/>
[Catlservicemodulet:: Handler](../atl/reference/catlservicemodulet-class.md#handler)

