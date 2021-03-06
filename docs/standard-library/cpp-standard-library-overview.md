---
title: C++ 표준 라이브러리 개요 | Microsoft 문서
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- headers, C++ library
- C++ Standard Library
- libraries, Standard C++
- C++ Standard Library, headers
ms.assetid: 7acb83a4-da73-4ad3-bc30-a71289db7f60
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2795ab431930627160b0275866b573aff36bb97b
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/07/2018
ms.locfileid: "33845322"
---
# <a name="c-standard-library-overview"></a>C++ 표준 라이브러리 개요

모든 C++ 라이브러리 엔터티가 하나 이상의 표준 헤더에서 선언되거나 정의됩니다. 이 구현에는 두 개의 추가 헤더 포함 됩니다. \<hash_map > 및 \<hash_set >, c + + 표준에 따라 필요 하지 않습니다. 이 구현에서 지원되는 헤더의 전체 목록을 보려면 [헤더 파일 참조](../standard-library/cpp-standard-library-header-files.md)를 참조하세요.

C++ 라이브러리의 독립형 구현에서는 이러한 헤더의 하위 집합만을 제공합니다.

|||
|-|-|
|[\<cstddef>](../standard-library/cstddef.md)|[\<cstdlib>](../standard-library/cstdlib.md)(적어도 함수 `abort`, `atexit` 및 `exit`를 선언함)|
|[\<exception>](../standard-library/exception.md)|[\<limits>](../standard-library/limits.md)|
|[\<new>](../standard-library/new.md)|[\<cstdarg>](../standard-library/cstdarg.md)|

C++ 라이브러리 헤더에는 광범위한 두 개의 하위 영역이 있습니다.

- [iostreams](../standard-library/iostreams-conventions.md) 규칙입니다.

- [C++ 표준 라이브러리 참조](../standard-library/cpp-standard-library-reference.md) 규칙입니다.

이 섹션에는 다음 섹션이 포함되어 있습니다.

- [C++ 라이브러리 헤더 사용](../standard-library/using-cpp-library-headers.md)

- [C++ 라이브러리 규칙](../standard-library/cpp-library-conventions.md)

- [iostreams 규칙](../standard-library/iostreams-conventions.md)

- [C++ 프로그램 시작 및 종료](../standard-library/cpp-program-startup-and-termination.md)

- [안전한 라이브러리: C++ 표준 라이브러리](../standard-library/safe-libraries-cpp-standard-library.md)

- [확인된 반복기](../standard-library/checked-iterators.md)

- [Debug Iterator Support](../standard-library/debug-iterator-support.md)

- [C++ 표준 라이브러리 참조](../standard-library/cpp-standard-library-reference.md)

- [C++ 표준 라이브러리의 스레드 보안](../standard-library/thread-safety-in-the-cpp-standard-library.md)

- [stdext 네임스페이스](../standard-library/stdext-namespace.md)

- [정규식(C++)](../standard-library/regular-expressions-cpp.md)

Visual C++ 런타임 라이브러리에 대한 자세한 내용은 [CRT 라이브러리 기능](../c-runtime-library/crt-library-features.md)을 참조하세요.

## <a name="see-also"></a>참고자료

[C++ 표준 라이브러리](../standard-library/cpp-standard-library-reference.md)<br/>
