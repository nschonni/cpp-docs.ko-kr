---
title: 예외 (C/c + +) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- ERROR_MOD_NOT_FOUND
- vcppException
- ERROR_SEVERITY_ERROR
dev_langs:
- C++
helpviewer_keywords:
- vcppException
- C++ exception handling, delayed loading of DLLs
- delayed loading of DLLs, exceptions
- ERROR_SEVERITY_ERROR exception
- ERROR_MOD_NOT_FOUND exception
ms.assetid: c03be05d-1c39-4f35-84cf-00c9af3bae9a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7d32b22d0ac8a065d59030dccd144236a79c6ac8
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45705694"
---
# <a name="exceptions-cc"></a>예외(C/C++)

두 개의 예외 코드 오류가 발생 하는 경우 발생할 수 있습니다.

- 에 **LoadLibrary** 실패

- 에 **GetProcAddress** 실패

예외 정보는 다음과 같습니다.

```
//
// Exception information
//
#define FACILITY_VISUALCPP  ((LONG)0x6d)
#define VcppException(sev,err)  ((sev) | (FACILITY_VISUALCPP<<16) | err)
```

Throw 된 예외 코드는 표준 VcppException (ERROR_SEVERITY_ERROR, ERROR_MOD_NOT_FOUND) 및 (ERROR_SEVERITY_ERROR, ERROR_PROC_NOT_FOUND) VcppException 값. 예외에 대 한 포인터를 전달를 **DelayLoadInfo** 하 여 검색할 수 있는 LPDWORD 값 구조체 **GetExceptionInformation** 에 [EXCEPTION_RECORD](/windows/desktop/api/winnt/ns-winnt-_exception_record) 구조 [0] ExceptionInformation 필드입니다.

또한 grAttrs 필드에 잘못 된 비트가 설정 된 경우는 ERROR_INVALID_PARAMETER 예외가 발생 합니다. 이 예외는에 대 한 모든 용도 치명적입니다.

참조 [구조체 및 상수 정의](../../build/reference/structure-and-constant-definitions.md) 자세한 내용은 합니다.

## <a name="see-also"></a>참고 항목

[오류 처리 및 알림](../../build/reference/error-handling-and-notification.md)