---
title: __raise | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- __raise
- __raise_cpp
dev_langs:
- C++
helpviewer_keywords:
- __raise keyword [C++]
ms.assetid: 6f1ae418-5f0f-48b6-9f6e-8ea7e66b239a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: abe0c1a2e443e88879cd7005d944acfcacc3c17d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46031472"
---
# <a name="raise"></a>__raise

이벤트의 호출 사이트를 강조합니다.

## <a name="syntax"></a>구문

```
__raise method-declarator;
```

## <a name="remarks"></a>설명

관리 코드에서 이벤트가 정의된 클래스 내에서만 이벤트를 발생시킬 수 있습니다. 참조 [이벤트](../windows/event-cpp-component-extensions.md) 자세한 내용은 합니다.

키워드 **__raise** 이벤트가 호출 하는 경우 내보낼 오류가 발생 합니다.

> [!NOTE]
>  템플릿 기반 클래스 또는 구조체에 event를 포함시킬 수 없습니다.

## <a name="example"></a>예제

```cpp
// EventHandlingRef_raise.cpp
struct E {
   __event void func1();
   void func1(int) {}

   void func2() {}

   void b() {
      __raise func1();
      __raise func1(1);  // C3745: 'int Event::bar(int)':
                         // only an event can be 'raised'
      __raise func2();   // C3745
   }
};

int main() {
   E e;
   __raise e.func1();
   __raise e.func1(1);  // C3745
   __raise e.func2();   // C3745
}
```

## <a name="see-also"></a>참고자료

[키워드](../cpp/keywords-cpp.md)<br/>
[이벤트 처리](../cpp/event-handling.md)<br/>
[런타임 플랫폼용 구성 요소 확장](../windows/component-extensions-for-runtime-platforms.md)