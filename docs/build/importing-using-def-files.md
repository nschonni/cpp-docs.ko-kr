---
title: DEF 파일을 사용 하 여 가져오기 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- importing DLLs [C++], DEF files
- def files [C++], importing with
- .def files [C++], importing with
- dllimport attribute [C++], DEF files
- DLLs [C++], DEF files
ms.assetid: aefdbf50-f603-488a-b0d7-ed737bae311d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3e1562e14b20e4e1dd96764414978889d6205179
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45710543"
---
# <a name="importing-using-def-files"></a>DEF 파일을 사용하여 가져오기

사용 하려는 경우 **__declspec (dllimport)** .def 파일을 함께 잘못 된 코딩 문제가 발생할 수 있는 가능성을 줄이기 위해 상수 대신 데이터를 사용 하려면.def 파일을 변경 해야 합니다.

```
// project.def
LIBRARY project
EXPORTS
   ulDataInDll   DATA
```

다음 표에서 이유를 보여 줍니다.

|키워드|가져오기 라이브러리에 내보냅니다.|내보내기|
|-------------|---------------------------------|-------------|
|`CONSTANT`|`_imp_ulDataInDll`, `_ulDataInDll`|`_ulDataInDll`|
|`DATA`|`_imp_ulDataInDll`|`_ulDataInDll`|

사용 하 여 **__declspec (dllimport)** 상수를 모두 나열 하 고는 `imp` .lib DLL에서에서 데코 레이트 되지 않은 이름과 버전 가져오기 명시적 연결을 허용 하기 위해 만들어지는 라이브러리입니다. 사용 하 여 **__declspec (dllimport)** 및 데이터 목록만 `imp` 버전의 이름입니다.

상수를 사용 하면 다음과 같은 코드 구문이 중 사용할 수 있는지에 액세스 하려면 `ulDataInDll`:

```
__declspec(dllimport) ULONG ulDataInDll; /*prototype*/
if (ulDataInDll == 0L)   /*sample code fragment*/
```

\-또는-

```
ULONG *ulDataInDll;      /*prototype*/
if (*ulDataInDll == 0L)  /*sample code fragment*/
```

그러나.def 파일에 데이터를 사용 하는 경우 다음 정의 사용 하 여 컴파일한 코드 에서만 액세스할 수 있습니다 변수의 `ulDataInDll`:

```
__declspec(dllimport) ULONG ulDataInDll;

if (ulDataInDll == 0L)   /*sample code fragment*/
```

상수를 사용 하 여 이므로 더 위험한 변수에 대 한 포인터 가져오기 주소 테이블을 추가 수준의 간접 참조를 사용 하지 않으면 잠재적으로 액세스할 수 없습니다-변수 자체가 없습니다. 이러한 유형의 문제는 가져오기 주소 테이블은 되기 때문에 현재 읽기 전용 컴파일러 및 링커에 자주 액세스 위반으로 나타날 수 있습니다.

이 경우를 고려 하는.def 파일에 상수를 발견 하는 경우 현재 Visual c + + 링커는 경고가 발생 합니다. 상수를 사용 하는 유일한 이유는 헤더 파일에 나열 되지 않은 일부 개체 파일을 다시 컴파일할 수 없는 경우 **__declspec (dllimport)** 프로토타입을에 있습니다.

## <a name="see-also"></a>참고 항목

[응용 프로그램으로 가져오기](../build/importing-into-an-application.md)
