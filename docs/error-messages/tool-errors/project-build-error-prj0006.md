---
title: 프로젝트 빌드 오류 PRJ0006 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- PRJ0006
dev_langs:
- C++
helpviewer_keywords:
- PRJ0006
ms.assetid: ce092be4-1652-414f-8cb5-b97ef5841f89
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 264b2f90a2d778b1545117ce5c3b1272626ebad6
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46073254"
---
# <a name="project-build-error-prj0006"></a>프로젝트 빌드 오류 PRJ0006

'File' 임시 파일을 열 수 없습니다. 파일이 있는지, 그리고 디렉터리 쓰기 금지 되어 있는지 확인 합니다.

Visual c + + 빌드 프로세스 중 임시 파일을 만들 수 없습니다. 이 대 한 이유:

- 임시 디렉터리가 없습니다.

- 읽기 전용으로 임시 디렉터리입니다.

- 디스크 공간이 부족 합니다.

- $ (Intdir) 폴더는 읽기 전용 이거나 읽기 전용 된 임시 파일을 포함 합니다.

다음 오류 PRJ0007도이 오류가 발생 합니다. 'directory' 출력 디렉터리를 만들지 못했습니다. 오류 PRJ0007 $ (intdir) 디렉터리를 만들 수 없습니다를 일시적으로 파일의 생성을 나타내므로 실패를 의미 합니다.

지정할 때마다 임시 파일이 생성 됩니다.

- 응답 파일입니다.

- 사용자 지정 빌드 단계입니다.

- 빌드 이벤트입니다.