---
title: /FUNCTIONPADMIN (핫 패치 가능 이미지 만들기) | Microsoft Docs
ms.custom: ''
ms.date: 03/09/2018
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /functionpadmin
dev_langs:
- C++
helpviewer_keywords:
- -FUNCTIONPADMIN linker option
- /FUNCTIONPADMIN linker option
ms.assetid: 25b02c13-1add-4fbd-add9-fcb30eb2cae7
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7a82611c453a96e9247e414d6adb777c07320482
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45703991"
---
# <a name="functionpadmin-create-hotpatchable-image"></a>/FUNCTIONPADMIN(핫 패치 가능 이미지 만들기)

핫 패치 가능한 이미지를 준비합니다.

## <a name="syntax"></a>구문

> **/FUNCTIONPADMIN**[**:**_space_]

### <a name="arguments"></a>인수

*space*<br/>
바이트에 있는 각 함수의 시작 부분에 추가할 안쪽 여백의 양입니다. X86이 기본적으로 5 바이트의 패딩이 고 기본값은 6 바이트 x64. 다른 대상에 값을 제공 해야 합니다.

## <a name="remarks"></a>설명

핫 패치 가능 이미지를 생성 하도록 링커에 대 한 순서로.obj 파일 해야 사용 하 여 컴파일된 [/hotpatch (핫 패치 가능 이미지 만들기)](../../build/reference/hotpatch-create-hotpatchable-image.md)합니다.

컴파일 및 cl.exe 한 번 호출을 사용 하 여 이미지를 연결 하는 경우 **/hotpatch** 의미 **/functionpadmin**합니다.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 참조 하세요 [Visual c + + 프로젝트 속성 설정](../../ide/working-with-project-properties.md)합니다.

1. 선택 된 **구성 속성** > **링커** > **명령줄** 속성 페이지.

1. 입력 된 **/FUNCTIONPADMIN** 옵션 **추가 옵션**합니다. 선택할 **확인** 변경 내용을 저장 합니다.

### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.AdditionalOptions%2A>을 참조하세요.

## <a name="see-also"></a>참고자료

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)
