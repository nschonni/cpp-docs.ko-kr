---
title: BSCMAKE 명령 파일 (지시 파일) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- BSCMAKE, response file
- BSCMAKE, command file
- response files, BSCMAKE
- command files, BSCMAKE
- response files
- command files
ms.assetid: abdffeea-35c7-4f2d-8c17-7d0d80bac314
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 69fb144bed21b00fc07107f3fa8d5e64c1afb10d
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45716566"
---
# <a name="bscmake-command-file-response-file"></a>BSCMAKE 명령 파일(지시 파일)

일부 또는 전체 명령 파일에서 명령줄 입력을 제공할 수 있습니다. 다음 구문을 사용 하 여 명령 파일을 지정 합니다.

```
BSCMAKE @filename
```

하나의 명령 파일은 허용 됩니다. 사용 하 여 경로 지정할 수 있습니다 *filename*합니다. 앞에 야 *filename* 사용 하 여는 at 기호 (**\@**). BSCMAKE는 확장을 가정 하지 않습니다. 추가 지정할 수 있습니다 *sbrfiles* 한 후 명령줄에서 *filename*합니다. 명령 파일은 명령줄에서 지정 하는 것 처럼 동일한 순서로 BSCMAKE에 대 한 입력을 포함 하는 텍스트 파일입니다. 하나 이상의 공백, 탭 또는 줄 바꿈 문자를 사용 하 여 명령줄 인수를 구분 합니다.

다음 명령은 BSCMAKE 명령 파일을 사용 하 여 호출 합니다.

```
BSCMAKE @prog1.txt
```

다음은 샘플 명령 파일입니다.

```
/n /v /o main.bsc /El
/S (
toolbox.h
verdate.h c:\src\inc\screen.h
)
file1.sbr file2.sbr file3.sbr file4.sbr
```

## <a name="see-also"></a>참고 항목

[BSCMAKE 참조](../../build/reference/bscmake-reference.md)