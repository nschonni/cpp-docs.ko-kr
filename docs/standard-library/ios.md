---
title: '&lt;ios&gt; | Microsoft 문서'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
f1_keywords:
- <ios>
- ios/std::<ios>
dev_langs:
- C++
helpviewer_keywords:
- ios header
ms.assetid: d3d4c161-2f37-4f04-93cc-0a2a89984a9c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: fce633707096db8913da6d3601da20d14d3704c7
ms.sourcegitcommit: 3614b52b28c24f70d90b20d781d548ef74ef7082
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/11/2018
ms.locfileid: "38961485"
---
# <a name="ltiosgt"></a>&lt;ios&gt;

Iostreams 작업의 여러 기본 형식 및 함수를 정의합니다. 이 헤더는 일반적으로 다른 iostream 헤더에 의해 포함되며, 직접 포함하는 경우는 거의 없습니다.

## <a name="syntax"></a>구문

```cpp
#include <ios>

```

## <a name="remarks"></a>설명

대부분의 함수는 조작자입니다. \<ios>에 선언된 조작자는 [ios_base](../standard-library/ios-base-class.md) 클래스의 해당 인수 개체에 저장된 값을 변경합니다. 다른 조작자는 [basic_istream](../standard-library/basic-istream-class.md) 또는 [basic_ostream](../standard-library/basic-ostream-class.md) 템플릿 클래스 중 하나의 특수화와 같이 이 클래스에서 파생된 형식의 개체에 의해 제어되는 스트림에서 작업을 수행합니다. 예를 들어 [noskipws](../standard-library/ios-functions.md#noskipws)(**str**) 형식 플래그를 지웁니다 `ios_base::skipws` 개체의 `str`, 이러한 형식 중 하나일 수 있습니다.

`ios_base`에서 파생 클래스에 대해 제공되는 특수 삽입 및 추출 작업을 통해 출력 스트림에 삽입하거나 입력 스트림에서 추출하여 조작자를 호출할 수도 있습니다. 예를 들어:

```cpp
istr>> noskipws;
```

[noskipws](../standard-library/ios-functions.md#noskipws)(**istr**)를 호출합니다.

### <a name="typedefs"></a>형식 정의

|형식 이름|설명|
|-|-|
|[ios](../standard-library/ios-typedefs.md#ios)|이전 iostream 라이브러리의 ios 클래스를 지원합니다.|
|[streamoff](../standard-library/ios-typedefs.md#streamoff)|내부 작업을 지원합니다.|
|[streampos](../standard-library/ios-typedefs.md#streampos)|버퍼 포인터 또는 파일 포인터의 현재 위치를 보유합니다.|
|[streamsize](../standard-library/ios-typedefs.md#streamsize)|스트림의 크기를 지정합니다.|
|[wios](../standard-library/ios-typedefs.md#wios)|이전 iostream 라이브러리의 wios 클래스를 지원합니다.|
|[wstreampos](../standard-library/ios-typedefs.md#wstreampos)|버퍼 포인터 또는 파일 포인터의 현재 위치를 보유합니다.|

### <a name="manipulators"></a>조작자

|||
|-|-|
|[boolalpha](../standard-library/ios-functions.md#boolalpha)|[bool](../cpp/bool-cpp.md) 형식의 변수가 스트림에서 **true** 또는 **false**로 표시되도록 지정합니다.|
|[dec](../standard-library/ios-functions.md#dec)|정수 변수가 밑수 10 표기법으로 표시되도록 지정합니다.|
|[defaultfloat](../standard-library/ios-functions.md#ios_defaultfloat)|부동 소수점 값에 기본 표시 형식을 사용하도록 `ios_base` 개체의 플래그를 구성합니다.|
|[fixed](../standard-library/ios-functions.md#fixed)|부동 소수점 숫자가 고정 Decimal 표기법으로 표시되도록 지정합니다.|
|[hex](../standard-library/ios-functions.md#hex)|정수 변수가 밑수 16 표기법으로 표시되도록 지정합니다.|
|[internal](../standard-library/ios-functions.md#internal)|숫자의 부호를 왼쪽에 맞추고 숫자를 오른쪽에 맞춥니다.|
|[left](../standard-library/ios-functions.md#left)|너비가 출력 너비보다 작은 텍스트를 왼쪽에 여백을 두고 스트림 플러시에 표시합니다.|
|[noboolalpha](../standard-library/ios-functions.md#noboolalpha)|[bool](../cpp/bool-cpp.md) 형식의 변수가 스트림에서 1 또는 0으로 표시되도록 지정합니다.|
|[noshowbase](../standard-library/ios-functions.md#noshowbase)|숫자가 표시되는 표기법 밑수 표시를 해제합니다.|
|[noshowpoint](../standard-library/ios-functions.md#noshowpoint)|소수 부분이 0인 부동 소수점 숫자의 정수 부분만 표시합니다.|
|[noshowpos](../standard-library/ios-functions.md#noshowpos)|양수에 명시적으로 부호가 지정되지 않습니다.|
|[noskipws](../standard-library/ios-functions.md#noskipws)|입력 스트림이 공백을 읽습니다.|
|[nounitbuf](../standard-library/ios-functions.md#nounitbuf)|출력이 버퍼링되고 버퍼가 가득 차면 처리됩니다.|
|[nouppercase](../standard-library/ios-functions.md#nouppercase)|16진수 숫자와 과학적 표기법의 지수가 소문자로 표시되도록 지정합니다.|
|[oct](../standard-library/ios-functions.md#oct)|정수 변수가 밑수 8 표기법으로 표시되도록 지정합니다.|
|[right](../standard-library/ios-functions.md#right)|너비가 출력 너비보다 작은 텍스트를 오른쪽에 여백을 두고 스트림 플러시에 표시합니다.|
|[scientific](../standard-library/ios-functions.md#scientific)|과학적 표기법을 사용하여 부동 소수점 숫자를 표시합니다.|
|[showbase](../standard-library/ios-functions.md#showbase)|숫자가 표시되는 표기법 밑수를 표시합니다.|
|[showpoint](../standard-library/ios-functions.md#showpoint)|소수 부분이 0인 경우에도 부동 소수점 숫자의 정수 부분과 소수점 이하 자릿수를 표시합니다.|
|[showpos](../standard-library/ios-functions.md#showpos)|양수에 명시적으로 부호가 지정됩니다.|
|[skipws](../standard-library/ios-functions.md#skipws)|입력 스트림이 공백을 읽지 않습니다.|
|[unitbuf](../standard-library/ios-functions.md#unitbuf)|버퍼가 비어 있지 않으면 출력이 처리됩니다.|
|[uppercase](../standard-library/ios-functions.md#uppercase)|16진수 숫자와 과학적 표기법의 지수가 대문자로 표시되도록 지정합니다.|

### <a name="classes"></a>클래스

|클래스|설명|
|-|-|
|[basic_ios](../standard-library/basic-ios-class.md)|이 템플릿 클래스는 템플릿 매개 변수에 따라 달라지는 입력 스트림(템플릿 클래스 [basic_istream](../standard-library/basic-istream-class.md)) 및 출력 스트림(템플릿 클래스 [basic_ostream](../standard-library/basic-ostream-class.md))에 공통된 저장소 및 멤버 함수를 설명합니다.|
|[fpos](../standard-library/fpos-class.md)|이 템플릿 클래스는 스트림 내의 임의 파일 위치 표시기를 복원하는 데 필요한 모든 정보를 저장할 수 있는 개체를 설명합니다.|
|[ios_base](../standard-library/ios-base-class.md)|이 클래스는 템플릿 매개 변수에 따라 달라지지 않는 입력 및 출력 스트림에 공통된 저장소 및 멤버 함수를 설명합니다.|

## <a name="see-also"></a>참고자료

[헤더 파일 참조](../standard-library/cpp-standard-library-header-files.md)<br/>
[C++ 표준 라이브러리의 스레드 보안](../standard-library/thread-safety-in-the-cpp-standard-library.md)<br/>
[iostream 프로그래밍](../standard-library/iostream-programming.md)<br/>
[iostreams 규칙](../standard-library/iostreams-conventions.md)<br/>
