---
title: MFC MBCS DLL 추가 기능 | Microsoft Docs
ms.custom: ''
ms.date: 1/04/2018
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- MBCS
- MFC
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: aa6840fe54478b88e201dd09950917b95c7a1cc4
ms.sourcegitcommit: 76fd30ff3e0352e2206460503b61f45897e60e4f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/13/2018
ms.locfileid: "39025736"
---
# <a name="mfc-mbcs-dll-add-on"></a>MFC MBCS DLL 추가 기능

MFC에 대 한 지원 및 멀티 바이트 문자 집합 (MBCS) 라이브러리는 Visual Studio 2013, 2015 및 2017의에서 Visual Studio를 설치 하는 동안는 추가 단계가 필요 합니다.

**Visual Studio 2013**: 기본적으로 Visual Studio 2013에 설치 하는 MFC 라이브러리만 유니코드 개발 지원. 에 Visual Studio 2013의 MFC 프로젝트를 빌드하려면 MBCS Dll이 필요 합니다 **문자 집합** 속성이로 설정 **멀티 바이트 문자 집합 사용** 또는 **설정 되지 않은**합니다. DLL을 다운로드 [Visual Studio 2013 용 멀티 바이트 MFC 라이브러리](https://www.microsoft.com/download/details.aspx?id=40770)합니다.

**Visual Studio 2015**: 모두 유니코드 및 MBCS MFC Dll Visual c + + 설치 구성 요소에 포함 되지만 지원이 MFC가 기본적으로 설치 되지 않습니다. Visual C++ 및 MFC는 Visual Studio 설치 프로그램에서 선택적 설치 구성입니다. MFC가 설치되었는지 확인하려면 설치 프로그램에서 **사용자 지정** 을 선택하고 **프로그래밍 언어**에서 **Visual C++** 및 **C++용 Microsoft Foundation Classes** 가 선택되어 있는지 확인합니다. Visual Studio를 이미 설치한 경우 MFC 프로젝트를 만들려고 하면 Visual C++ 및/또는 MFC를 설치하라는 메시지가 표시됩니다.

**Visual Studio 2017**: 유니코드 및 MBCS MFC Dll와 함께 설치 되는 **c + +를 사용한 데스크톱 개발** 워크 로드를 선택 하면 **MFC 및 ATL 지원** 에서 **옵션 구성 요소** 창입니다. 설치에는 이러한 구성 요소 포함 되어 있지 않으면로 이동 합니다 **파일 | 새 프로젝트** 대화 상자를 클릭 합니다 **Visual Studio 설치 관리자 열기** 링크 합니다.

## <a name="see-also"></a>참고자료

[MFC 라이브러리 버전](../mfc/mfc-library-versions.md)

