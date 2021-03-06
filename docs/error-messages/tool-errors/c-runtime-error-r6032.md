---
title: C 런타임 오류 R6032 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- R6032
dev_langs:
- C++
helpviewer_keywords:
- R6032
ms.assetid: 52092a63-cc51-444a-bfc3-fad965a3558e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7dc68723e07d7ef8c3b9d9f6ad913466b7ff27e4
ms.sourcegitcommit: 997e6b7d336cddb388bb6e9e56527725fcaa0624
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2018
ms.locfileid: "48859720"
---
# <a name="c-runtime-error-r6032"></a>C 런타임 오류 R6032

로캘 정보에 대 한 공간 부족

> [!NOTE]
> 앱을 실행 하는 동안이 오류 메시지를 발생 하는 경우 앱 종료가 내부 메모리 문제가 있기 때문입니다. 이 오류에 대 한 몇 가지 가능한 이유는 없지만 아주 짧을 뿐 아니라 메모리가 부족 하거나 프로그램의 버그로 인해 발생 한 경우가 많습니다.
>
> 이 오류를 해결하려면 다음 단계를 시도할 수 있습니다.
>
> - 실행 중인 다른 응용 프로그램을 닫거나 메모리 확보 하기 위해 컴퓨터를 다시 시작 합니다.
> - 사용 하 여 합니다 **앱 및 기능** 또는 **프로그램 및 기능** 페이지를 **제어판** 를 복구 하거나 프로그램을 다시 설치 합니다.
> - 확인할 **Windows 업데이트** 에 **제어판** 소프트웨어 업데이트에 대 한 합니다.
> - 앱의 업데이트 된 버전을 확인 합니다. 문제가 지속 되는 경우 앱 공급 업체에 문의 합니다.

**프로그래머를 위한 정보**

런타임 로캘 구분 함수에 대 한 호출을 처리할 수 있도록 각 스레드의 로캘에 대 한 정보를 유지 합니다. 이 정보에 대 한 메모리 할당이 실패 하면 런타임이 종속 되어 있으므로 기본 기능을 너무 많이 계속할 수 없는 경우.