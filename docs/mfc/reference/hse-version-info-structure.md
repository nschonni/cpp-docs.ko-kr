---
title: HSE_VERSION_INFO 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: reference
f1_keywords:
- HSE_VERSION_INFO
dev_langs:
- C++
helpviewer_keywords:
- HSE_VERSION_INFO structure [MFC]
ms.assetid: 4837312d-68c8-4d05-9afa-1934d7d49b20
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 08b16c59f155864a781feccbfd08842380cccd01
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46433805"
---
# <a name="hseversioninfo-structure"></a>HSE_VERSION_INFO 구조체

이 구조는 가리키는 합니다 *pVer* 에 매개 변수는 `CHttpServer::GetExtensionVersion` 멤버 함수입니다. ISA 버전 번호 및 텍스트는 ISA. 설명은 제공

## <a name="syntax"></a>구문

```
typedef struct _HSE_VERSION_INFO {
    DWORD dwExtensionVersion;
    CHAR lpszExtensionDesc[HSE_MAX_EXT_DLL_NAME_LEN];
} HSE_VERSION_INFO, *LPHSE_VERSION_INFO;
```

#### <a name="parameters"></a>매개 변수

*dwExtensionVersion*<br/>
ISA.의 버전 번호

*lpszExtensionDesc*<br/>
텍스트에 대 한 설명은 ISA. 기본 구현은 자리 표시자 텍스트를 제공합니다. 재정의 `CHttpServer::GetExtensionVersion` 고유한 설명을 제공 합니다.

## <a name="requirements"></a>요구 사항

**헤더:** httpext.h

## <a name="see-also"></a>참고 항목

[구조체, 스타일, 콜백 및 메시지 맵](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)

