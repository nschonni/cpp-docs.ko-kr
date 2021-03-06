---
title: 이전 버전의 런타임에서 C++ -clr 응용 프로그램 실행 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-ide
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- applications [C++], runtime version specified
- versions [C++]
- app.config files, runtime version specified
- compatibility [C++], runtime version specified
- backward compatibility [C++], runtime version specified
- application deployment [C++], runtime version specified
- common language runtime [C++], version specified
- deploying applications [C++], runtime version specified
ms.assetid: 940171b7-6937-4b14-8e87-c199e23f4f2e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ee823d7b37428ea335d5d789a4fcfb4caa673dda
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46378063"
---
# <a name="running-a-c-clr-application-on-a-previous-runtime-version"></a>이전 버전의 런타임에서 C++ /clr 응용 프로그램 실행

별도로 지정하지 않는 한, C++ .NET Framework 응용 프로그램은 컴파일러가 응용 프로그램을 빌드하는 데 사용하는 CLR(공용 언어 런타임) 버전에서 실행되도록 빌드됩니다. 그러나 특정 버전의 런타임용으로 빌드된 .exe 응용 프로그램은 필요한 기능을 제공하는 다른 버전에서 실행될 수 있습니다.

이 작업을 수행하려면 `supportedRuntime` 태그에 런타임 버전 정보가 포함된 app.config 파일을 제공하세요.

런타임 시 app.config 파일은 *filename.ext*.config 형식의 이름을 가져야 합니다. 여기서 *filename.ext*는 응용 프로그램을 시작한 실행 파일의 이름이고, 실행 파일과 동일한 디렉터리에 있어야 합니다. 예를 들어 응용 프로그램의 이름이 TestApp.exe인 경우 app.config 파일의 이름은 TestApp.exe.config가 됩니다.

둘 이상의 런타임 버전을 지정한 상태에서 응용 프로그램이 둘 이상의 런타임 버전이 설치된 컴퓨터에서 실행되는 경우, 응용 프로그램은 구성 파일에 지정되어 설치된 첫 번째 버전을 사용합니다.

## <a name="see-also"></a>참고 항목

[데스크톱 응용 프로그램 배포](../ide/deploying-native-desktop-applications-visual-cpp.md)