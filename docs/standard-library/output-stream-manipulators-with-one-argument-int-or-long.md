---
title: 하나의 인수를 포함하는 출력 스트림 조작자(int 또는 long) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- output streams, int or long argument manipulators
ms.assetid: 338f3164-b5e2-4c5a-a605-7d9dc3629ca1
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f569b064d2ee5de5bd1aa39c9d443c8a49ca2677
ms.sourcegitcommit: 3614b52b28c24f70d90b20d781d548ef74ef7082
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/11/2018
ms.locfileid: "38961853"
---
# <a name="output-stream-manipulators-with-one-argument-int-or-long"></a>하나의 인수를 포함하는 출력 스트림 조작자(int 또는 long)

iostream 클래스 라이브러리는 매개 변수가 있는 조작자를 만들기 위한 매크로 집합을 제공합니다. 단일 조작자 **int** 하거나 **긴** 인수는 특별 한 경우. 단일을 허용 하는 출력 스트림 조작자를 만들려면 **int** 또는 **긴** 인수 (같은 `setw`)에서 정의 되는 _Smanip 매크로 사용 해야 \<iomanip >. 이 예제에서는 지정된 수의 공백을 스트림에 삽입하는 `fillblank` 조작자를 정의합니다.

## <a name="example"></a>예

```cpp
// output_stream_manip.cpp
// compile with: /GR /EHsc
#include <iostream>
#include <iomanip>
using namespace std;

void fb( ios_base& os, int l )
{
   ostream *pos = dynamic_cast<ostream*>(&os);
   if (pos)
   {
      for( int i=0; i < l; i++ )
      (*pos) << ' ';
   };
}

_Smanip<int>
   __cdecl fillblank(int no)
   {
   return (_Smanip<int>(&fb, no));
   }

int main( )
{
   cout << "10 blanks follow" << fillblank( 10 ) << ".\n";
}
```

## <a name="see-also"></a>참고자료

[인수 포함 사용자 지정 조작자](../standard-library/custom-manipulators-with-arguments.md)<br/>
