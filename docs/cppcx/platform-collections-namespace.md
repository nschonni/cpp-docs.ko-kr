---
title: 'Platform:: collections Namespace | Microsoft Docs'
ms.custom: ''
ms.date: 01/18/2018
ms.technology: cpp-windows
ms.topic: reference
f1_keywords:
- collection/Platform::Collections
dev_langs:
- C++
helpviewer_keywords:
- Platform::Collections Namespace
ms.assetid: b5042864-5f22-40b7-b7a5-c0691f65cc47
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 0a8c6191f8cbcf79973a5af55d222dd6f17fc47e
ms.sourcegitcommit: 761c5f7c506915f5a62ef3847714f43e9b815352
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44106072"
---
# <a name="platformcollections-namespace"></a>Platform::Collections 네임스페이스

Platform:: collections 네임 스페이스를 포함 합니다 `Map`, `MapView`를 `Vector`, 및 `VectorView` 클래스입니다. 이러한 클래스에 정의 된 해당 인터페이스의 구체적 구현 되는 [Windows::Foundation::Collections](/uwp/api/Windows.Foundation.Collections) 네임 스페이스입니다. 구체적인 컬렉션 형식은 ABI를 통해 이식할 수 없습니다. Javascript 또는 C# 프로그램이 C++ 구성 요소를 호출하는 경우를 예로 들 수 있습니다. 그러나 구체적인 컬렉션 형식을 해당 인터페이스 형식으로 암시적으로 변환할 수는 있습니다. 예를 들어 채우고 컬렉션을 반환 하는 공용 메서드를 구현 하는 경우 다음 사용 하 여 [Platform::Collections::Vector](../cppcx/platform-collections-vector-class.md) 내부적으로 컬렉션을 구현 하 고 사용 [Windows::Foundation::Collections: : IVector](/uwp/api/Windows.Foundation.Collections.IVector_T_) 반환 형식으로 합니다. 자세한 내용은 [컬렉션](../cppcx/collections-c-cx.md) 하 고 [Creating Windows Runtime Components in c + +](/windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp)합니다.

Platform::Collections::Vector는 [std::vector](../standard-library/vector-class.md) 에서 [Platform::Collections::Map](../cppcx/platform-collections-map-class.md) 은 [std::map](../standard-library/map-class.md)에서 작성할 수 있습니다.

Platform:: collections 네임 스페이스 삽입 및 입력된 반복기에 대 한 지원에 제공 하는 또한 및 `Vector` 고 `VectorView` 반복기입니다.

포함 해야 합니다 (`#include`) platform:: collections 네임 스페이스의 형식을 사용 하려면 collection.h 헤더입니다.

## <a name="syntax"></a>구문

```cpp
#include <collection.h>
using namespace Platform::Collections;
```

### <a name="members"></a>멤버

이 네임스페이스에는 다음 멤버가 포함되어 있습니다.

|이름|설명|
|----------|-----------------|
|[Platform::Collections::BackInsertIterator 클래스](../cppcx/platform-collections-backinsertiterator-class.md)|컬렉션 끝 부분에 요소를 삽입하는 반복기를 나타냅니다.|
|[Platform::Collections::InputIterator 클래스](../cppcx/platform-collections-inputiterator-class.md)|컬렉션 시작 부분에 요소를 삽입하는 반복기를 나타냅니다.|
|[Platform::Collections::Map 클래스](../cppcx/platform-collections-map-class.md)|키에서 액세스할 수 있는 키/값 쌍의 수정 가능한 컬렉션을 나타냅니다. [std::map](../standard-library/map-class.md)과 비슷합니다.|
|[Platform::Collections::MapView 클래스](../cppcx/platform-collections-mapview-class.md)|키에서 액세스할 수 있는 키/값 쌍의 읽기 전용 컬렉션을 나타냅니다.|
|[Platform::Collections::Vector Class](../cppcx/platform-collections-vector-class.md)|요소의 수정 가능한 시퀀스를 나타냅니다. [std::vector](../standard-library/vector-class.md)과 비슷합니다.|
|[Platform::Collections::VectorIterator 클래스](../cppcx/platform-collections-vectoriterator-class.md)|`Vector` 컬렉션을 트래버스하는 반복기를 나타냅니다.|
|[Platform::Collections::VectorView 클래스](../cppcx/platform-collections-vectorview-class.md)|요소의 읽기 전용 시퀀스를 나타냅니다.|
|[Platform::Collections::VectorViewIterator 클래스](../cppcx/platform-collections-vectorviewiterator-class.md)|`VectorView` 컬렉션을 트래버스하는 반복기를 나타냅니다.|

## <a name="inheritance-hierarchy"></a>상속 계층

[Platform 네임 스페이스](../cppcx/platform-namespace-c-cx.md)

### <a name="requirements"></a>요구 사항

**메타데이터:** platform.winmd

**네임스페이스:** Platform::Collections

**컴파일러 옵션:** /ZW

## <a name="see-also"></a>참고자료

[플랫폼 Namespace](../cppcx/platform-namespace-c-cx.md)
