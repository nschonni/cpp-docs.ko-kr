---
title: -MANIFESTFILE (매니페스트 파일 이름) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- VC.Project.VCLinkerTool.ManifestFile
dev_langs:
- C++
helpviewer_keywords:
- MANIFESTFILE linker option
- -MANIFESTFILE linker option
- /MANIFESTFILE linker option
ms.assetid: befa5ab2-a9cf-4c9b-969a-e7b4a930f08d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7d3869b0cb656e7bde9a12fb028f84d1d4d09965
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45706981"
---
# <a name="manifestfile-name-manifest-file"></a>/MANIFESTFILE(매니페스트 파일 이름 지정)

```
/MANIFESTFILE:filename
```

## <a name="remarks"></a>설명

/MANIFESTFILE를 사용 하면 매니페스트 파일의 기본 이름을 변경할 수 있습니다.  매니페스트 파일의 기본 이름은 파일 이름에.manifest가 붙은입니다.

에 링크 하지 않은 경우 영향을 주지 것입니다 /MANIFESTFILE [매니페스트/](../../build/reference/manifest-create-side-by-side-assembly-manifest.md)합니다.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. **구성 속성** 노드를 확장합니다.

1. 확장 된 **링커** 노드.

1. 선택 된 **매니페스트 파일** 속성 페이지.

1. 수정 된 **매니페스트 파일** 속성입니다.

### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면

1. <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.ManifestFile%2A>을 참조하세요.

## <a name="see-also"></a>참고 항목

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)