---
title: Make 함수 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::Make
dev_langs:
- C++
helpviewer_keywords:
- Make function
ms.assetid: 66704143-df99-4a95-904d-ed99607e1034
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: a8b02b51dca4ae3712274b2b011c1967e5006637
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46422404"
---
# <a name="make-function"></a>Make 함수

지정된 된 Windows 런타임 클래스를 초기화합니다. 이 함수를 사용 하 여 동일한 모듈에 정의 된 구성 요소를 인스턴스화합니다.

## <a name="syntax"></a>구문

```cpp
template <
   typename T,
   typename TArg1,
   typename TArg2,
   typename TArg3,
   typename TArg4,
   typename TArg5,
   typename TArg6,
   typename TArg7,
   typename TArg8,
   typename TArg9
>
ComPtr<T> Make(
   TArg1 &&arg1,
   TArg2 &&arg2,
   TArg3 &&arg3,
   TArg4 &&arg4,
   TArg5 &&arg5,
   TArg6 &&arg6,
   TArg7 &&arg7,
   TArg8 &&arg8,
   TArg9 &&arg9
);
template <
   typename T,
   typename TArg1,
   typename TArg2,
   typename TArg3,
   typename TArg4,
   typename TArg5,
   typename TArg6,
   typename TArg7,
   typename TArg8
>
ComPtr<T> Make(
   TArg1 &&arg1,
   TArg2 &&arg2,
   TArg3 &&arg3,
   TArg4 &&arg4,
   TArg5 &&arg5,
   TArg6 &&arg6,
   TArg7 &&arg7,
   TArg8 &&arg8
);
template <
   typename T,
   typename TArg1,
   typename TArg2,
   typename TArg3,
   typename TArg4,
   typename TArg5,
   typename TArg6,
   typename TArg7
>
ComPtr<T> Make(
   TArg1 &&arg1,
   TArg2 &&arg2,
   TArg3 &&arg3,
   TArg4 &&arg4,
   TArg5 &&arg5,
   TArg6 &&arg6,
   TArg7 &&arg7
);
template <
   typename T,
   typename TArg1,
   typename TArg2,
   typename TArg3,
   typename TArg4,
   typename TArg5,
   typename TArg6
>
ComPtr<T> Make(
   TArg1 &&arg1,
   TArg2 &&arg2,
   TArg3 &&arg3,
   TArg4 &&arg4,
   TArg5 &&arg5,
   TArg6 &&arg6
);
template <
   typename T,
   typename TArg1,
   typename TArg2,
   typename TArg3,
   typename TArg4,
   typename TArg5
>
ComPtr<T> Make(
   TArg1 &&arg1,
   TArg2 &&arg2,
   TArg3 &&arg3,
   TArg4 &&arg4,
   TArg5 &&arg5
);
template <
   typename T,
   typename TArg1,
   typename TArg2,
   typename TArg3,
   typename TArg4
>
ComPtr<T> Make(
   TArg1 &&arg1,
   TArg2 &&arg2,
   TArg3 &&arg3,
   TArg4 &&arg4
);
template <
   typename T,
   typename TArg1,
   typename TArg2,
   typename TArg3
>
ComPtr<T> Make(
   TArg1 &&arg1,
   TArg2 &&arg2,
   TArg3 &&arg3
);
template <
   typename T,
   typename TArg1,
   typename TArg2
>
ComPtr<T> Make(
   TArg1 &&arg1,
   TArg2 &&arg2
);
template <
   typename T,
   typename TArg1
>
ComPtr<T> Make(
   TArg1 &&arg1
);
template <
   typename T
>
ComPtr<T> Make();
```

### <a name="parameters"></a>매개 변수

*T*<br/>
사용자 지정 클래스에서 상속 되는 `WRL::RuntimeClass`합니다.

*TArg1*<br/>
지정된 된 런타임 클래스에 전달 되는 인수 1의 형식입니다.

*TArg2*<br/>
지정된 된 런타임 클래스에 전달 되는 2 인수 형식입니다.

*TArg3*<br/>
지정된 된 런타임 클래스에 전달 되는 3 번째 인수의 형식입니다.

*TArg4*<br/>
지정된 된 런타임 클래스에 전달 되는 4 번째 인수의 형식입니다.

*TArg5*<br/>
지정된 된 런타임 클래스에 전달 되는 5 번째 인수의 형식입니다.

*TArg6*<br/>
지정된 된 런타임 클래스에 전달 되는 6 번째 인수의 형식입니다.

*TArg7*<br/>
지정된 된 런타임 클래스에 전달 되는 7 번째 인수의 형식입니다.

*TArg8*<br/>
지정된 된 런타임 클래스에 전달 되는 8 번째 인수의 형식입니다.

*TArg9*<br/>
지정된 된 런타임 클래스에 전달 되는 9 번째 인수의 형식입니다.

*arg1*<br/>
인수 1 지정된 된 런타임 클래스에 전달 되는입니다.

*Arg2*<br/>
인수 2 지정된 된 런타임 클래스에 전달 되는입니다.

*arg3*<br/>
인수 3 지정된 된 런타임 클래스에 전달 되는입니다.

*arg4*<br/>
인수 4 지정된 된 런타임 클래스에 전달 되는입니다.

*arg5*<br/>
인수 5 지정된 된 런타임 클래스에 전달 되는입니다.

*a r g 6*<br/>
인수 6 지정된 된 런타임 클래스에 전달 되는입니다.

*arg7*<br/>
7 전달 된 인수를 지정 된 런타임 클래스입니다.

*arg8*<br/>
8 전달 된 인수를 지정 된 런타임 클래스입니다.

*arg9*<br/>
9 전달 된 인수를 지정 된 런타임 클래스입니다.

## <a name="return-value"></a>반환 값

A `ComPtr<T>` 개체가 고, 그렇지 않으면 성공적인 **nullptr**합니다.

## <a name="remarks"></a>설명

참조 [방법: 직접 WRL 구성 요소 인스턴스화](../windows/how-to-instantiate-wrl-components-directly.md) 이 함수 간의 차이점을 알아보려면 및 [Microsoft::WRL::Details::MakeAndInitialize](../windows/makeandinitialize-function.md), 및 예제입니다.

## <a name="requirements"></a>요구 사항

**헤더:** implements.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[Microsoft::WRL 네임스페이스](../windows/microsoft-wrl-namespace.md)