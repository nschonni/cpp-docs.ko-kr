---
title: 액셀러레이터 키 한정자 속성 (c + +) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- Modifier property
ms.assetid: f05a9379-e037-4cfb-b6ef-d2c655bcfa7f
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 3c053af58842c75910b0214ae828c652daa33a81
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46389293"
---
# <a name="accelerator-modifier-property-c"></a>액셀러레이터 키 한정자 속성 (c + +)

액셀러레이터 키 테이블의 한정자 속성에 대해 사용할 수 있는 항목은 다음과 같습니다.

|값|설명|
|-----------|-----------------|
|**없음**|만 누르면 합니다 **키** 값입니다. 이 가장 효과적으로 사용 됩니다 026 통해 ASCII/ANSI 값 001로 해석 되는 ^ A-^ Z (CTRL + A CTRL + Z를 통해).|
|**Alt**|눌러야 합니다 **Alt** 하기 전에 키를 **키** 값입니다.|
|**Ctrl**|눌러야 합니다 **Ctrl** 하기 전에 키를 **키** 값입니다. ASCII 형식으로 유효 하지 않습니다.|
|**Shift**|눌러야 합니다 **Shift** 하기 전에 키를 **키** 값입니다.|
|**Ctrl + Alt**|눌러야 합니다 **Ctrl** 키와 **Alt** 하기 전에 키를 **키** 값. ASCII 형식으로 유효 하지 않습니다.|
|**Ctrl + Shift**|눌러야 합니다 **Ctrl** 키와 **Shift** 하기 전에 키를 **키** 값. ASCII 형식으로 유효 하지 않습니다.|
|**Alt + Shift**|눌러야 합니다 **Alt** 키 및 **Shift** 하기 전에 키를 **키** 값입니다. ASCII 형식으로 유효 하지 않습니다.|
|**Ctrl + Alt + Shift**|눌러야 **Ctrl**를 **Alt**, 및 **Shift** 전에 **키** 값입니다. ASCII 형식으로 유효 하지 않습니다.|

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[액셀러레이터 키 속성 설정](../windows/setting-accelerator-properties.md)<br/>
[액셀러레이터 키 편집기](../windows/accelerator-editor.md)