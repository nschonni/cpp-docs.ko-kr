---
title: NMAKE 심각한 오류 U1045 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- U1045
dev_langs:
- C++
helpviewer_keywords:
- U1045
ms.assetid: dc70d162-14b9-4107-9237-7514044d72e3
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c2b9be4f7440d9e79d603e917c1886aebe7c44af
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46056887"
---
# <a name="nmake-fatal-error-u1045"></a>NMAKE 심각한 오류 U1045

생성 실패: 메시지

NMAKE에 의해 호출된 프로그램이나 명령이 지정된 이유로 인해 실패했습니다. NMAKE에서 컴파일러나 링커 등의 다른 프로그램을 호출할 때 호출이 실패하거나 호출된 프로그램에서 오류를 반환할 수 있습니다. 이 메시지는 오류를 보고하는 데 사용됩니다.

이 문제를 해결하려면 먼저 오류의 원인을 확인합니다. NMAKE에서 보고 된 명령을 사용할 수 있습니다 [/N](../../build/nmake-options.md) 옵션 환경 설정을 확인 하 고 명령줄에서 NMAKE가 수행한 작업을 반복 합니다.