---
title: basic_ifstream 클래스 | Microsoft 문서
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
f1_keywords:
- fstream/std::basic_ifstream
- fstream/std::basic_ifstream::close
- fstream/std::basic_ifstream::is_open
- fstream/std::basic_ifstream::open
- fstream/std::basic_ifstream::rdbuf
- fstream/std::basic_ifstream::swap
dev_langs:
- C++
helpviewer_keywords:
- std::basic_ifstream [C++]
- std::basic_ifstream [C++], close
- std::basic_ifstream [C++], is_open
- std::basic_ifstream [C++], open
- std::basic_ifstream [C++], rdbuf
- std::basic_ifstream [C++], swap
ms.assetid: 366cd9a7-efc4-4b7f-ba10-c8271e47ffcf
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 63712f6eb7efd9c52db5480b7f13babe9601dea2
ms.sourcegitcommit: 761c5f7c506915f5a62ef3847714f43e9b815352
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44110229"
---
# <a name="basicifstream-class"></a>basic_ifstream 클래스

문자 특성이 클래스 `Tr`에 의해 결정되는 `Elem` 형식의 요소가 있는 클래스 [basic_filebuf](../standard-library/basic-filebuf-class.md)< `Elem`, `Tr`>의 스트림 버퍼에서 요소 및 인코드된 개체의 추출을 제어하는 개체에 대해 설명합니다.

## <a name="syntax"></a>구문

```cpp
template <class Elem, class Tr = char_traits<Elem>>
class basic_ifstream : public basic_istream<Elem, Tr>
```

### <a name="parameters"></a>매개 변수

*Elem*<br/>
파일 버퍼의 기본 요소입니다.

*Tr*<br/>
파일 버퍼 기본 요소의 특성(일반적으로 `char_traits`< `Elem`>)입니다.

## <a name="remarks"></a>설명

이 개체는 `basic_filebuf`< `Elem`, `Tr`> 클래스의 개체를 저장합니다.

## <a name="example"></a>예제

다음 예제에서는 파일에서 텍스트를 읽는 방법을 보여 줍니다.

```cpp
// basic_ifstream_class.cpp
// compile with: /EHsc

#include <fstream>
#include <iostream>

using namespace std;

int main(int argc, char **argv)
{
    ifstream ifs("basic_ifstream_class.txt");
    if (!ifs.bad())
    {
        // Dump the contents of the file to cout.
        cout << ifs.rdbuf();
        ifs.close();
    }
}
```

## <a name="input-basicifstreamclasstxt"></a>입력: basic_ifstream_class.txt

```cpp
This is the contents of basic_ifstream_class.txt.
```

## <a name="output"></a>출력

```cpp
This is the contents of basic_ifstream_class.txt.
```

### <a name="constructors"></a>생성자

|생성자|설명|
|-|-|
|[basic_ifstream](#basic_ifstream)|`basic_ifstream` 개체의 새 인스턴스를 초기화합니다.|

### <a name="member-functions"></a>멤버 함수

|멤버 함수|설명|
|-|-|
|[close](#close)|파일을 닫습니다.|
|[is_open](#is_open)|파일이 열려 있는지 확인합니다.|
|[open](#open)|파일을 엽니다.|
|[rdbuf](#rdbuf)|저장된 스트림 버퍼 주소를 반환합니다.|
|[swap](#swap)|이 `basic_ifstream`의 콘텐츠를 제공된 `basic_ifstream`의 콘텐츠로 교환합니다.|

### <a name="operators"></a>연산자

|연산자|설명|
|-|-|
|[operator=](#op_eq)|이 스트림 개체의 콘텐츠를 할당합니다. 복사본을 남기지 않는 `rvalue`와 관련된 이동 할당입니다.|

## <a name="requirements"></a>요구 사항

**헤더:** \<fstream>

**네임스페이스:** std

## <a name="basic_ifstream"></a>  basic_ifstream::basic_ifstream

`basic_ifstream` 형식의 개체를 생성합니다.

```cpp
basic_ifstream();

explicit basic_ifstream(
    const char* _Filename,
    ios_base::openmode _Mode = ios_base::in,
    int _Prot = (int)ios_base::_Openprot);

explicit basic_ifstream(
    const wchar_t* _Filename,
    ios_base::openmode _Mode = ios_base::in,
    int _Prot = (int)ios_base::_Openprot);

basic_ifstream(basic_ifstream&& right);
```

### <a name="parameters"></a>매개 변수

*_Filename*<br/>
열어야 할 파일의 이름입니다.

*모드 (_m)*<br/>
[ios_base::openmode](../standard-library/ios-base-class.md#openmode)의 열거형 중 하나입니다.

*_Prot*<br/>
[_fsopen, _wfsopen](../c-runtime-library/reference/fsopen-wfsopen.md)의 `shflag` 매개 변수와 같은 기본 파일 열기 보호입니다.

### <a name="remarks"></a>설명

첫 번째 생성자는 [basic_istream](../standard-library/basic-istream-class.md)( `sb`)를 호출하여 기본 클래스를 초기화합니다. 여기서 `sb`는 [basic_filebuf](../standard-library/basic-filebuf-class.md)< `Elem`, `Tr`> 클래스의 저장된 개체입니다. 또한 `basic_filebuf`< `Elem`, `Tr`>을 호출하여 `sb`를 초기화합니다.

두 번째 및 세 번째 생성자는 `basic_istream`( `sb`)를 호출하여 기본 클래스를 초기화합니다. 또한 `sb`를 초기화하는데, 이번에는 [basic_filebuf](../standard-library/basic-filebuf-class.md#basic_filebuf)< `Elem`, `Tr`> 및 `sb`. [open](../standard-library/basic-filebuf-class.md#open)( `_Filename`, `_Mode` &#124; `ios_base::in`)을 차례로 호출합니다. 후자 함수가 null 포인터를 반환하면 생성자는 **setstate**( `failbit`)를 호출합니다.

네 번째 생성자는 rvalue 참조로 처리되는 `right`의 내용으로 개체를 초기화합니다.

### <a name="example"></a>예제

다음 예제에서는 파일에서 텍스트를 읽는 방법을 보여 줍니다. 파일을 만들려면 [basic_ofstream::basic_ofstream](../standard-library/basic-ofstream-class.md#basic_ofstream)에 대한 예제를 참조하세요.

```cpp
// basic_ifstream_ctor.cpp
// compile with: /EHsc

#include <fstream>
#include <iostream>

using namespace std;

int main(int argc, char **argv)
{
    ifstream ifs("basic_ifstream_ctor.txt");
    if (!ifs.bad())
    {
        // Dump the contents of the file to cout.
        cout << ifs.rdbuf();
        ifs.close();
    }
}
```

## <a name="close"></a>  basic_ifstream::close

파일을 닫습니다.

```cpp
void close();
```

### <a name="remarks"></a>설명

멤버 함수 호출 [rdbuf](#rdbuf) **->** [닫습니다](../standard-library/basic-filebuf-class.md#close)합니다.

### <a name="example"></a>예제

`close`의 사용 예제는 [basic_filebuf::close](../standard-library/basic-filebuf-class.md#close)를 참조하세요.

## <a name="is_open"></a>  basic_ifstream::is_open

파일이 열려 있는지 확인합니다.

```cpp
bool is_open() const;
```

### <a name="return-value"></a>반환 값

파일이 열린 경우 **true**, 아닌 경우 **false**입니다.

### <a name="remarks"></a>설명

멤버 함수는 반환 [rdbuf](#rdbuf) **->** [is_open](../standard-library/basic-filebuf-class.md#is_open)합니다.

### <a name="example"></a>예제

`is_open`을 사용하는 방법의 예는 [basic_filebuf::is_open](../standard-library/basic-filebuf-class.md#is_open)을 참조하세요.

## <a name="open"></a>  basic_ifstream::open

파일을 엽니다.

```cpp
void open(
    const char* _Filename,
    ios_base::openmode _Mode = ios_base::in,
    int _Prot = (int)ios_base::_Openprot);

void open(
    const char* _Filename,
    ios_base::openmode _Mode);

void open(
    const wchar_t* _Filename,
    ios_base::openmode _Mode = ios_base::in,
    int _Prot = (int)ios_base::_Openprot);

void open(
    const wchar_t* _Filename,
    ios_base::openmode _Mode);
```

### <a name="parameters"></a>매개 변수

*_Filename*<br/>
열어야 할 파일의 이름입니다.

*모드 (_m)*<br/>
[ios_base::openmode](../standard-library/ios-base-class.md#openmode)의 열거형 중 하나입니다.

*_Prot*<br/>
[_fsopen, _wfsopen](../c-runtime-library/reference/fsopen-wfsopen.md)의 `shflag` 매개 변수와 같은 기본 파일 열기 보호입니다.

### <a name="remarks"></a>설명

멤버 함수는 [rdbuf](#rdbuf) **->** [open](../standard-library/basic-filebuf-class.md#open)(_ *Filename*, `_Mode` &#124; **ios_base::in**)을 호출합니다. 경우 열기에 실패 하면 함수 호출 [setstate](../standard-library/basic-ios-class.md#setstate)(`failbit`)에 ios_base:: failure 예외가 throw 될 수 있습니다.

### <a name="example"></a>예제

참조 [basic_filebuf:: open](../standard-library/basic-filebuf-class.md#open) 사용 하는 예제에 대 한 `open`합니다.

## <a name="op_eq"></a>  basic_ifstream::operator=

이 스트림 개체의 콘텐츠를 할당합니다. 복사본을 남기지 않는 rvalue와 관련된 이동 할당입니다.

```cpp
basic_ifstream& operator=(basic_ifstream&& right);
```

### <a name="parameters"></a>매개 변수

*right*<br/>
`basic_ifstream` 개체에 대한 rvalue 참조입니다.

### <a name="return-value"></a>반환 값

`*this`를 반환합니다.

### <a name="remarks"></a>설명

멤버 연산자의 콘텐츠를 사용 하 여 개체의 내용을 바꿉니다 *오른쪽*는 rvalue 참조로 처리 합니다. 자세한 내용은 [Lvalue 및 Rvalue](../cpp/lvalues-and-rvalues-visual-cpp.md)를 참조하세요.

## <a name="rdbuf"></a>  basic_ifstream::rdbuf

저장된 스트림 버퍼 주소를 반환합니다.

```cpp
basic_filebuf<Elem, Tr> *rdbuf() const
```

### <a name="return-value"></a>반환 값

저장된 스트림 버퍼를 나타내는 [basic_filebuf](../standard-library/basic-filebuf-class.md) 개체에 대한 포인터입니다.

### <a name="example"></a>예제

`rdbuf`의 사용 예제는 [basic_filebuf::close](../standard-library/basic-filebuf-class.md#close)를 참조하세요.

## <a name="swap"></a>  basic_ifstream::swap

두 `basic_ifstream` 개체의 내용을 교환합니다.

```cpp
void swap(basic_ifstream& right);
```

### <a name="parameters"></a>매개 변수

*right*<br/>
다른 스트림 버퍼에 대한 참조입니다.

### <a name="remarks"></a>설명

멤버 함수는 내용에 대해이 개체의 내용을 교환 *오른쪽*합니다.

## <a name="see-also"></a>참고자료

[C++ 표준 라이브러리의 스레드 보안](../standard-library/thread-safety-in-the-cpp-standard-library.md)<br/>
[iostream 프로그래밍](../standard-library/iostream-programming.md)<br/>
[iostreams 규칙](../standard-library/iostreams-conventions.md)<br/>
