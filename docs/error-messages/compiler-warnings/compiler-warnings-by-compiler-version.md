---
title: 컴파일러 버전별 컴파일러 경고 | Microsoft Docs
ms.custom: ''
ms.date: 10/24/2018
ms.technology:
- devlang-cpp
ms.topic: error-reference
dev_langs:
- C++
helpviewer_keywords:
- warnings, by compiler version
- cl.exe compiler, setting warning options
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1c4d815ba1036a03042992d2715e49bbd8f74a28
ms.sourcegitcommit: c045c3a7e9f2c7e3e0de5b7f9513e41d8b6d19b2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/24/2018
ms.locfileid: "49990388"
---
# <a name="compiler-warnings-by-compiler-version"></a>컴파일러 버전별 컴파일러 경고

컴파일러를 사용 하 여 지정 된 버전 이후 도입 된 경고 표시 하지 않을 수는 [/Wv](../../build/reference/compiler-option-warning-level.md) 컴파일러 옵션입니다. 새 도구 집합 버전을 소개 하 고 새 경고를 일시적으로 표시 하지 않을 때 빌드 프로세스를 관리 하기 위한 유용 합니다. 이 옵션에서 새 오류 메시지를 숨기지 않습니다. 모든 새 경고를 억제 하지 않는 것이 좋습니다 영구적으로! 항상 가장 일반적인 경고 수준에서 컴파일하는 것이 좋습니다 __/w4__, 및 제거 합니다 __/Wv__ 빌드에서 가능한 한 빨리 옵션.

이러한 버전의 컴파일러에는 새로운 경고가 추가 되었습니다.

| 제품 | 컴파일러 버전 번호 |
|-|-|
| Visual C++ 2002 | 13.00.9466 |
| Visual C++ 2003 | 13.10.3077 |
| Visual C++ 2005 | 14.00.50727.762 |
| Visual C++ 2008 | 15.00.21022.08 |
| Visual C++ 2010 | 16.00.40219.01 |
| Visual C++ 2012 | 17.00.51106.1 |
| Visual C++ 2013 | 18.00.21005.1 |
| Visual C++ 2015 RTM | 19.00.23026.0 |
| Visual c + + 2015 업데이트 1 | 19.00.23506.0 |
| Visual c + + 2015 업데이트 2 | 19.00.23918.0 |
| Visual c + + 2015 업데이트 3 | 19.00.24215.1 |
| Visual c + + 2017 RTM | 19.10.25017.0 |
| Visual c + + 2017 버전 15.3 | 19.11.25506.0 |
| Visual c + + 2017 버전 15.5 | 19.12.25830.0 |
| Visual c + + 2017 버전 15.6 | 19.13.26128.0 |
| Visual c + + 2017 버전 15.7 | 19.14.26428.0 |
| Visual c + + 2017 버전 15.8 | 19.15.26726.0 |

만 주 번호, 주 및 부 번호 또는 주, 부를 지정할 수 있으며 빌드 번호를 합니다 __/Wv__ 옵션입니다. 컴파일러는 지정된 된 수로 시작 하는 버전과 일치 하는 모든 경고를 보고 하 고 지정된 된 숫자 보다 큰 버전에 대 한 모든 경고를 표시 하지 않습니다. 예를 들어 __/Wv:17__ 이전의 모든 버전의 Visual Studio 2012에서 도입 된 모든 경고를 보고 하 고 이상 Visual Studio 2013 (버전 18)에서 모든 컴파일러에서 도입 된 모든 경고를 표시 하지 않습니다. Visual Studio 2015에서 도입 된 경고를 표시 하지 않으려면 2를 업데이트 하 고 나중에 사용할 수 있습니다 __/Wv:19.00.23506__합니다. 사용 하 여 __/Wv:19.11__ 보고할 모든 경고는 Visual Studio 2017 버전 15.5 이전 Visual Studio의 모든 버전에서 도입 되었지만 Visual Studio 2017 버전 15.5 이상에서 도입 된 경고를 표시 하지 않습니다.

다음 섹션에서는 사용 하 여 표시 하지 않을 수 있는 Visual c + +의 각 버전에서 도입 된 경고를 나열 합니다 __/Wv__ 컴파일러 옵션입니다. 합니다 __/Wv__ 옵션은 지정 된 버전의 컴파일러는 나열 되지 않은 경고 표시 하지 않을 수 있습니다.

## <a name="warnings-introduced-in-visual-c-2017-version-158-compiler-version-1915267260"></a>Visual c + + 2017 버전 15.8 (컴파일러 버전 19.15.26726.0)에서 도입 된 경고

이러한 경고 및 이후 버전에서 모든 경고는 컴파일러 옵션을 사용 하 여 억제 __/Wv:19.14__합니다.

|||
|-|-|
C5046|'*함수*': 정의 되지 않은 내부 링크가 있는 형식을 포함 하는 기호|

## <a name="warnings-introduced-in-visual-c-2017-version-157-compiler-version-1914264280"></a>Visual c + + 2017 버전 15.7 (컴파일러 버전 19.14.26428.0)에서 도입 된 경고

이러한 경고 및 이후 버전에서 모든 경고는 컴파일러 옵션을 사용 하 여 억제 __/Wv:19.13__합니다.

|||
|-|-|
C4642|'*문제*': 제네릭 매개 변수에 대 한 제약 조건을 가져올 수 없습니다 '*매개 변수*'
C5045|컴파일러는 메모리 /Qspectre 스위치 하는 경우 지정 된 로드에 대 한 스펙터 완화를 삽입

## <a name="warnings-introduced-in-visual-c-2017-version-156-compiler-version-1913261280"></a>Visual c + + 2017 버전 15.6 (컴파일러 버전 19.13.26128.0)에서 도입 된 경고

이러한 경고 및 이후 버전에서 모든 경고는 컴파일러 옵션을 사용 하 여 억제 __/Wv:19.12__합니다.

|||
|-|-|
C5044|명령줄 옵션에 인수가 *옵션* 경로 가리키는 '*경로*' 존재 하지 않는

## <a name="warnings-introduced-in-visual-c-2017-version-155-compiler-version-1912258300"></a>Visual c + + 2017 버전 15.5 (컴파일러 버전 19.12.25830.0)에서 도입 된 경고

이러한 경고 및 이후 버전에서 모든 경고는 컴파일러 옵션을 사용 하 여 억제 __/Wv:19.11__합니다.

|||
|-|-|
C4843|'*type1*': 배열 또는 함수 형식에 대 한 참조의 예외 처리기를 연결할 수 없는 경우, 사용 하 여 '*type2*' 대신
C4844|' 모듈을 내보내는 *module_name*;' 모듈 인터페이스를 선언 하기 위한 기본 구문은 이제
C5039|'*함수*':-ehc extern C 함수에 대 한 포인터 또는 참조 잠재적인 throw 함수에 전달 합니다. 이 함수가 예외를 throw 하는 경우 정의 되지 않은 동작이 발생할 수 있습니다.
C5040|및 이전 버전, c++14에만 동적 예외 사양 유효합니다. noexcept(false)로 처리 하는 방법
C5041|'*정의*': constexpr 정적 데이터 멤버에 대 한 아웃오브 라인 정의 필요 하지 않으며 c++17에서 사용 되지 않습니다
C5042|'*선언*': 블록 범위의 함수 선언은 일 수 없습니다. 지정 된 'inline' 표준 c + +에서 'inline' 지정자를 제거 합니다.
C5043|'*사양*': 예외 사양이 이전 선언과 일치 하지 않습니다

## <a name="warnings-introduced-in-visual-c-2017-version-153-compiler-version-1911255060"></a>Visual c + + 2017 버전 15.3 (컴파일러 버전 19.11.25506.0)에서 도입 된 경고

이러한 경고 및 이후 버전에서 모든 경고는 컴파일러 옵션을 사용 하 여 억제 __/Wv:19.10__합니다.

|||
|-|-|
C4597|정의 되지 않은 동작: *설명*
C4604|'*형식*': 네이티브 및 관리 되는 경계 값으로 인수를 전달 하려면 유효한 복사 생성자가 필요 합니다. 그렇지 않으면 런타임 동작이 정의 되지 않습니다.
C4749|조건부로 지원 됨: *설명*
C4768|링크 사양 앞의 __declspec 특성은 무시 됩니다.
C4834|'nodiscard' 특성이 포함 된 함수의 반환 값
C4841|비표준 확장이 사용 됨: *확장*
C4842|다중 상속을 사용 하는 형식에 적용 된 'offsetof' 결과 컴파일러 릴리스 간에 일관 되도록 보장 되지 않습니다.
C4869|'nodiscard' 클래스, 열거형 및 void가 아닌 반환 형식이 있는 함수에만 적용 될 수 있습니다.
C5033|'*저장소 클래스*'는 더 이상 지원 되는 저장소 클래스
C5034|내장 함수의 사용 하 여 '*내장*' 함수 *함수* 게스트 코드로 컴파일됩니다
C5035|기능을 사용 하 여 '*기능*' 함수 *함수* 게스트 코드로 컴파일됩니다
C5036|/ hybrid:x86arm64를 사용 하 여 컴파일할 때의 varargs 함수 포인터 변환이 있습니다. '*type1*'to'*type2*'
C5037|'*멤버 함수*': 클래스 템플릿의 멤버는 아웃오브 라인 정의 기본 인수를 사용할 수 없습니다
C5038|데이터 멤버 '*member1*'다음에 초기화 됩니다 데이터 멤버'*member2*'

## <a name="warnings-introduced-in-visual-c-2017-rtm-compiler-version-1910250170"></a>Visual c + + 2017 RTM (컴파일러 버전 19.10.25017.0)에서 도입 된 경고

이러한 경고 및 이후 버전에서 모든 경고는 컴파일러 옵션을 사용 하 여 억제 __/Wv:19.00__합니다.

|||
|-|-|
C4468|'fallthrough': 특성 뒤에 야 case 레이블 또는 default 레이블이
C4698|'*기능*' 제거 나중에 업데이트 하거나 평가 목적 으로만 제공 되며 변경 될 수 있습니다.
C4839|클래스의 비표준 사용*클래스*' variadic 함수에 인수로 서
C4840|클래스의 비 휴대용 활용*클래스*' variadic 함수에 인수로 서

## <a name="warnings-introduced-in-visual-c-2015-update-3-compiler-version-1900242151"></a>Visual c + + 2015 업데이트 3 (컴파일러 버전 19.00.24215.1)에 도입 된 경고

이러한 경고 및 이후 버전에서 모든 경고는 컴파일러 옵션을 사용 하 여 억제 __/Wv:19.00.23918__합니다.

|||
|-|-|
C4467|ATL 특성의 사용은 사용 되지 않습니다.
C4596|'*이름을*': 멤버 선언의 정규화 된 이름이 잘못 되었습니다.
C4598|' #include \< *헤더*\>': 헤더 번호 *번호* 에 *원본* 일치 하지 않습니다 *원본* 이때 위치
C4599|'*인수*': *원본* 인수 번호 *번호* 맞지 *원본*

## <a name="warnings-introduced-in-visual-c-2015-update-2-compiler-version-1900239180"></a>Visual c + + 2015 업데이트 2 (컴파일러 버전 19.00.23918.0)에 도입 된 경고

이러한 경고 및 이후 버전에서 모든 경고는 컴파일러 옵션을 사용 하 여 억제 __/Wv:19.00.23506__합니다.

|||
|-|-|
C4466|코 루틴 힙 생략을 수행할 수 없습니다.
C4595|'*클래스*': 멤버가 아닌 연산자 new 또는 delete 함수 있습니다 인라인으로 선언할 수 없습니다
C4828|파일 오프셋 0에서 시작 문자가 x*값* 현재 소스 문자 집합에서 사용할 수 없는 (codepage *수*).
C4868|컴파일러는 중괄호로 묶인된 이니셜라이저 목록에서 왼쪽에서 오른쪽 계산 순서를 적용할 수 없습니다.

## <a name="warnings-introduced-in-visual-c-2015-update-1-compiler-version-1900235060"></a>Visual c + + 2015 업데이트 1 (컴파일러 버전 19.00.23506.0)에 도입 된 경고

이러한 경고 및 이후 버전에서 모든 경고는 컴파일러 옵션을 사용 하 여 억제 __/Wv:19.00.23026__합니다.

|||
|-|-|
C4426|헤더를 포함 한 후 변경 된 최적화 플래그 #pragma optimize () 때문일 수 있습니다.
C4654|앞에 배치 하는 코드에는 미리 컴파일된 헤더 포함 줄은 무시 됩니다. 미리 컴파일된 헤더에 코드를 추가 합니다.
C5031|#pragma warning (pop): 다른 파일에서 푸시된 경고 상태 팝업 불일치 가능성
C5032|해당 없음 #pragma warning (pop이) 사용 하 여 #pragma warning (push)를 검색합니다.

## <a name="warnings-introduced-in-visual-c-2015-rtm-compiler-version-1900230260"></a>Visual c + + 2015 RTM (컴파일러 버전 19.00.23026.0)에서 도입 된 경고

이러한 경고 및 이후 버전에서 모든 경고는 컴파일러 옵션을 사용 하 여 억제 __/wv:18__합니다.

|||
|-|-|
C4427|'*오류*': 상수 분할, 정의 되지 않은 동작의에서 오버플로
C4438|'*형식*': /await 안전 하 게 호출할 수 없습니다: clrcompat 모드입니다. 경우 '*형식*'에 대 한 호출은 CLR 손상에서 될 수 있습니다
C4455|' 연산자 *이름을*': 밑줄로 시작 하지 않는 리터럴 접미사 식별자는 예약 되어 있습니다.
C4456|선언의 '*이름을*' 이전 로컬 선언을 숨깁니다.
C4457|선언의 '*이름을*' 숨깁니다 함수 매개 변수
C4458|선언의 '*이름을*' 클래스 멤버를 숨깁니다
C4459|선언의 '*이름을*' 전역 선언을 숨깁니다.
C4462|'*형식*': 형식의 GUID를 확인할 수 없습니다. 프로그램은 런타임에 실패할 수 있습니다.
C4463|오버플로. 할당 *값* 의 값만 포함할 수 있는 비트 필드에 *값* 에 *값*
C4473|'*함수*': 서식 문자열에 전달 된 인수가 부족 합니다.
C4474|'*함수*': 서식 문자열에 전달 된 인수가 너무 많습니다.
C4475|'*함수*': 길이 한정자 '*한정자*'형식 필드 문자를 사용할 수 없습니다'*문자*'의 형식 지정자
C4476|'*함수*': 알 수 없는 형식 필드 문자 '*문자*'의 형식 지정자
C4477|'*함수*': 서식 문자열 '*문자열*'형식의 인수가 필요 합니다.'*형식*', 하지만 variadic 인수 *번호* 형식이 '*형식*'
C4478|'*함수*': 동일한 서식 문자열의 위치 및 비 위치 자리 표시자를 혼합할 수 없습니다
C4494|'*형식*': 포인터 또는 참조 하지는 함수 반환 형식 때문에 (allocator)를 무시 합니다.
C4495|비표준 확장이 사용 '_': 명시적 기본 클래스 이름으로 대체
C4496|'for each' 비표준 확장이 사용: ranged-for 문으로 대체
C4497|비표준 확장이 사용 되는 'sealed': '최종'으로 바꾸기
C4498|비표준 확장이 사용 됨: '*확장*'
C4499|'*특수화*': 명시적 특수화 (무시 됨) 저장소 클래스를 가질 수 없습니다.
C4576|괄호로 묶은 이니셜라이저 목록 뒤에 형식은 비표준 명시적 형식 변환 구문
C4577|' noexcept' 처리 모드를 지정 합니다; 예외가 사용 예외 시 종료가 보장 되지 않습니다. /EHsc를 지정 합니다.
C4578|'abs': 변환에서 '*형식*'to'*유형*', 데이터 손실 될 수 있습니다 (호출 하려고 했습니까 '*이름*' 또는 #include \<cmath >?)
C4582|'*형식*': 생성자가 암시적으로 호출 되지 않습니다
C4583|'*형식*': 소멸자가 암시적으로 호출 되지 않습니다
C4587|'*형식*': 동작 변경: 생성자가 더 이상 암시적으로 호출
C4588|'*형식*': 동작 변경: 소멸자가 더 이상 암시적으로 호출 되 고 없습니다.
C4589|추상 클래스의 생성자*형식*'가상 기본 클래스에 대 한 이니셜라이저가 무시'*형식*'
C4591|'constexpr' 호출 깊이 제한인 *번호* 초과 (/ constexpr:depth\<번호 >)
C4592|'*형식*': 기호는 동적으로 됩니다 (구현 제한)를 초기화 합니다.
C4593|'*형식*': 'constexpr' 호출 실행 단계 제한 *값* 초과; /constexpr:를 사용 하 여\<번호 >도를 늘리려면
C4647|동작 변경: __is_pod (*형식*) 이전 버전에 다른 값
C4648|표준 특성 'carries_dependency'는 무시 됩니다.
C4649|이 컨텍스트에서 특성은 무시 됩니다.
C4753|포인터의 범위를 찾을 수 없습니다. 무시 MPX 내장 함수
C4771|범위는 간단한 포인터를 사용 하 여 만들어야 무시 MPX 내장 함수
C4774|'*설명을*': 서식 문자열 인수에 예상 *번호* 이 문자열 리터럴
C4775|비표준 확장이 서식 문자열에 사용 되는 '*문자열*'함수의'*함수*'
C4776|' %*문자*'함수의 서식 문자열에서 허용 되지 않는'*함수*'
C4777|'*설명을*': 서식 문자열 '*문자열*'형식의 인수가 필요 합니다.'*형식*', 하지만 variadic 인수 *번호* 형식이 '*형식*'
C4778|'*설명을*': 서식 문자열을 종결 되지 않았습니다 '*문자열*'
C4838|변환에서 '*형식*'to'*형식*' 축소 변환이 필요 합니다.
C5022|'*형식*': 이동 생성자가 여러 개 지정
C5023|'*형식*': 지정 된 여러 명의 이동 할당 연산자
C5024|'*선언*': 이동 생성자가 암시적으로 삭제 된 것으로 정의 됩니다
C5025|'*선언*': 이동 대입 연산자가 삭제 된 것으로 암시적으로 정의 됩니다
C5026|'*형식*': 이동 생성자가 암시적으로 삭제 된 것으로 정의 됩니다
C5027|'*형식*': 이동 대입 연산자가 삭제 된 것으로 암시적으로 정의 됩니다
C5028|'*이름을*': 이전 선언에 지정 된 맞춤 (*번호*) 정의에 지정 되지 않은
C5029|비표준 확장이 사용 됨: 변수, 데이터 멤버 및 태그 형식에만에 c + +의 맞춤 특성 적용
C5030|특성 '*특성*' 인식할 수 없습니다

## <a name="warnings-introduced-in-visual-c-2013-compiler-version-1800210051"></a>Visual c + + 2013 (컴파일러 버전 18.00.21005.1)에 도입 된 경고

이러한 경고 및 이후 버전에서 모든 경고는 컴파일러 옵션을 사용 하 여 억제 __/Wv:17__합니다.

|||
|-|-|
C4301|'*형식*': 재정의 가상 함수에서 다른만 '*선언*' const/volatile 한정자
C4316|'*형식*': 힙에 할당 된 개체를 정렬할 수 있습니다 *수*
C4380|'*형식*': 기본 생성자를 사용 되지 않을 수 없습니다.
C4388|'*토큰*': signed 또는 unsigned 일치 하지 않습니다.
C4423|'std:: bad_alloc': 클래스에 의해 포착 됩니다 ('*형식*') 줄에 *수*
C4424|catch에 대 한 '*형식*'앞 에'*유형*' 줄에 *번호*; 예기치 않은 동작 'std:: bad_alloc' throw 되는 경우 발생할 수 있습니다
C4425|SAL 주석에 '...'에 적용할 수 없습니다.
C4464|include에 상대 경로 '..'
C4575|와 호환 되지 않는 ' __vectorcall'는 ' / clr' 옵션: '__stdcall'으로 변환
C4609|'*형식*'기본 인터페이스에서 파생 됩니다'*유형*'type' on*형식*'. 에 대 한 다른 기본 인터페이스를 사용 하 여 '*형식*', 또는 기본/파생 관계를 중단 합니다.
C4754|비교에 산술 연산의 변환 규칙 *설명을*(*번호*) 분기 하나를 실행할 수 없음을 의미 합니다. Cast '*형식*'to'*유형*' (또는 비슷한 형식의 *번호* 바이트)입니다.
C4755|비교에 산술 연산의 변환 규칙 *설명을*(*번호*) 인라인된 함수에서 분기 하나를 실행할 수 없음을 의미 합니다. Cast '*형식*'to'*유형*' (또는 비슷한 형식의 *번호* 바이트)입니다.
C4767|섹션 이름 '*이름을*' 8 자 보다 긴 및 링커에서 잘립니다
C4770|부분적으로 열거형 유효성 검사 '*이름을*' 인덱스로 사용
C4827|공용 'ToString' 메서드 매개 변수가 0 가상으로 표시 되어야 하 고 재정의
C4882|concurrency:: parallel_for_each에 비 const 호출 연산자를 사용 하 여 함수를 전달할 사용 되지 않음
C4973|'*형식*': 사용 되지 않는 것으로 표시
C4974|'*형식*': 사용 되지 않는 것으로 표시
C4981|Warbird: 함수 '*선언*' 아니라 __forceinline로 표시 인라인 예외 의미 체계를 포함 하기 때문에
C4990|Warbird: *메시지*
C4991|Warbird: 함수 '*선언*' 아니라 __forceinline로 표시 인라인 부모 보다 높으므로 인라인이 보호 수준 이므로
C4992|Warbird: 함수 '*선언*' 아니라 __forceinline로 표시 인라인 보호할 수 없는 인라인 어셈블리가 포함 되어 있으므로

## <a name="warnings-introduced-in-visual-c-2012-compiler-version-1700511061"></a>Visual c + + 2012 (컴파일러 버전 17.00.51106.1)에서 도입 된 경고

이러한 경고 및 이후 버전에서 모든 경고는 컴파일러 옵션을 사용 하 여 억제 __/Wv:16__합니다.

|||
|-|-|
C4330|특성 '*특성*'for '섹션*섹션*' 무시
C4415|duplicate __declspec(code_seg('*name*'))
C4416|code_seg 빈 문자열이 포함 됩니다: 무시
C4417|명시적 템플릿 인스턴스화에 code_seg를 사용할 수 없습니다: 무시
C4418|code_seg enum에서 무시
C4419|'*이름을*'private ref 클래스에 적용 될 때 효과가 있습니다'*형식*'.
C4435|'*형식*': 가상 기본으로 인해/vd2의 개체 레이아웃이 변경 됩니다 '*형식*'
C4436|가상 기본 사이의 dynamic_cast가 '*형식*'to'*형식*' 생성자 또는 소멸자가 부분적으로 생성 된 개체를 사용 하 여 실패할 수 있습니다
C4437|가상 기본 사이의 dynamic_cast가 '*형식*'to'*형식*' 일부 컨텍스트에서 실패할 수 있습니다
C4443|pragma 매개 변수는 '0', '1' 또는 '2'
C4446|'*형식*': 멤버를 매핑할 수 없습니다 '*이름*'이 형식으로 형식 이름으로 충돌 합니다. 메서드 이름이로 바뀌었습니다. '*이름을*'
C4447|스레딩 모델이 없는 'main' 시그니처입니다. 사용 하는 것이 좋습니다. ' int main (platform:: array\<platform:: string ^ > ^ args)'.
C4448|'*형식*' 메타 데이터에 지정 된 기본 인터페이스가 없습니다. 선택 합니다. '*형식*'에 런타임에 실패할 수 있습니다.
C4449|'*형식*'에서는 unsealed 형식이 '[WebHostHidden]'으로 표시 됨
C4450|'*형식*'로 표시 되어야 합니다 '[WebHostHidden]'에서 파생 되므로'*형식*'
C4451|'*형식*': ref 클래스의 사용 현황*형식*' 내부 컨텍스트 간에 개체의 잘못 된 마샬링이 컨텍스트에서 발생할 수 있습니다
C4452|'*형식*': public 형식은 전역 범위에 있을 수 없습니다. 출력.winmd 파일 이름의 자식인 네임 스페이스에 있어야 합니다.
C4453|'*형식*': '[WebHostHidden]' 형식이 아닌 public 형식의 게시 된 표면에 사용할 수 없습니다는 '[WebHostHidden]'
C4454|'*형식*' [defaultoverload] 지정 하지 않고 포함 된 입력된 매개 변수의 수 이상으로 오버 로드 합니다. 선택 '*선언*' 기본 오버 로드로
C4471|'*이름을*': 범위가 지정 되지 않은 열거형의 정방향 선언에는 기본 형식 (int로 가정) 있어야 합니다.
C4472|'*이름을*'가 네이티브 열거형: 관리 되는 WinRT 열거형을 선언 하려면 액세스 지정자 (전용/공용)를 추가 합니다.
C4492|'*형식*': 일치 기본 ref 클래스 메서드 '*형식*', 'override' 표시 되지 않지만
C4493|삭제 식은 효과가 없습니다 소멸자 '*형식*' 'public' 액세스 가능성이 없는
C4585|'*형식*': 'public ref class' sealed 여야 하거나 또는 기존의에서 파생 되는 WinRT 클래스 봉인 되지 않은
C4586|'*형식*': public 형식은 'Windows' 라는 최상위 네임 스페이스에서 선언할 수 없습니다
C4695|#pragma execution_character_set: '*인수*' 지원 되는 인수가 아닙니다: 현재 ' u t F-8'는
C4703|잠재적으로 초기화 되지 않은 로컬 포인터 변수 '*이름을*' 사용
C4728|/Yl-옵션이 PCH 참조 필요 하기 때문에 무시 됩니다.
C4745|volatile 액세스 '*이름을*' 크기로 인해 적용할 수 없는
C4746|volatile 액세스 '*이름을*' 하려면 /volatile:\<iso\|ms > __iso_volatile_load/store 내장 함수를 사용해 설정 합니다.
C4872|concurrency:: parallel_for_each에 대해 호출 그래프를 컴파일하는 경우를 검색 하는 0으로 부동 소수점 나누기: '*설명을*'
C4880|캐스팅 '*형식*'to'*형식*': amp 제한 함수에 정의 되지 않은 동작이 발생할 포인터 또는 참조에서 상수 성 캐스팅
C4881|생성자 및/또는 소멸자가 호출 되지 것입니다 tile_static 변수 '*형식*'
C4966|'*설명을*'에 지원 되지 않는 세그먼트 이름으로 무시 하는 주석 __code_seg 주석이 있습니다.
C4988|'*형식*': 변수가 클래스/함수 범위 외부 선언
C4989|'*설명을*': 형식은 정의가 충돌 합니다.

## <a name="warnings-introduced-in-visual-c-2010-compiler-version-16004021901"></a>Visual c + + 2010 (컴파일러 버전 16.00.40219.01)에서 도입 된 경고

이러한 경고 및 이후 버전에서 모든 경고는 컴파일러 옵션을 사용 하 여 억제 __/Wv:15__합니다.

|||
|-|-|
C4352|'*이름을*': 이미 정의 된 내장 함수
C4573|사용 '*형식*' 컴파일러 'this'이 하지만 캡처에 필요한 현재 기본 캡처 모드를 허용 하지 않습니다
C4574|'*이름을*'0 '으로 정의 된': 사용 하려고 했습니까 ' #if *이름*'?
C4689|'*문자*': #pragma detect_mismatch에 지원 되지 않는 문자; #pragma 무시
C4751|intel (r) 스트리밍 SIMD 확장 인라인 ASM에 포함 된 /arch AVX 플래그 적용 되지 않습니다.
C4752|intel (r) Advanced Vector Extensions; 발견 적절 한 /arch AVX 플래그를 사용 하는 것이 좋습니다.
C4837|삼중 자가 발견 되었습니다. '?? *문자*'로 대체'*문자*'
C4986|'*선언*': 예외 사양이 이전 선언과 일치 하지 않습니다
C4987|비표준 확장명 사용: 'throw (...)'

## <a name="warnings-introduced-in-visual-c-2008-compiler-version-15002102208"></a>Visual c + + 2008 (컴파일러 버전 15.00.21022.08)에 도입 된 경고

이러한 경고 및 이후 버전에서 모든 경고는 컴파일러 옵션을 사용 하 여 억제 __/Wv:14__합니다.

|||
|-|-|
C4396|'*형식*': friend 선언이 함수 템플릿의 특수화를 참조 하는 경우 인라인 지정자를 사용할 수 없습니다.
C4413|'*선언*': 생성자가 끝낸 후에 존속 되지 않는 임시 참조 멤버가 초기화는
C4491|'*설명을*': IDL 버전 형식이 잘못 되었습니다에
C4603|'*이름을*': 매크로가 정의 되지 않았거나 미리 컴파일된 헤더 사용 후 정의가 다릅니다
C4627|'*설명을*': 미리 컴파일된 헤더 사용을 찾을 때 건너뛰었습니다
C4750|'*설명을*': 루프에 인라이닝된 인라이닝 _alloca () 사용 하 여 함수
C4910|'*형식*': '__declspec (dllexport)' 및 'extern' 명시적 인스턴스화에서 호환 되지 않습니다.
C4985|'*선언*': 이전 선언에 특성이 없습니다.

## <a name="warnings-introduced-in-visual-c-2005-compiler-version-140050727762"></a>Visual c + + 2005 (컴파일러 버전 14.00.50727.762)에 도입 된 경고

이러한 경고 및 이후 버전에서 모든 경고는 컴파일러 옵션을 사용 하 여 억제 __/Wv:13__합니다.

|||
|-|-|
C4000|알 수 없는 경고 하세요 Visual c + + 도움말 메뉴에서 [기술 지원] 명령을 선택 또는 자세한 정보에 대 한 기술 지원 도움말 파일
C4272|'*형식*': __declspec (dllimport)을 표시 하는; 함수를 가져올 때 네이티브 호출 규칙을 지정 해야 합니다.
C4333|'*식*': 오른쪽 시프트 횟수가 너무 커 데이터가 손실
C4334|'*식*': 32 비트 시프트의 결과가 암시적으로 64 비트로 변환 (64 비트 시프트를 사용 했습니다.)
C4335|Mac 파일 형식이 발견 되었습니다: 원본 파일을 DOS 나 UNIX 형식으로 변환 하세요
C4342|동작 변경: '*형식*' 호출 되었지만 이전 버전에서는 멤버 연산자가 호출
C4350|동작 변경: '*선언*'대신 호출'*선언*'
C4357|매개 변수 배열 인수 대리자에 대 한 정식 인수 목록에 '*선언*'를 생성할 때 무시'*형식*'
C4358|'*식*': 결합된 대리자의 반환 형식은 'void' 되지 않으면 반환된 값 정의 되지 않습니다.
C4359|'*형식*': 맞춤 지정 자가 실제 맞춤 보다 작습니다 (*번호*), 무시 됩니다.
C4362|'*형식*': 맞춤 8 바이트 보다 큰 CLR에서 지원 되지 않습니다
C4364|#using 어셈블리에 대 한 '*이름을*'에서 이전에 표시 *설명*(*번호*) as_friend 특성 없이 as_friend 적용 되지 않습니다
C4365|'*식을*': 변환할 '*유형*'to'*형식*', signed 또는 unsigned 일치 하지 않습니다.
C4366|단항의 결과가 '*연산자*' 연산자는 정렬 되지 않을 수 있습니다
C4367|변환에서 '*형식*'to'*형식*' 데이터 형식 잘못 맞춤 예외가 발생할 수 있습니다
C4368|정의할 수 없습니다. '*이름*의 멤버는 다음 작업을 관리 되 는' 있는 그대로'*형식*': 혼합된 형식은 지원 되지 않습니다
C4369|'*형식*': 열거자 값 '*번호*'로 표시할 수 없는'*형식*', 값은 '*번호*'
C4374|'*선언*': 인터페이스 메서드는 비가상 메서드에 의해 구현 되지 것입니다 '*선언*'
C4375|public이 아닌 메서드 '*선언*'재정의 하지 않는'*선언*'
C4376|액세스 지정자 '*지정자*:'는 지원 되지 않습니다: 사용 하십시오 '*지정자*:' 대신
C4377|네이티브 형식은 기본적으로 private입니다. -d1PrivateNativeTypes는 사용 되지 않습니다.
C4378|이니셜라이저를 실행 하는 함수 포인터를 가져와야 합니다. resolvemethodhandle
C4379|버전 *버전* 공용 언어 런타임에서이 컴파일러에서 지원 되지 않습니다. 이 버전을 사용 하 여 예기치 않은 결과가 발생할 수 있습니다.
C4381|'*선언*': public이 아닌 메서드에 의해 인터페이스 메서드를 구현할 수는 '*선언*'
C4382|throw '*형식*': __clrcall 소멸자 또는 복사 생성자를 사용 하 여 형식 /clr에서 낼 수 있습니다: 순수 모듈
C4383|'*형식*': 사용자 정의 하는 경우에 대 한 핸들 역참조의 의미가 변경할 수 '*연산자*' 연산자가; 연산자는 피연산자에 대 한 명시적 정적 함수로 작성
C4384|#pragma '*지시문*' 전역 범위에만 사용 해야
C4393|'*형식*': const 영향을 주지 않습니다 *설명* 데이터 멤버; 무시
C4394|'*형식*': __declspec로 appdomain 별 기호를 표시 되어야 합니다 (*값*)
C4395|'*형식*': initonly 데이터 멤버의 복사본에서 멤버 함수를 호출할 수는 '*형식*'
C4397|DefaultCharSetAttribute가 무시 됩니다.
C4398|'*형식*': appdomain이 여러 개 프로세스별 전역 개체가 제대로 작동 하지 않으면 __declspec (appdomain)를 사용 하는 것이 좋습니다.
C4399|'*형식*': __declspec로 프로세스별 기호를 표시 되어야 합니다 (*값*) /clr을 사용 하 여 컴파일하면: 순수
C4400|'*형식*':이 형식에서 const/volatile 한정자는 지원 되지 않습니다
C4412|'*선언*': 함수 시그니처에 형식 '*형식*'; C + + 개체에는 순수 코드 간에 전달 하는 안전 하지 않은 혼합형 / 네이티브 됩니다.
C4429|가능한 불완전 하거나 형식이 잘못 된 유니버설 문자 이름
C4430|형식 지정자가 없습니다. int로 가정합니다. 참고: c + + 기본 int를 지원 하지 않습니다.
C4431|형식 지정자가 없습니다. int로 가정합니다. 참고: C에서는 더 이상 기본 int를 지원하지 않습니다.
C4434|정적 생성자는 private 액세스 가능성이; 있어야 합니다. 개인 액세스로 변경합니다.
C4439|'*형식*': 시그니처에 관리 되는 형식 사용 하 여 함수 정의는 __clrcall 호출 규칙이 있어야 합니다.
C4441|호출 규칙의 '*규칙*' 무시 됩니다. '*규칙*' 대신 사용
C4445|'*선언*': 관리 되는 WinRT 형식 가상 메서드를 private 일 수 없습니다
C4460|CLR/WinRT 연산자 '*형식*', 참조로 매개 변수를 전달 합니다. CLR/WinRT 연산자 '*연산자*'에 c + + 연산자에서 다른 의미 체계가'*연산자*', 값으로 전달 하려고 했습니까?
C4461|'*형식*':이 클래스에 종료 자가 '! *형식*' 소멸자가 없습니다 있지만 ' ~*형식*'
C4470|/clr에서 무시 되는 부동 소수점 제어 pragma
C4480|비표준 확장이 사용 됨: 열거형에 대 한 기본 형식 지정 '*형식*'
C4481|비표준 확장이 사용 됨: 재정의 지정자 '*지정자*'
C4482|비표준 확장이 사용 됨: 열거형 '*형식*' 정규화 된 이름에 사용
C4483|구문 오류: c + + 키워드 필요 합니다.
C4484|'*형식*': 일치 기본 ref 클래스 메서드 '*형식*', 'virtual', 'new' 또는 'override'; 표시 되지 않지만 'new' (및 'virtual' 아님) 가정
C4485|'*형식*': 일치 기본 ref 클래스 메서드 '*형식*'를 아닌 '표시 된 new' 또는 'override'; 'new' ('virtual')는 가정
C4486|'*형식*': ref 클래스 또는 값 클래스의 전용 가상 메서드를 'sealed'으로 표시 되어야 합니다
C4487|'*형식*': 일치 상속 된 비가상 메서드 '*형식*' 명시적으로 표시 되어 있지 않습니다 'new' 하지만
C4488|'*형식*': 필요한 '*키워드*'키워드는 인터페이스 메서드를 구현 하려면'*형식*'
C4489|'*키워드*': 인터페이스 메서드를 사용할 수 없습니다 '*이름*'; 재정의 지정자는 ref 클래스와 값 클래스 메서드에만 사용할 수
C4490|'*키워드*': 재정의 지정자;를 잘못 사용 했습니다. '*형식*' 기본 ref 클래스 메서드를 일치 하지 않습니다
C4538|'*형식*':이 형식에서 const/volatile 한정자는 지원 되지 않습니다
C4559|'*형식*': 재정의; 함수 향상 __declspec (*값*)
C4565|'*형식*': 재정의; 기호를 __declspec를 사용 하 여 이전에 선언 되었습니다 (*값*)
C4566|유니버설 문자 이름으로 표현 되는 문자 '*문자*' 현재 코드 페이지에서 표현할 수 없는 (*번호*)
C4568|'*형식*': 멤버가 명시적 재정의의 시그니처와 일치
C4569|'*형식*': 멤버가 명시적 재정의의 시그니처와 일치
C4570|'*형식*': 명시적으로 선언 되지 추상 않았지만 추상 함수를가지고
C4571|Visual c + + 7.1; 변경 알림:부터 의미 체계 구조적된 예외 (SEH) 변경 되었습니다.
C4572|'...'를 사용 합니다 /clr [ParamArray] 특성은 사용 되지 않습니다. 대신
C4580|[attribute]는 사용 되지 않습니다. 대신 지정할 *지정한*기본 클래스로 특성
C4581|사용 되지 않는 동작: ' "*이름을*"' 바뀝니다 '*이름*' 프로세스 특성
C4606|#pragma 경고: '*번호*' 무시 됩니다. 코드 분석 경고가 경고 수준과 연결 되어 있지 않습니다.
C4631|MSXML 또는 XPath를 사용할 수 없습니다. XML 문서 주석이 처리되지 않습니다. *description*
C4632|XML 문서 주석: *설명을* -액세스 거부: *설명*
C4633|XML 문서 주석을*설명을*: 오류: *설명*
C4634|XML 문서 주석을*설명을*: 적용할 수 없습니다: *설명*
C4635|XML 문서 주석을*설명을*: 잘못 된 형식의 XML: *설명*
C4636|XML 문서 주석을*설명을*: 태그 필요 비어 있지 않은 '*설명*' 특성입니다.
C4637|XML 문서 주석을*설명을*: \<포함 > 태그가 삭제 되었습니다. *description*
C4638|XML 문서 주석을*설명을*: 알 수 없는 기호에 대 한 참조가 '*설명*'.
C4639|MSXML 오류, XML 문서 주석이 처리 되지 것입니다. *description*
C4641|XML 문서 주석에 모호한 상호 참조가 있습니다.
C4678|기본 클래스*선언*'인덱서보다 is'*이름*'
C4679|'*설명을*': 멤버를 가져올 수 없습니다
C4687|'*형식*': 봉인된 추상 클래스는 인터페이스를 구현할 수 없습니다 '*형식*'
C4688|'*이름을*': 제약 조건 목록에 어셈블리 전용 형식 '*선언*'
C4690|\[ emitidl (pop)]: 푸시 횟수 보다 팝
C4691|'*형식*': 참조 되지 않은 참조 하는 형식에서 예상 된 *모듈* '*설명*'를 대신 사용 하는 현재 변환 단위에 정의 된 형식
C4692|'*이름을*': 전용이 아닌 멤버의 시그니처에 어셈블리 전용 네이티브 형식 '*선언*'
C4693|'*형식*': 봉인된 추상 클래스는 인스턴스 멤버를 사용할 수 없습니다*이름*'
C4694|'*형식*': 봉인된 추상 클래스는 기본 클래스 '를 사용할 수 없습니다*형식*'
C4720|인라인 어셈블러 보고서: '*설명을*'
C4721|'*설명을*': 내장 함수로 사용할 수 없음
C4722|'*설명을*': 소멸자가 반환 하지 않습니다 잠재적인 메모리 누수
C4726|Arch4/4T 지원만 ARM '\<r _ f > 또는 \<spsr_f >' 즉 치 값을 사용 하 여
C4727|명명 된 PCH *이름* 있는 동일한 타임 스탬프를 사용 하 여 *이름* 하 고 *이름*합니다.  첫 번째 PCH를 사용합니다.
C4729|선형 그래프 기반 경고에 사용하기에는 함수가 너무 큽니다.
C4730|'*설명을*': _m64 혼합 및 부동 소수점 식이 잘못 된 코드에서 발생할 수 있습니다
C4731|'*설명을*': 프레임 포인터 레지스터가 '*등록*' 인라인 어셈블리 코드에 의해 수정
C4732|내장 '*내장*'이 아키텍처에서 지원 되지 않습니다
C4733|인라인 asm 'fs:0'에 할당 합니다: 처리기 안전한 처리기로 등록 되지 않았습니다
C4734|두 개 64k COFF에 줄 번호 디버그 정보 섹션 이상 모듈에 대 한 COFF 디버그 줄 번호를 내보내지 않습니다. '*모듈*'
C4738|32비트 float 결과를 메모리에 저장하면 성능이 저하될 수 있습니다.
C4739|변수에 대 한 참조가 '*변수*' 저장소 공간을 초과 합니다
C4740|인라인 asm 코드 안팎에서 흐름을 선택 하면 전역 최적화
C4742|'*변수에*'다른 맞춤에 '*위치*'및'*위치*': *번호* 고 *수*
C4743|'*이름을*'다른 크기의 '*위치*'및'*위치*': *번호* 하 고 *번호* 바이트
C4744|'*이름을*'에 다른 형식'*위치*'및'*위치*': '*형식*'및'*형식*'
C4747|관리 되는 호출 '*형식*': DLL 진입점 및 DLL 진입점에서에 도달 하는 호출을 포함 하 여, 로더 잠금 상태에서 관리 되는 코드를 실행할 수 있습니다
C4761|정수 크기가 인수와 일치 하지 않습니다 변환 됩니다.
C4764|16바이트를 초과하도록 catch 개체를 맞출 수 없습니다.
C4788|'*식별자*': 식별자로 잘렸습니다. '*번호*' 문자
C4789|버퍼 '*이름을*' 크기인 *번호* 바이트 오버런 됩니다. *번호* 바이트가 오프셋부터 쓰입니다 *수*
C4801|참조로 반환은 확인할 수 없습니다: *설명*
C4819|현재 코드 페이지에서 표현할 수 없는 문자가 파일 (*수*). 데이터 손실을 방지 하려면 유니코드 형식으로 파일을 저장 합니다.
C4826|변환에서 '*형식*'to'*형식*' 부호가 확장 됩니다. 이 예기치 않은 런타임 동작이 발생할 수 있습니다.
C4829|main 함수에 대한 매개 변수가 잘못된 것 같습니다. 고려 ' int main (platform:: array\<platform:: string ^ > ^ argv)'
C4835|'*형식*': 내보낸된 데이터에 대 한 이니셜라이저는 관리 되는 코드가 호스트 어셈블리에서 먼저 실행 될 때까지 실행 되지 것입니다
C4867|'*형식*': 비표준 구문; 사용 하 여 '&' 멤버에 대 한 포인터를 만들려면
C4936|/clr 또는 /clr:pure를 지정하여 컴파일한 경우에만 이 __declspec를 사용할 수 있습니다.
C4937|'*이름을*'및'*이름*'에 대 한 인수로 구분할 수 없습니다 는'*옵션*'
C4938|'*형식*': 부동 지점 환산 변수 /fp 결과가 일치 하지 않을 수 있습니다: strict 또는 #pragma fenv_access
C4939|#pragma vtordisp는 사용되지 않으므로 이후 Visual C++ 릴리스에서 제거될 예정입니다.
C4947|'*형식*': 되지 않음으로 표시
C4949|pragma 'managed' 및 '는 사용 하 여 컴파일된 경우에 의미가 ' / clr [: 옵션]'
C4950|'*형식*': 되지 않음으로 표시
C4955|'*설명을*': 가져오기 무시;에서 이미 가져온 '*원본*'
C4956|'*형식*':이 형식은 확인할 수 없습니다
C4957|'*식*': 명시적 캐스트에서 '*유형*'to'*형식*'를 확인할 수 없습니다
C4958|'*식*': 포인터 산술 연산은 확인할 수 없습니다
C4959|관리 되지 않는 정의할 수 없습니다 *클래스* '*형식*' /clr: safe에서 해당 멤버에 액세스 하면 비안정형 코드가 생성 되므로
C4960|'*설명을*' 너무 커서 프로 파일링 할 수 없습니다.
C4961|프로필 데이터가 병합 된 '*위치*'를 사용 하지 않도록 설정 하는 프로필 기반 최적화
C4962|'*설명을*': 최적화 프로필 데이터가 일관성이 없는 상태가 발생 하므로 사용 하지 않도록 설정 하는 프로필 기반 최적화
C4963|'*설명을*': 프로필 데이터가 없습니다; 계측 된 빌드에서 다른 컴파일러 옵션을 사용한
C4964|최적화 옵션을 지정 합니다. 프로필 정보 수집 되지 않습니다.
C4965|정수 0; 암시적 상자 nullptr 또는 명시적 캐스트를 사용 하 여
C4970|대리 생성자: 이후 대상 개체가 무시 '*선언*'는 정적
C4971|인수 순서: \<대상 개체 >를 \<함수를 대상 > 대리자 생성자는 사용 되지 않는, 사용 \<함수를 대상 >, \<대상 개체 >
C4972|왼쪽 항의 값(l-value)을 확인할 수 없어 unboxing 작업의 결과를 직접 수정하거나 처리하고 있습니다.

## <a name="warnings-introduced-in-visual-c-2003-compiler-version-13103077"></a>Visual c + + 2003 (컴파일러 버전 13.10.3077)에 도입 된 경고

이러한 경고 및 이후 버전에서 모든 경고는 컴파일러 옵션을 사용 하 여 억제 __/Wv:13.00.9466__합니다.

|||
|-|-|
C4343|#pragma 최적화 (*설명을*, off) /Og 옵션을 재정의
C4344|동작 변경: 명시적 템플릿 인수 결과 호출에서 사용 하 여 '*선언*'
C4346|'*형식*': 종속 이름이 형식이 아닙니다.
C4348|'*선언*': 기본 매개 변수 재정의: 매개 변수 *수*
C4356|'*형식*': 파생된 클래스를 통해 정적 데이터 멤버를 초기화할 수 없습니다
C4408|익명 *구조체* 데이터 멤버를 선언 하지 않았습니다.
C4544|'*선언*': 기본 템플릿 인수가이 템플릿 선언에서 무시 됩니다.
C4545|쉼표 앞의 식이 인수 목록이 없는 함수로 계산됩니다.
C4546|쉼표 앞의 함수에 인수 목록이 없습니다.
C4547|'*식*': 쉼표 효과가 없습니다; 앞의 연산자 파생 작업이 있는 연산자 여야 합니다.
C4548|쉼표 앞의 식은 의미 없는 식입니다. 파생 작업이 있는 식이어야 합니다.
C4549|'*식을*': 쉼표 앞의 연산자는 의미 없는 사용 하려고 했습니까 '*식*'?
C4628|-Ze에는 digraph가 지원되지 않습니다. 문자 시퀀스 '*시퀀스*'에 대 한 대체 토큰으로 해석 되지 않는'*토큰*'
C4629|digraph 사용 되는 문자 시퀀스 '*시퀀스*'토큰으로 해석'*토큰*' (아니라면이 경우 두 문자 사이 공백을 삽입)
C4671|'*설명을*': 복사 생성자가 액세스할 수 없습니다
C4676|'*설명을*': 소멸자에 액세스할 수 없는
C4677|'*이름을*': 전용이 아닌 멤버의 시그니처에 어셈블리 전용 형식 '*선언*'
C4686|'*형식*': 동작 변경 되었을 수 있습니다, udt 반환 호출 규칙이
C4812|사용 되지 않는 선언 스타일:를 사용 하십시오 '*형식*::*이름*' 대신
C4813|'*형식*': 지역 클래스의 friend 함수가 이전에 선언 해야
C4821|시그니처 (BOM)를 사용 하 여 파일을 저장 하세요 유니코드 인코딩 형식을 확인할 수 없습니다.
C4822|'*형식*': 지역 클래스 멤버 함수에 본문이 없습니다.
C4823|'*형식*': 사용 고정 포인터 하지만 해제 의미 체계를 사용할 수 없습니다. /EHa를 사용 하는 것이 좋습니다.
C4913|사용자 정의 이항 연산자 ','가 존재하지만 오버로드가 모든 피연산자를 변환하지 못했습니다. 기본 내장 이항 연산자 ','를 사용합니다.
C4948|반환 형식 '*선언*' 해당 setter의 마지막 매개 변수 형식과 일치 하지 않습니다
C4951|'*설명을*' 프로필 데이터가 수집 된 함수 프로필 데이터가 사용 되지 않습니다 이후 편집 되었습니다.
C4952|'*설명을*': 프로그램 데이터베이스에 프로필 데이터가 없습니다 '*설명*'
C4953|인라인 '*설명을*' 프로필 데이터가 수집 된 이후 편집 되었습니다.
C4954|'*설명을*': 프로 파일링 되지 ((__int64 switch 식 포함)

## <a name="warnings-introduced-in-visual-c-2002-compiler-version-13009466"></a>Visual c + + 2002 (컴파일러 버전 13.00.9466)에 도입 된 경고

이러한 경고 및 이후 버전에서 모든 경고는 컴파일러 옵션을 사용 하 여 억제 __/Wv:12__합니다.

|||
|-|-|
C4096|'*형식*': 인터페이스가 COM 인터페이스가 아니므로; IDL로 내보내지 것입니다
C4097|pragma 매개 변수는 'restore' 또는 'off'이어야 합니다.
C4165|'Bool'; 'HRESULT' 변환 되는 원하는 작업 인지 입니까?
C4183|'*이름을*': 'int'를 반환 하는 멤버 함수로 간주; 반환 형식이 없습니다
C4199|*description*
C4255|'*이름을*': 함수 프로토타입을 입력 하지 않았습니다. '()'에서 '(void)'로 변환
C4256|'*선언*': 가상 기본 클래스 생성자가 '...'; 호출 이전 버전의 Visual c + +와 호환 되지 않을 수 있습니다
C4258|'*이름을*': 정의 바깥쪽 범위에서 정의 되 루프 무시 됩니다.
C4263|'*선언*': 멤버 함수가 기본 클래스 가상 멤버 함수를 재정의 하지 않습니다
C4264|'*선언*': 재정의 기본 가상 멤버 함수에 대해 사용할 수 없습니다 '*클래스*'; 함수가 숨겨집니다.
C4265|'*형식*': 클래스에 가상 함수가 있지만 소멸자는 가상이이 클래스의 인스턴스 수 하지 정확 하 게 소멸
C4266|'*선언*': 재정의 기본 가상 멤버 함수에 대해 사용할 수 없습니다 '*클래스*'; 함수가 숨겨집니다.
C4267|'*식을*': 변환 하려면 'size_t'에서 '*형식*', 데이터 손실 될 수 있습니다
C4274|#ident 무시 됩니다. #pragma 주석 (exestr, 'string')에 대 한 설명서를 참조 하세요.
C4277|가져온된 항목 '*형식*::*이름*' 데이터 멤버 및 함수 멤버에 있는 데이터 멤버가 무시 됩니다.
C4278|'*이름을*': 형식 라이브러리의 식별자 '*설명*'가 이미 매크로 'rename' 한정자를 사용 하십시오.
C4279|'*이름을*': 형식 라이브러리의 식별자 '*설명*' 키워드는 'rename' 한정자를 사용 합니다.
C4287|'*식*': 서명 되지 않은 또는 음의 상수가 일치 하지 않습니다
C4288|비표준 확장이 사용 됨: '*이름을*': for 루프에서 선언 된 루프 제어 변수가 for 루프 범위 외부에서 사용은; 외부 범위에 있는 선언과 충돌
C4289|비표준 확장이 사용 됨: '*이름을*': for 루프에서 선언 된 루프 제어 변수가 for 루프 범위 외부에서 사용 됩니다
C4293|'*식*': 시프트 횟수가 음수 이거나 너무 큽니다., 정의 되지 않은 동작
C4295|'*형식*': 배열이 너무 작아서 null 종결 문자를 포함 합니다.
C4296|'*식을*': 식이 항상 *값*
C4297|'*형식*': 함수 간주 되었으나 예외를 throw 하지 않습니다
C4298|'*이름을*': 형식 라이브러리의 식별자 '*설명*'가 이미 매크로; 이름을 ' __*이름*'
C4299|'*이름*': 형식 라이브러리의 식별자 '*설명*' 키워드는 이름을 ' __*이름*'
C4302|'*식을*':에서 잘림 '*유형*'to'*형식*'
C4303|*변환이* 에서 '*형식*'to'*형식*'는 static_cast, __try_cast 또는 dynamic_cast 사용 하 여 사용 되지 않으며,
C4314|pragma 매개 변수는 '32' 또는 '64' 이어야 합니다.
C4315|'*형식*': 'this'이 포인터 멤버에 대 한 '*유형*' 정렬 되지 않을 수 있습니다 *번호* 생성자가 예상 대로
C4318|memset에 길이로 상수 0을 전달합니다.
C4319|'*식을*': 0 확장 '*유형*'to'*형식*' 큰 크기의
C4321|자동으로 생성 되는 인터페이스의 IID를 '*형식*'
C4322|자동으로 생성 되는 클래스에 대 한 CLSID*형식*'
C4323|다시 사용 하 여 등록 된 CLSID를 클래스*형식*'
C4324|'*형식*': 맞춤 지정자 때문에 구조체가 채워졌습니다
C4325|표준 섹션에 대 한 특성 '*설명을*' 무시
C4326|반환 형식 '*이름을*'있어야'*유형*' of '*형식*'
C4327|'*식을*': LHS의 간접 참조 맞춤이 (*번호*) RHS 보다 크면 (*번호*)
C4328|'*설명*': 정식 매개 변수의 간접 참조 맞춤이 *수* (*번호*) 실제 인수의 맞춤 보다 큽니다 (*번호*)
C4329|맞춤 지정 자가 enum에서 무시 됩니다.
C4336|상호 참조 된 형식 라이브러리 가져오기 '*라이브러리*'가져오기' before*설명*'
C4337|상호 참조 된 형식 라이브러리 '*라이브러리*'에서'*설명*'는 자동으로 가져옵니다.
C4338|#pragma *설명을*: 표준 섹션 '*섹션*' 사용
C4339|'*형식*':이 형식 사용 하면 런타임 예외가 발생할 수 있습니다 CLR/WinRT 메타 데이터에 정의 되지 않은 형식이 사용 되었습니다
C4353|비표준 확장이 사용 됨: 함수 식으로 상수 0입니다.  내장 '__noop' 함수를 대신 사용
C4370|'*선언*': 압축 기능이 향상 되어 컴파일러의 이전 버전에서 클래스 레이아웃이 변경 되었습니다
C4371|'*선언*': 멤버를 잘 압축 했기 때문에 컴파일러의 이전 버전에서 클래스 레이아웃이 변경 될 수 있습니다 '*멤버*'
C4373|'*형식*': 가상 함수 재정의*선언*', 이전 버전의 컴파일러는 매개 변수는 const/volatile 한정자만 다릅니다 때 재정의 하지 않았습니다
C4387|'*설명을*': 고려 되었습니다
C4389|'*식*': signed 또는 unsigned 일치 하지 않습니다.
C4391|'*선언*': 예상 내장 함수에 대 한 잘못 된 반환 형식 '*형식*'
C4392|'*선언*': 내장 함수를 예상에 대 한 인수 개수가 잘못 되었습니다 '*번호*' 인수
C4407|멤버 표현이 다른 포인터를 간의 캐스팅, 컴파일러 발생할 잘못 된 코드
C4420|'*이름을*': 사용 하 여 연산자를 사용할 수 없는 '*이름*' 대신 런타임 검사가 손상 될 수 있습니다
C4440|재정의 된 호출 규칙이에서 '*설명을*'to'*설명*' 무시
C4442|__annotation 인수에 null 종결자를 포함 합니다.  값이 잘립니다.
C4444|'*이름을*':이 컨텍스트에서 최상위 '__unaligned' 구현 되지 않았습니다
C4526|'*형식*': 정적 멤버 함수는 가상 함수를 재정의할 수 없습니다 '*선언*' 무시 재정의 가상 함수는 숨겨집니다.
C4531|C + + 예외 처리를 Windows CE에서 사용할 수 없습니다. 구조적된 예외 처리 사용
C4532|'*설명을*': 밖으로 점프할 *마지막으로* 블록의 동작을 정의 되지 않은 종료 처리 중
C4533|초기화의 '*선언*' 의해 생략 되었습니다. ' goto *선언*'
C4534|'*선언*'에 대 한 기본 생성자를 됩니다 *클래스* '*형식*' 인해 기본 인수
C4535|호출 _set_se_translator /EHa 필요
C4536|'*설명을*': 형식-이름이 메타 데이터 한계인 초과 '*번호*' 문자
C4537|'*선언*': '.' 비 UDT 형식에 적용
C4542|쓸 수 없습니다 병합된 삽입 된 텍스트 파일의 생성을 건너뛰므로 *형식* 파일: '*filename*': *오류*
C4543|특성으로 표시 되지 않도록 하는 텍스트를 삽입 ' 없습니다\_injected_text'
C4555|식이 효과가 없습니다. 파생 작업이 있는 식이어야 합니다.
C4557|'__assume' 효과가 있습니다. '*효과*'
C4558|피연산자의 값 '*번호*'범위를 벗어났습니다'*번호* - *번호*'
C4561|와 호환 되지 않는 ' __fastcall'는 ' / clr' 옵션: '__stdcall'으로 변환
C4562|완전히 프로토타입화 된 함수가 필요는 ' / clr' 옵션: '()'에서 '(void)'로 변환
C4564|메서드 '*이름을*'의 *클래스* '*형식*'지원 되지 않는 기본 매개 변수 정의'*매개 변수*'
C4584|'*형식*': 기본 클래스 '*선언*'의 기본 클래스는 이미'*선언*'
C4608|공용 구조체의 여러 멤버를 초기화 합니다. '*형식*'및'*형식*'
C4619|#pragma 경고: 방법이 없는 경고 번호 '*번호*'
C4623|'*형식*': 기본 생성자가 암시적으로 삭제 된 것으로 정의 됩니다
C4624|'*형식*': 소멸자가 삭제 된 것으로 암시적으로 된 정의
C4625|'*형식*': 복사 생성자가 암시적으로 삭제 된 것으로 정의 됩니다
C4626|'*형식*': 삭제 된 것으로 대입 연산자가 암시적 된 정의
C4645|'noreturn'으로 선언 된 함수에 return 문이
C4646|'noreturn'으로 선언 된 함수에 void가 아닌 반환 형식이
C4659|#pragma '*설명을*': 예약 된 세그먼트 '*이름*'에 정의 되지 않은 동작을 사용 하 여 #pragma 주석 (linker,...)
C4667|'*선언*': 강제 인스턴스화와 일치 하는 정의 된 함수 템플릿이 없습니다
C4668|'*이름을*'에 대해 '0'으로 바꾸기 전처리기 매크로로 정의 되지 않은'*값*'
C4669|'*식을*': 안전 하지 않은 변환: '*형식*'는 관리 되는 WinRT 형식 개체
C4674|'*이름을*'로 선언 해야 'static' 및 매개 변수가 하나만 있어야
C4680|'*형식*': coclass는 기본 인터페이스를 지정 하지 않습니다
C4681|'*형식*': coclass가 이벤트 소스인 기본 인터페이스를 지정 하지 않습니다
C4682|'*형식*': 방향 매개 변수 특성을 지정 하지, 기본적으로 [in]
C4683|'*선언*': 이벤트 소스에 'out'-여러 이벤트 처리기를 후크 하는 경우 주의 해야 합니다; 매개 변수
C4684|'*설명을*': 경고!! 특성으로 인해 잘못 된 코드가 생성 될 수 있습니다: 주의 하 여 사용
C4685|템플릿 매개 변수를 분석하는 경우 '> >'가 있어야 하는데 '>>'가 왔습니다.
C4700|초기화 되지 않은 지역 변수 '*이름을*' 사용
C4701|잠재적으로 초기화 되지 않은 지역 변수 '*이름을*' 사용
C4702|접근할 수 없는 코드
C4711|함수 '*이름을*' 자동 인라인 확장 선택
C4714|함수 '*선언*' 인라인이 아니라 __forceinline로 표시
C4715|'*함수*': 값을 반환 하는 모든 제어 경로
C4716|'*함수*': 값을 반환 해야 합니다
C4717|'*함수*': 모든 제어 경로에서 재귀적 함수로 인해 런타임 스택 오버플로
C4718|'*함수*': 재귀 호출에 파생 작업이 없습니다. 삭제 하는 중
C4719|이중 상수를 Qfast로 지정 된 경우-사용 하 여 'f'를 단 정밀도 나타내는 접미사를 찾았습니다.
C4723|0으로 나누기 연산이 발생할 수
C4724|0의 나머지 연산이 발생할 수 있습니다.
C4725|명령이 일부 Pentium에서 정확하지 않을 수 있습니다.
C4757|첨자가 부호 없는 값이 크면, 음의 상수를 사용 하려고 했습니까?
C4772|#import; 누락 된 형식 라이브러리에서 형식을 참조 '*설명을*' 자리 표시자로 사용
C4792|함수 '*함수*' sysimport를 사용 하 여 선언 되 고 참조 된 네이티브 코드에서 가져오기 라이브러리 하는 데 필요한 연결
C4794|스레드 로컬 저장소 변수 세그먼트 '*이름을*'에서 변경'*세그먼트*'to'*세그먼트*'
C4798|p 코드 함수에 대 한 생성 된 네이티브 코드 '*이름을*' 예외 처리기를 사용 하 여 또는 해제 의미 체계
C4799|함수 '*이름을*'에 emms 명령이 없습니다
C4803|'*선언*': raise 메서드에 이벤트를 다른 저장소 클래스에 '*선언*'
C4810|pragma pack (show) 값 = = *수*
C4811|pragma conform (forScope, show) = = *값*
C4820|'*형식*': '*번호*' 바이트 채움 문자가 뒤에 추가 *형식* '*형식*'
C4905|와이드 문자열 리터럴 캐스팅 '*형식*'
C4906|문자열 리터럴을로 캐스트 '*형식*'
C4912|'*특성*': 특성의 중첩된 UDT에 대 한 동작으로 정의 되지 않은.
C4916|dispid를 하기 위해 '*형식*': 인터페이스에 의해 정의 되어야 합니다
C4917|'*형식*': GUID 클래스, 인터페이스 또는 네임 스페이스를 사용 하 여 연결할 수만
C4918|'*문자*': pragma 최적화 목록에 잘못 된 문자
C4920|열거형 *이름을* 멤버 *이름*=*번호* 열거형에 이미 표시 *이름을* 으로 *이름* = *수*
C4921|'*이름을*': 특성 값 '*값*' 여러 번 지정할 수 없습니다
C4925|'*선언*': 스크립트에서 dispinterface 메서드를 호출할 수 없습니다.
C4926|'*선언*': 기호가 이미 정의 되어: 무시 된 특성
C4927|변환이 잘못 되었습니다. 둘 이상의 사용자 정의 변환이 암시적으로 적용 된
C4928|복사 초기화가 잘못되었습니다. 사용자 정의 변환이 암시적으로 두 번 이상 적용되었습니다.
C4929|'*설명을*': typelibrary 있습니다. 'embedded_idl' 한정자를 무시 합니다.
C4930|'*선언*': 프로토타입 함수가 호출 되지 않습니다 (의도 되는 변수 정의 었 나요?)
C4931|에 대 한 형식 라이브러리를 빌드 했다고 간주 *수*-비트 포인터
C4932|__identifier (*설명을*)와 __identifier (*설명*)를 구분할 수 없습니다
C4934|'__delegate' 대신 사용 하 여, '__delegate(multicast)'는 사용 되지 않습니다.
C4935|어셈블리 액세스 지정 자가 수정에서 '*설명을*'
C4944|'*이름을*': 기호를 가져올 수 없습니다 '*원본*': '*선언*' 현재 범위에 이미 있습니다
C4945|'*이름을*': 기호를 가져올 수 없습니다 '*원본*': '*선언*'이미 가져온 다른 어셈블리에서 '*원본*'
C4946|reinterpret_cast가 관련된 클래스 간의 사용 되었습니다. '*선언*'및'*선언*'
C4995|'*이름을*': 사용 되지 않는 #pragma로 표시 되어 이름
C4996|'*문제*': *설명*
C4997|'*형식*': coclass가 COM 인터페이스 또는 의사 (pseudo) 인터페이스를 구현 하지 않습니다
C4998|예상 실패: *설명을*(*번호*)

## <a name="see-also"></a>참고자료

- [/Wv 컴파일러 옵션](../../build/reference/compiler-option-warning-level.md)
- [기본적으로 해제 되어 있는 컴파일러 경고](../../preprocessor/compiler-warnings-that-are-off-by-default.md)
- [warning](../../preprocessor/warning.md)
