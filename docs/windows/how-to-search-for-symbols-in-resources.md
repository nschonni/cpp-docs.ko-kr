---
title: '방법: 리소스 (c + +)에서 기호 검색 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- symbols [C++], finding
- resources [C++], searching for symbols
ms.assetid: 6efef8e8-d0d4-4c49-b895-314974e7791a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: b4adac3b4e593ab19287e21e5a965f3a28d008b8
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46427617"
---
# <a name="how-to-search-for-symbols-in-resources-c"></a>방법: 리소스 (c + +)에서 기호 검색

### <a name="to-find-symbols-in-resources"></a>리소스에서 기호를 찾으려면

1. **편집할** 메뉴 선택 **기호 찾기**합니다.

2. 에 [기호 찾기 대화 상자](/visualstudio/ide/go-to)를 **찾을 내용** 상자, 드롭 다운 목록에서 이전에 검색 문자열을 선택 하거나 (예: ID_ACCEL1) 찾으려는 액셀러레이터 키를 입력 합니다.

   > [!TIP]
   > 사용 하도록 [정규식](/visualstudio/ide/using-regular-expressions-in-visual-studio) 검색을 사용 해야 합니다는 [파일에서에서 찾기 명령](/visualstudio/ide/reference/find-command) 에서 합니다 **편집** 대신 메뉴는 **기호 찾기**명령입니다. 정규식을 사용 하도록 설정 하려면 해야는 **사용: Regular Expressions** 확인란을 선택 합니다 [찾기 대화 상자](/visualstudio/ide/finding-and-replacing-text). 오른쪽의 오른쪽 화살표 단추를 클릭 합니다 **찾을 내용** 정규 검색 식의 목록을 표시 하려면 상자입니다. 검색 텍스트로 대체 식을이 목록에서를 선택 하면 합니다 **찾을 내용** 상자입니다.

3. 중 하나를 선택 합니다 **찾을** 옵션입니다.

4. 클릭 **다음 찾기**합니다.

   > [!NOTE]
   > 문자열, 액셀러레이터 또는 이진 리소스에서 기호를 검색할 수 없습니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 리소스에 액세스 하는 관리 되는 프로젝트에 리소스 파일을 수동으로 추가 하는 방법은 속성에 문자열, 정적 리소스 표시 및 리소스를 할당 합니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[기호: 리소스 식별자](../windows/symbols-resource-identifiers.md)<br/>
[리소스 파일](../windows/resource-files-visual-studio.md)<br/>
[리소스 편집기](../windows/resource-editors.md)