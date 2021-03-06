---
title: -hotpatch (핫 패치 가능 이미지 만들기) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /hotpatch
- VC.Project.VCCLCompilerTool.CreateHotpatchableImage
dev_langs:
- C++
helpviewer_keywords:
- hot patching
- -hotpatch compiler option [C++]
- /hotpatch compiler option [C++]
- hotpatching
ms.assetid: aad539b6-c053-4c78-8682-853d98327798
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 97e1b6197ea60099457db7788ad7e24b96c9fcb8
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45716978"
---
# <a name="hotpatch-create-hotpatchable-image"></a>/hotpatch(핫 패치 가능 이미지 만들기)

핫 패치 가능한 이미지를 준비합니다.

## <a name="syntax"></a>구문

```
/hotpatch
```

## <a name="remarks"></a>설명

때 **/hotpatch** 는 컴파일에서 컴파일러는 각 함수의 첫 번째 명령이 최소한 2 바이트가 되도록, 핫 패치에 필요한 합니다.

사용 하 여는 이미지 핫 패치 가능 하기 위한 준비를 완료 하려면 **/hotpatch** 컴파일하려면를 사용 해야 [/FUNCTIONPADMIN (핫 패치 가능 이미지 만들기)](../../build/reference/functionpadmin-create-hotpatchable-image.md) 연결 합니다. 컴파일 및 cl.exe를 한 호출을 사용 하 여 이미지를 연결 하는 경우 **/hotpatch** 의미 **/functionpadmin**합니다.

지침은 항상 2 바이트 이상 ARM 아키텍처 이므로 컴파일은 항상 처리 하는 x64 처럼 **/hotpatch** 지정 지정할 필요가 **/hotpatch** 때 이러한 대상;에 대 한 컴파일 그러나 사용 하 여 여전히 연결 해야 합니다 **/functionpadmin** 에 핫 패치 가능 이미지를 만들 수 있습니다. 합니다 **/hotpatch** 컴파일러 옵션만 영향을 줍니다 x86 컴파일.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. 선택 된 **C/c + +** 폴더입니다.

1. 선택 된 **명령줄** 속성 페이지.

1. 컴파일러 옵션을 추가 합니다 **추가 옵션** 상자입니다.

### <a name="to-set-this-compiler-option-programmatically"></a>프로그래밍 방식으로 이 컴파일러 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>을 참조하세요.

## <a name="guidance"></a>지침

업데이트 관리에 대 한 자세한 내용은 "업데이트 관리에 대 한 보안 지침"를 참조 [ http://www.microsoft.com/technet/security/guidance/PatchManagement.mspx ](http://www.microsoft.com/technet/security/guidance/PatchManagement.mspx)합니다.

## <a name="see-also"></a>참고 항목

[컴파일러 옵션](../../build/reference/compiler-options.md)<br/>
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)