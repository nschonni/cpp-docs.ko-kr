---
title: ATL 마법사로 추가한 ATL 지원의 세부 정보 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: reference
f1_keywords:
- vc.codewiz.atl.support
dev_langs:
- C++
helpviewer_keywords:
- MFC, ATL support
- ATL, MFC projects
ms.assetid: aa66bad0-008f-4886-94c1-2a0a0d04bce4
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: efa96037139e61e16b752b45617bb8a3c54be993
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46442151"
---
# <a name="details-of-atl-support-added-by-the-atl-wizard"></a>ATL 마법사로 추가한 ATL 지원에 대한 세부 정보

경우 있습니다 [기존 MFC 실행 파일 또는 DLL에 ATL 지원 추가](../../mfc/reference/adding-atl-support-to-your-mfc-project.md), Visual c + +에서 기존 MFC 프로젝트에 다음과 같이 수정 하면 (이 예제에서는 프로젝트 라고 `MFCEXE`):

- 두 개의 새 파일 (.idl 파일 및 서버를 등록 하는 데.rgs 파일) 추가 됩니다.

- (Mfcexe.h 및 Mfcexe.cpp) 주 응용 프로그램 헤더 파일과 구현 파일에서 새 클래스 (에서 파생 된 `CAtlMFCModule`) 추가 됩니다. 새 클래스 외에도 코드에 추가 됩니다 `InitInstance` 등록 합니다. 코드에도 추가 됩니다는 `ExitInstance` 클래스 개체를 해지 하는 것에 대 한 함수입니다. 헤더 파일에 마지막으로 두 개의 새 헤더 파일 (Initguid.h 및 Mfcexe_i.c)에 포함시킬지 구현 파일 선언 및 초기화에 대 한 새 Guid를 `CAtlMFCModule`-클래스를 파생 합니다.

- 서버에 올바르게 등록 하려면 새.rgs 파일에 대 한 항목이 프로젝트의 리소스 파일에 추가 됩니다.

## <a name="notes-for-dll-projects"></a>DLL 프로젝트에 대 한 정보

MFC DLL 프로젝트에 ATL 지원을 추가 하면 약간의 차이가 표시 됩니다. 코드를 추가 하는 `DLLRegisterServer` 및 `DLLUnregisterServer` 함수를 등록 하 고 DLL의 등록을 취소 합니다. 코드에도 추가 됩니다 [DllCanUnloadNow](../../atl/reference/catldllmodulet-class.md#dllcanunloadnow) 하 고 [DllGetClassObject](../../atl/reference/catldllmodulet-class.md#dllgetclassobject)합니다.

## <a name="see-also"></a>참고 항목

[MFC 프로젝트에 ATL 지원](../../mfc/reference/adding-atl-support-to-your-mfc-project.md)<br/>
[코드 마법사로 기능 추가](../../ide/adding-functionality-with-code-wizards-cpp.md)<br/>
[클래스 추가](../../ide/adding-a-class-visual-cpp.md)<br/>
[멤버 함수 추가](../../ide/adding-a-member-function-visual-cpp.md)<br/>
[멤버 변수 추가](../../ide/adding-a-member-variable-visual-cpp.md)<br/>
[가상 함수 재정의](../../ide/overriding-a-virtual-function-visual-cpp.md)<br/>
[MFC 메시지 처리기](../../mfc/reference/adding-an-mfc-message-handler.md)<br/>
[클래스 구조 탐색](../../ide/navigating-the-class-structure-visual-cpp.md)
