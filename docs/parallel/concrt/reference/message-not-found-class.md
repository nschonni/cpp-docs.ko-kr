---
title: message_not_found 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-concrt
ms.topic: reference
f1_keywords:
- message_not_found
- CONCRT/concurrency::message_not_found
- CONCRT/concurrency::message_not_found::message_not_found
dev_langs:
- C++
helpviewer_keywords:
- message_not_found class
ms.assetid: a96b9995-5ad7-4600-83c8-c15e329ff10e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 5e73a33817ef39d8998173dacc282e6ee9477944
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46445611"
---
# <a name="messagenotfound-class"></a>message_not_found 클래스

이 클래스는 메시징 블록이 요청된 메시지를 찾을 수 없는 경우 발생하는 예외를 설명합니다.

## <a name="syntax"></a>구문

```
class message_not_found : public std::exception;
```

## <a name="members"></a>멤버

### <a name="public-constructors"></a>Public 생성자

|이름|설명|
|----------|-----------------|
|[message_not_found](#ctor)|오버로드됨. `message_not_found` 개체를 생성합니다.|

## <a name="inheritance-hierarchy"></a>상속 계층

`exception`

`message_not_found`

## <a name="requirements"></a>요구 사항

**헤더:** concrt.h

**네임스페이스:** 동시성

##  <a name="ctor"></a> message_not_found

`message_not_found` 개체를 생성합니다.

```
explicit _CRTIMP message_not_found(_In_z_ const char* _Message) throw();

message_not_found() throw();
```

### <a name="parameters"></a>매개 변수

*메시지 (_m)*<br/>
오류 설명 메시지입니다.

## <a name="see-also"></a>참고 항목

[concurrency 네임스페이스](concurrency-namespace.md)<br/>
[비동기 메시지 블록](../../../parallel/concrt/asynchronous-message-blocks.md)

