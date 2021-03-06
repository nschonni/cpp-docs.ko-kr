---
title: 오류 및 예외 처리 (최신 c + +) | Microsoft Docs
ms.custom: ''
ms.date: 09/17/2018
ms.technology:
- cpp-language
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: a6c111d0-24f9-4bbb-997d-3db4569761b7
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 86d041c5ba3770cdd39c03a8ea9b2346e6cefb90
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46100424"
---
# <a name="errors-and-exception-handling-modern-c"></a>오류 및 예외 처리(최신 C++)

대부분의 시나리오에서 최신 c + +의 보고 및 논리 오류 및 런타임 오류를 처리 하는 기본 방법은 예외를 사용 합니다. 스택의 오류를 감지 하는 함수 및 처리 하는 방법을 확인 하기 위한 컨텍스트가 있는 함수 간의 몇 가지 함수 호출 포함 될 수 있습니다 하는 경우 특히 그렇습니다. 예외 호출 스택 정보를 전달 하는 오류를 감지 하는 코드에 대 한 정식, 잘 정의 된 방법을 제공 합니다.

프로그램 오류는 일반적으로 두 가지 범주로 나뉩니다. "네트워크 서비스 사용할 수 없음" 프로그래밍 실수, 예를 들어, "인덱스가 범위를 벗어났습니다" 오류 및 예를 들어, 프로그래머의 제어를 벗어난는 런타임 오류가 발생 하는 논리 오류 오류가 발생 했습니다. C 스타일 프로그래밍 및 COM에서 오류 보고는 관리 되는 오류 코드 또는 특정 함수에 대 한 상태 코드를 나타내는 값을 반환 하거나 호출자에 게 확인 하려면 모든 함수 호출 후 필요에 따라 검색할 수 있는 전역 변수를 설정 하 여 여부 오류가 보고 되었습니다. 예를 들어 COM 프로그래밍 HRESULT 반환 값을 사용 하 여 호출자에 게 오류를 전달 하 고 Win32 API에는 호출 스택에서 보고 된 마지막 오류를 검색 하는 GetLastError 함수가 있습니다. 두 경우 모두,가 호출자가 코드를 인식 하 고 적절 하 게 응답할 수 있습니다. 호출자에 게 오류 코드를 명시적으로 처리 하지 않는 경우 프로그램이 경고 없이 중단 하거나 계속 잘못 된 데이터를 사용 하 여 실행 하 고 잘못 된 결과 생성할 수 있습니다.

다음과 같은 이유로 최신 c + + 예외를 선호 합니다.

- 예외가 호출 코드 오류 조건을 인식 하 고 처리를 강제로 수행 합니다. 처리 되지 않은 예외는 프로그램 실행을 중지 합니다.

- 예외 오류를 처리할 수 있는 호출 스택의 위치로 이동 합니다. 중간 함수는 예외를 전파할 수. 있습니다 다른 레이어와 조정 필요가 없습니다.

- 예외 스택 언 와인딩 메커니즘은 예외가 throw 된 후 잘 정의 된 규칙에 따라 범위의 모든 개체를 제거 합니다.

- 예외 오류를 감지 하는 코드 및 오류를 처리 하는 코드를 분명히 구분할 수 있습니다.

다음 간단한 예제는 throw 및 c + +에서 예외를 catch 하는 데 필요한 구문을 보여 줍니다.

```cpp

#include <stdexcept>
#include <limits>
#include <iostream>

using namespace std;

void MyFunc(int c)
{
    if (c > numeric_limits< char> ::max())
        throw invalid_argument("MyFunc argument too large.");
    //...
}

int main()
{
    try
    {
        MyFunc(256); //cause an exception to throw
    }

    catch (invalid_argument& e)
    {
        cerr << e.what() << endl;
        return -1;
    }
    //...
    return 0;
}

```

C + +에서 예외를 사용 하면 C# 및 Java와 같은 언어에서 비슷합니다. 에 **시도** 예외인 경우 차단 *발생* 됩니다 *포착* 첫 번째 연결 **catch** 블록 형식이 일치는 예외입니다. 실행에서 이동 하는 즉, 합니다 **throw** 문을 합니다 **catch** 문입니다. 사용할 수 있는 catch 블록이 없는 있으면 `std::terminate` 호출 되 고 프로그램이 종료 합니다. C + +에서는 형식일 throw 될 수 있습니다. 하지만 직접 또는 간접적으로 파생 되는 형식을 throw 하는 권장 `std::exception`합니다. 이전 예제에서는 예외 유형 [invalid_argument](../standard-library/invalid-argument-class.md)에서 표준 라이브러리에 정의 된를 [ \<stdexcept >](../standard-library/stdexcept.md) 헤더 파일입니다. C + +는 제공 하지 않으며 필요 하지 않습니다는 **마지막** 블록 예외가 throw 되 면 모든 리소스가 해제 되도록 합니다. Resource는 초기화 (RAII) 관용구 스마트 포인터를 사용 하는 리소스 정리에 필요한 기능을 제공 합니다. 자세한 내용은 [방법: 예외 안전성을 위한 디자인](../cpp/how-to-design-for-exception-safety.md)합니다. C + + 스택 언 와인딩 메커니즘에 대 한 자세한 내용은 [예외 및 스택 해제](../cpp/exceptions-and-stack-unwinding-in-cpp.md)합니다.

## <a name="basic-guidelines"></a>기본 지침

강력한 오류 처리는 모든 프로그래밍 언어에서 까다로운 문제입니다. 예외가 좋은 오류 처리를 지 원하는 여러 기능을 제공 하지만 수에 대 한 모든 작업을 수행할 수 없습니다. 예외 메커니즘의 혜택을 누리려 코드를 디자인할 때 염두에서 예외를 유지 합니다.

- 어설션을 사용 하 여 한 오류가 발생 하지 않습니다 있는지 확인 합니다. 예외를 사용 하 여 예를 들어, 발생할 수 있는 오류에 대 한 공용 함수의 매개 변수에서 입력 유효성 검사 오류를 확인 합니다. 자세한 내용은 섹션을 참조 하세요. **예외 vs. 어설션**합니다.

- 하나 이상의 중간 함수 호출에서 오류를 처리 하는 코드 오류를 감지 하는 코드에서 분리 될 수 있을 때 예외를 사용 합니다. 밀접 하 게 검색 하는 코드에 코드 오류를 처리 하는 경우 성능이 중요 한 루프에서 오류 코드를 대신 사용할지 여부를 고려 합니다.

- Throw 하거나 예외를 전파할 수 있는 모든 함수에 대 한 세 가지 예외 보증 중 하나를 제공 합니다: 강력한 보장, 기본 보장 또는 nothrow (noexcept) 보장 합니다. 자세한 내용은 [방법: 예외 안전성을 위한 디자인](../cpp/how-to-design-for-exception-safety.md)합니다.

- 값으로 예외를 throw, 참조로 catch 합니다. 처리할 수 없는 catch 하지 마십시오.

- C++11에서 사용 되지 않는 예외 사양을 사용 하지 마세요. 자세한 내용은 섹션을 참조 하세요 **예외 사양 및 noexcept**합니다.

- 표준 라이브러리 예외 형식을 사용 하 여 적용 될 경우. 사용자 지정 예외 형식을 파생 합니다 [exception 클래스](../standard-library/exception-class.md) 계층입니다.

- 소멸자에서 이스케이프 처리 하거나 메모리 할당 해제 함수에 대 한 예외를 허용 하지 마십시오.

## <a name="exceptions-and-performance"></a>예외 및 성능

예외 메커니즘은 예외가 throw 되지 않습니다 하는 경우 비용은 최소 성능을 있습니다. 예외가 throw 되 면 비용 스택 통과 및 해제은 함수 호출 비용과 거의 비슷합니다. 후 호출 스택을 추적 하는 데 필요한 추가 데이터 구조를 **시도** 블록을 입력 하 고 추가 지침 예외가 발생 하는 경우 스택을 해제 하는 데 필요 합니다. 그러나 대부분의 시나리오에서 성능 및 메모리 사용 공간 비용이 크지 않습니다. 성능에 예외가 미치는 부정적인 영향은 매우 메모리 제약이 심한 시스템 에서만 중요 한 것으로 가능성이 또는에서 성능이 중요 한 루프 오류가 정기적으로 발생 하기 쉽습니다. 않았고 처리 하는 코드는 밀접 하 게 보고 하는 코드입니다. 어떤 경우 든, 프로 파일링 하 고 측정 하지 않고 예외의 실제 비용을 알 수 없는 합니다. 드문 경우에도 비용을 중요 한 경우에 향상 된 정확성, 쉬워진 유지 관리 및 잘 디자인 된 예외 정책에 의해 제공 되는 다른 장점에 대해 평가 수 있습니다.

## <a name="exceptions-vs-assertions"></a>예외 및 어셜션 비교

예외 어설션 프로그램에서 런타임 오류를 감지 하는 것에 대 한 두 가지 메커니즘이 있습니다. 어설션을 사용 하 여 개발에 모든 코드가 정확할 경우 true 않아야 하는 동안 조건을 테스트 합니다. 오류 수정에 코드에서 무언가 나타내기 때문에 예외를 사용 하 여 이러한 오류를 처리에 포인터가 없는 프로그램에서 런타임 시 복구 해야 하는 조건을 나타내지는 합니다. Assert; 디버거에서 프로그램 상태를 검사할 수 있도록 문에서 실행을 중지 예외는 첫 번째 적절 한 catch 처리기에서 실행을 계속합니다. 예외를 사용 하 여도 올바르면 코드, 예를 들어 "파일 not found" 또는 "메모리 부족 합니다." 실행 시 발생할 수 있는 오류 조건 확인 방금 복구 로그에 메시지를 출력 한 프로그램을 종료 하는 경우에 이러한 상황에서 복구 하려는 경우. 항상 예외를 사용 하 여 public 함수에 대 한 인수를 확인 합니다. 함수를 오류가 없는 경우에 사용자를 전달할 수 있는 인수를 완전히 제어가 없을 수 있습니다.

## <a name="c-exceptions-versus-windows-seh-exceptions"></a>Windows SEH 예외와 c + + 예외

C 및 c + + 프로그램에는 구조적된 예외 처리 (SEH) 메커니즘이 Windows 운영 체제에서 사용할 수 있습니다. SEH의 개념 유사 c + + 예외를 제외 하 고 SEH를 사용 합니다 **__try**를 **__except**, 및 **__finally** 대신 생성 **시도** 하 고 **catch**합니다. Visual c + +, c + + 예외는 SEH에 대해 구현 됩니다. 그러나 c + + 코드를 작성할 때 c + + 예외 구문을 사용 합니다.

SEH에 대 한 자세한 내용은 참조 하세요. [구조적 예외 처리 (C/c + +)](../cpp/structured-exception-handling-c-cpp.md)합니다.

## <a name="exception-specifications-and-noexcept"></a>예외 사양 및 noexcept

예외 사양은 함수가 throw 할 수 있는 예외를 지정 하는 방법으로 c + +에 도입 되었습니다. 그러나 예외 사양 실제로 문제가 입증 및 c+11 초안 표준에서 사용 되지 않습니다. 제외 하 고 예외 사양을 사용 하지 않는 것이 좋습니다 `throw()`, 함수 예외가 이스케이프를 허용 하는지 나타냅니다. 형식의 예외 사양을 사용 해야 하는 경우 `throw(` *형식을*`)`, Visual c + + 표준에서 다양 한 방식으로 분리 하는 알고 있어야 합니다. 자세한 내용은 [예외 사양 (throw)](../cpp/exception-specifications-throw-cpp.md)합니다. 합니다 `noexcept` 지정자를 안으로 c++11에서 도입 된 `throw()`합니다.

## <a name="see-also"></a>참고자료

[방법: 예외 코드와 예외가 아닌 코드 간 인터페이스](../cpp/how-to-interface-between-exceptional-and-non-exceptional-code.md)<br/>
[C++의 진화](../cpp/welcome-back-to-cpp-modern-cpp.md)<br/>
[C++ 언어 참조](../cpp/cpp-language-reference.md)<br/>
[C++ 표준 라이브러리](../standard-library/cpp-standard-library-reference.md)