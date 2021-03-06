---
title: is_trivially_default_constructible 클래스 | Microsoft 문서
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
f1_keywords:
- type_traits/std::is_trivially_default_constructible
dev_langs:
- C++
helpviewer_keywords:
- is_trivially_default_constructible
ms.assetid: 653ecd73-909f-4dd8-b95a-d1164d1c2da4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 73bdd8186f2ce56e4a6ecec0fa4f9468d9da8e8c
ms.sourcegitcommit: 761c5f7c506915f5a62ef3847714f43e9b815352
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44102709"
---
# <a name="istriviallydefaultconstructible-class"></a>is_trivially_default_constructible 클래스

형식에 Trivial 기본 생성자가 있는지 여부를 테스트합니다.

## <a name="syntax"></a>구문

```cpp
template <class Ty>
struct is_trivially_default_constructible;
```

### <a name="parameters"></a>매개 변수

*Ty*<br/>
형식이 쿼리입니다.

## <a name="remarks"></a>설명

형식 조건자의 인스턴스 형태인 경우 true 형식을 *Ty* 는 클래스에 trivial 생성자가 있는 그렇지 않으면 false입니다.

클래스에 대 한 기본 생성자 *Ty* 간단 하는 경우:

- 암시적으로 선언된 기본 생성자인 경우

- 클래스 *Ty* 에 가상 함수가 없는

- 클래스 *Ty* 에 없는 가상 기본

- 모든 직접 기본 클래스의 *Ty* trivial 생성자가 있는 경우

- 클래스 형식의 모든 비정적 데이터 멤버의 클래스에 Trivial 생성자가 있는 경우

- 클래스 배열 형식의 모든 비정적 데이터 멤버의 클래스에 Trivial 생성자가 있는 경우

## <a name="requirements"></a>요구 사항

**헤더:** \<type_traits>

**네임스페이스:** std

## <a name="see-also"></a>참고자료

[<type_traits>](../standard-library/type-traits.md)<br/>
