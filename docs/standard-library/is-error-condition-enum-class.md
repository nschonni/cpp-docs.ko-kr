---
title: is_error_condition_enum 클래스 | Microsoft 문서
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
f1_keywords:
- system_error/std::is_error_condition_enum
dev_langs:
- C++
helpviewer_keywords:
- is_error_condition_enum class
ms.assetid: 752bb87a-c61c-4304-9254-5aaf228b59c0
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 01650db9c1aec141852f66a2f4e2f09f5d5e78ac
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/07/2018
ms.locfileid: "33842302"
---
# <a name="iserrorconditionenum-class"></a>is_error_condition_enum 클래스

[error_condition](../standard-library/error-condition-class.md) 열거형을 테스트하는 형식 조건자를 나타냅니다.

## <a name="syntax"></a>구문

```cpp
template <_Enum>
class is_error_condition_enum;
```

## <a name="remarks"></a>설명

이 [형식 조건자](../standard-library/type-traits.md)의 인스턴스는 `_Enum` 형식이 `error_condition` 형식의 개체에 저장하는 데 적합한 열거형 값이면 true입니다.

사용자 정의 형식의 경우 이 형식에 특수화를 추가할 수 있습니다.

## <a name="requirements"></a>요구 사항

**헤더:** \<system_error>

**네임스페이스:** std

## <a name="see-also"></a>참고자료

[<type_traits>](../standard-library/type-traits.md)<br/>
[<system_error>](../standard-library/system-error.md)<br/>
