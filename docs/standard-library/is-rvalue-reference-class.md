---
title: is_rvalue_reference 클래스 | Microsoft 문서
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
f1_keywords:
- type_traits/std::is_rvalue_reference
dev_langs:
- C++
helpviewer_keywords:
- is_rvalue_reference class
- is_rvalue_reference
ms.assetid: 40a97072-7b5c-4274-9154-298d3dcf064a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6bbaa215335a299eee8971b113fdcf3860e9b740
ms.sourcegitcommit: 761c5f7c506915f5a62ef3847714f43e9b815352
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44106498"
---
# <a name="isrvaluereference-class"></a>is_rvalue_reference 클래스

형식이 rvalue 참조인지 테스트합니다.

## <a name="syntax"></a>구문

```cpp
template <class Ty>
struct is_rvalue_reference;
```

### <a name="parameters"></a>매개 변수

*Ty*<br/>
형식이 쿼리입니다.

## <a name="remarks"></a>설명

이 형식 조건자의 인스턴스 형태인 경우 true 형식을 *Ty* 되는 [rvalue 참조](../cpp/rvalue-reference-declarator-amp-amp.md)합니다.

## <a name="requirements"></a>요구 사항

**헤더:** \<type_traits>

**네임스페이스:** std

## <a name="see-also"></a>참고자료

[<type_traits>](../standard-library/type-traits.md)<br/>
[Lvalue 및 Rvalue](../cpp/lvalues-and-rvalues-visual-cpp.md)<br/>
