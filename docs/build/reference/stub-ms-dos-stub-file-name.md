---
title: -STUB (MS-DOS 스텁 파일 이름) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /stub
- VC.Project.VCLinkerTool.DosStub
dev_langs:
- C++
helpviewer_keywords:
- Win32 [C++], attaching MS-DOS stub program
- STUB linker option
- MS-DOS stub file name linker option
- /STUB linker option
- Windows API [C++], attaching MS-DOS stub program
- -STUB linker option
ms.assetid: 65221ffe-4f9a-4a14-ac69-3cfb79b40b5f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 0c279d6f33befb4c308afe0c92b7dcca3d45ba66
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45707722"
---
# <a name="stub-ms-dos-stub-file-name"></a>/STUB(MS-DOS 스텁 파일 이름)

```
/STUB:filename
```

## <a name="arguments"></a>인수

*filename*<br/>
MS-DOS 응용 프로그램입니다.

## <a name="remarks"></a>설명

/STUB 옵션을 Win32 프로그램 MS-DOS 스텁 프로그램을 연결합니다.

스텁 프로그램 파일 MS-DOS에서 실행 되는 경우 호출 됩니다. 일반적으로 적절 한 메시지를; 표시 그러나 모든 유효한 MS-DOS 응용 프로그램에 스텁 프로그램을 수 있습니다.

지정 된 *filename* 스텁 프로그램 명령줄에 콜론 (:)에 대 한 합니다. 링커 검사 *filename* 및 파일을 실행할 수 없는 경우 오류 메시지를 발생 시킵니다. 프로그램은.exe 파일; 이어야 합니다. .com 파일 스텁 프로그램에 대해 올바르지 않습니다.

이 옵션을 사용 하지 않으면 링커 다음 메시지를 발급 하는 기본 스텁 프로그램을 연결 합니다.

```
This program cannot be run in MS-DOS mode.
```

가상 장치 드라이버를 빌드하면 *filename* (WINNT에 정의 된 IMAGE_DOS_HEADER 구조를 포함 하는 파일 이름을 지정 하면. H) 데 사용할 기본 헤더가 아닌 VXD 합니다.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 참조 하세요 [Visual c + + 프로젝트 속성 설정](../../ide/working-with-project-properties.md)합니다.

1. 클릭 합니다 **링커** 폴더입니다.

1. **명령줄** 속성 페이지를 클릭합니다.

1. 에 옵션을 입력 합니다 **추가 옵션** 상자입니다.

### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.AdditionalOptions%2A>을 참조하세요.

## <a name="see-also"></a>참고 항목

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)