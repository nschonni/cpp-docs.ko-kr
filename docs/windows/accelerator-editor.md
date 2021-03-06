---
title: 액셀러레이터 키 편집기 (c + +) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: conceptual
f1_keywords:
- vc.editors.accelerator.F1
dev_langs:
- C++
helpviewer_keywords:
- accelerator tables [C++], editing
- tables [C++], accelerator key
- accelerator keys [C++]
- resource editors [C++], Accelerator editor
- keyboard shortcuts [C++], Accelerator editor
ms.assetid: 013c30b6-5d61-4f1c-acef-8bd15bed7060
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 42870002ff84b697599443da8ab9b9b88dbbd7ca
ms.sourcegitcommit: f0c90000125a9497bf61e41624de189a043703c0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44318800"
---
# <a name="accelerator-editor-c"></a>액셀러레이터 키 편집기 (c + +)

액셀러레이터 키 테이블은 연관 된 명령 식별자 및 액셀러레이터 키 (바로 가기 키 라고도 함)의 목록을 포함 하는 c + + Windows 리소스입니다. 프로그램에는 액셀러레이터 키 테이블이 두 개 이상 있을 수 있습니다.

일반적으로 액셀러레이터 키는 메뉴 또는 도구 모음에서도 사용할 수 있는 프로그램 명령에 대한 바로 가기 키로 사용됩니다. 그러나 연결된 사용자 인터페이스 개체가 없는 명령에 대한 키 조합을 정의하는 데 액셀러레이터 키 테이블을 사용할 수 있습니다.

사용할 수 있습니다 [클래스 뷰](/visualstudio/ide/viewing-the-structure-of-code) 액셀러레이터 키 명령을 코드에 연결 합니다.

사용 하 여는 **가속기** 편집기를 할 수 있습니다.

- [액셀러레이터 키 속성 설정](../windows/setting-accelerator-properties.md)

- [메뉴 항목과 액셀러레이터 키 연결](../windows/associating-an-accelerator-key-with-a-menu-item.md)

- [액셀러레이터 키 테이블 편집](../windows/editing-accelerator-tables.md)

- [사전 정의된 액셀러레이터 키 사용](../windows/predefined-accelerator-keys.md)

   > [!TIP]
   > 사용 하는 동안 합니다 **가속기** 자주 사용 되는 명령의 바로 가기 메뉴를 표시할 단추로 편집기입니다. 사용할 수 있는 명령은 포인터가 가리키는 내용에 따라 달라집니다.

   > [!NOTE]
   > Windows에서는 빈 액셀러레이터 키 테이블을 만들 수 없습니다. 항목이 없는 액셀러레이터 키 테이블을 만들 경우 해당 테이블을 저장할 때 테이블이 자동으로 삭제됩니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리 되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대 한 내용은 참조 하세요 [데스크톱 앱에 대 한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)합니다. 전역화 및 지역화 관리 되는 앱의 리소스에 대 한 내용은 참조 하세요 [Globalizing and Localizing.NET Framework Applications](/dotnet/standard/globalization-localization/index)합니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[리소스 편집기](../windows/resource-editors.md)