---
title: -NATVIS (PDB에 Natvis 추가) | Microsoft Docs
ms.date: 08/10/2017
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /natvis
- VC.Project.VCLinkerTool.ImportLIbrary
dev_langs:
- C++
helpviewer_keywords:
- NATVIS linker option
- /NATVIS linker option
- -NATVIS linker option
- Add Natvis file to PDB
ms.assetid: 8747fc0c-701a-4796-bb4d-818ab4465cca
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2c1a20fef785c0267eb630bf044c8cb9609605e2
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45708125"
---
# <a name="natvis-add-natvis-to-pdb"></a>/ NATVIS (PDB에 Natvis 추가)

> / NATVIS:*파일 이름*

## <a name="parameters"></a>매개 변수

*filename*<br/>
PDB 파일에 추가할 Natvis 파일입니다. PDB에 Natvis 파일의 디버거 시각화 포함 합니다.

## <a name="remarks"></a>설명

/NATVIS 옵션 Natvis 파일에 정의 된 디버거 시각화를 포함 *filename* 링크에 의해 생성 된 PDB 파일에 있습니다. 따라서 디버거를.natvis 파일을 독립적으로 시각화를 표시할 수 있습니다. 생성된 된 PDB 파일에 둘 이상의 Natvis 파일을 포함 하려면 여러 /NATVIS 옵션을 사용할 수 있습니다.

PDB 파일을 사용 하 여 만들어지지 않은 경우 링크 무시 /NATVIS를 [디버그/](../../build/reference/debug-generate-debug-info.md) 옵션입니다. .Natvis 파일의 생성 및 사용에 대 한 내용은 참조 하세요 [Visual Studio 디버거에서 네이티브 개체의 사용자 지정 뷰 만들기](/visualstudio/debugger/create-custom-views-of-native-objects)합니다.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 참조 하세요 [Visual c + + 프로젝트 속성 설정](../../ide/working-with-project-properties.md)합니다.

1. 선택 된 **명령줄** 속성 페이지에는 **링커** 폴더.

1. /NATVIS 옵션을 추가 합니다 **추가 옵션** 입력란입니다.

### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면

- 이 옵션에 프로그래밍 방식으로 해당 하는 없습니다.

## <a name="see-also"></a>참고 항목

[Visual Studio 디버거에서 네이티브 개체의 사용자 지정 뷰 만들기](/visualstudio/debugger/create-custom-views-of-native-objects)<br/>
[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)