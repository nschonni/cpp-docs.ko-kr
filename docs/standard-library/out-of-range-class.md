---
title: out_of_range 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
f1_keywords:
- stdexcept/std::out_of_range
dev_langs:
- C++
helpviewer_keywords:
- out_of_range class
ms.assetid: d0e14dc0-065e-4666-9ac9-51e52223c503
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: aeb29538dc73ddbefe2ee443cf7f8bfa660eb528
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/08/2018
ms.locfileid: "33852867"
---
# <a name="outofrange-class"></a>out_of_range 클래스

이 클래스는 유효 범위를 벗어난 인수를 보고하기 위해 발생하는 모든 예외에 대한 기본 클래스로 사용됩니다.

## <a name="syntax"></a>구문

```cpp
class out_of_range : public logic_error {
public:
    explicit out_of_range(const string& message);

    explicit out_of_range(const char *message);

};
```

## <a name="remarks"></a>설명

[what](../standard-library/exception-class.md)에서 반환된 값은 **message**`.`[data](../standard-library/basic-string-class.md#data)의 복사본입니다.

## <a name="example"></a>예제

```cpp
// out_of_range.cpp
// compile with: /EHsc
#include <string>
#include <iostream>

using namespace std;

int main() {
// out_of_range
   try {
      string str( "Micro" );
      string rstr( "soft" );
      str.append( rstr, 5, 3 );
      cout << str << endl;
   }
   catch ( exception &e ) {
      cerr << "Caught: " << e.what( ) << endl;
   };
}
```

## <a name="output"></a>출력

```cpp
Caught: invalid string position
```

## <a name="requirements"></a>요구 사항

**헤더:** \<stdexcept>

**네임스페이스:** std

## <a name="see-also"></a>참고자료

[logic_error 클래스](../standard-library/logic-error-class.md)<br/>
[C++ 표준 라이브러리의 스레드 보안](../standard-library/thread-safety-in-the-cpp-standard-library.md)<br/>
