---
title: AsWeak 함수 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- client/Microsoft::WRL::AsWeak
dev_langs:
- C++
helpviewer_keywords:
- AsWeak function
ms.assetid: a6f10cfc-c1d6-4761-adb9-1a119cc99913
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: dfd626a3e0ca1866f6db046554220c6e631c18b4
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46394311"
---
# <a name="asweak-function"></a>AsWeak 함수

지정된 인스턴스에 대한 약한 참조를 가져옵니다.

## <a name="syntax"></a>구문

```cpp
template<typename T>
HRESULT AsWeak(
   _In_ T* p,
   _Out_ WeakRef* pWeak
);
```

### <a name="parameters"></a>매개 변수

*T*<br/>
매개 변수의 형식에 대 한 포인터 *p*합니다.

*p*<br/>
형식의 인스턴스입니다.

*pWeak*<br/>
이 작업이 완료 되 면 매개 변수에 대 한 약한 참조에 대 한 포인터 *p*합니다.

## <a name="return-value"></a>반환 값

이 작업에 성공 하면 S_OK 그렇지 않으면 실패의 원인을 나타내는 HRESULT 오류가 발생 합니다.

## <a name="requirements"></a>요구 사항

**헤더:** client.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[Microsoft::WRL 네임스페이스](../windows/microsoft-wrl-namespace.md)