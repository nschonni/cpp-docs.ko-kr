---
title: BSCMAKE 오류 BK1503 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- BK1503
dev_langs:
- C++
helpviewer_keywords:
- BK1503
ms.assetid: e6582344-b91e-486f-baf3-4f9028d83c3b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 16bf228804cb24f4fe7a2428dc581116d4cec91d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46064673"
---
# <a name="bscmake-error-bk1503"></a>BSCMAKE 오류 BK1503

'filename' 파일에 쓸 수 없습니다 [: 이유]

BSCMAKE는 하나의 브라우저 데이터베이스로 컴파일하는 동안 생성 된.sbr 파일을 결합 합니다. 이 오류는 결과 브라우저 데이터베이스 64MB를 초과 하는 경우, 입력 파일 (.sbr) 수가 4092 초과 하는 경우에 내보내집니다.

문제 4092 개 이상의.sbr 파일에서 발생 하는 경우 입력된 파일의 수를 줄여야 합니다. Visual Studio 내에서 수 이렇게 [/FR](../../build/reference/fr-fr-create-dot-sbr-file.md) 에 전체 프로젝트에 다음 파일에서 파일 단위로 다시 확인 합니다.

.Bsc 파일이 64MB 보다 큰 문제는 발생 하는 경우 입력으로.sbr 파일의 수를 줄이면 줄어듭니다 결과.bsc 파일의 크기입니다. 또한 찾아보기 정보의 양은 (매크로 확장 기호 제외) / e m, /El (로컬 변수 제외) 및 /Es (시스템 파일 제외) 줄일 수 있습니다.

## <a name="see-also"></a>참고 항목

[BSCMAKE 옵션](../../build/reference/bscmake-options.md)