---
title: -Gw (전역 데이터 최적화) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /Gw
dev_langs:
- C++
helpviewer_keywords:
- /Gw compiler option [C++]
- -Gw compiler option [C++]
ms.assetid: 6f90f4e9-5eb8-4c47-886e-631278a5a4a9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: edb0dc94ce7c2193717be4cdb402fdea14c99b71
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45712545"
---
# <a name="gw-optimize-global-data"></a>/Gw(전역 데이터 최적화)

최적화를 위한 COMDAT 섹션의 전역 데이터 패키지

## <a name="syntax"></a>구문

```
/Gw[-]
```

## <a name="remarks"></a>설명

합니다 **/Gw** 옵션을 개별 COMDAT 섹션에서 컴파일러가 전역 데이터 패키지를 사용 하면 됩니다. 기본적으로 **/Gw** 해제 되 고 명시적으로 설정 해야 합니다. 명시적으로 사용 하지 않도록를 사용 하 여 **/Gw-** 합니다. 때 둘 다 **/Gw** 하 고 [/GL](../../build/reference/gl-whole-program-optimization.md) 는 사용 하도록 설정, 링커를 사용 하 여 전체 프로그램 최적화 병합 또는 참조 되지 않은 전역 데이터를 제외 하기 위해 여러 개체 파일에서 COMDAT 섹션을 비교 동일한 읽기 전용 전역 데이터입니다. 이렇게 하면 결과로 생성되는 바이너리 실행 파일의 크기를 크게 줄일 수 있습니다.

를 컴파일하고 개별적으로 연결 하는 경우 사용할 수 있습니다는 [/opt: ref](../../build/reference/opt-optimizations.md) 링커 옵션으로 컴파일된 개체 파일에 참조 되지 않은 전역 데이터 파일을 실행에서 제외할 합니다 **/Gw** 옵션입니다.

사용할 수도 있습니다는 [/opt: icf](../../build/reference/opt-optimizations.md) 하 고 [/LTCG](../../build/reference/ltcg-link-time-code-generation.md) 링커 옵션을 함께 사용 하 여 여러 개체 파일 간에 동일한 읽기 전용 전역 데이터 컴파일된 실행 파일에 병합 합니다 **/Gw** 옵션입니다.

자세한 내용은 [/Gw 컴파일러 스위치 소개](http://blogs.msdn.com/b/vcblog/archive/2013/09/11/introducing-gw-compiler-switch.aspx) Visual c + + 팀 블로그.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. 선택 된 **C/c + +** 폴더입니다.

1. 선택 된 **명령줄** 속성 페이지.

1. 수정 된 **추가 옵션** 포함할 속성을 **/Gw** 를 선택한 후 **확인**합니다.

### <a name="to-set-this-compiler-option-programmatically"></a>프로그래밍 방식으로 이 컴파일러 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>을 참조하세요.

## <a name="see-also"></a>참고 항목

[컴파일러 옵션](../../build/reference/compiler-options.md)<br/>
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)