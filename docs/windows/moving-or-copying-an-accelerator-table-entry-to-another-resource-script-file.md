---
title: 다른 리소스 스크립트 파일 (c + +)에 액셀러레이터 키 테이블 항목을 복사 또는 이동 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- accelerator tables [C++], copying entries
- rc files [C++], moving an accelerator table entry
- .rc files [C++], moving accelerator table entries
- accelerator tables [C++], moving entries
ms.assetid: 7b4dc149-c972-4ab2-8477-76c52b6feb5b
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 0d3f75ef8c2820c227716e3208ff2cded54d1fd7
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46414734"
---
# <a name="moving-or-copying-an-accelerator-table-entry-to-another-resource-script-file-c"></a>다른 리소스 스크립트 파일 (c + +)에 액셀러레이터 키 테이블 항목을 복사 또는 이동

### <a name="to-move-or-copy-an-accelerator-table-entry-to-another-resource-script-file"></a>액셀러레이터 키 테이블 항목을 다른 리소스 스크립트 파일로 이동/복사

1. 두 리소스 스크립트 파일 모두에서 액셀러레이터 키 테이블을 엽니다.

   > [!NOTE]
   > 프로젝트에 .rc 파일이 아직 없는 경우 [새 리소스 스크립트 파일 만들기](../windows/how-to-create-a-resource-script-file.md)를 참조하세요.

2. 이동하려는 항목을 선택합니다.

3. **편집할** 메뉴에서 선택 **복사** 또는 **잘라내기**합니다.

4. 대상 리소스 스크립트 파일에서 항목을 선택합니다.

5. **편집할** 메뉴 선택 **붙여넣기**합니다.

   > [!NOTE]
   > 복사 및 붙여넣기의 바로 가기 키를 사용할 수도 있습니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[액셀러레이터 키 테이블 편집](../windows/editing-accelerator-tables.md)<br/>
[액셀러레이터 키 편집기](../windows/accelerator-editor.md)