---
title: MSG 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: reference
f1_keywords:
- MSG
dev_langs:
- C++
helpviewer_keywords:
- MSG structure [MFC]
ms.assetid: dc166d27-9423-41f1-9599-5ba76d2f0138
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 2b2f58af3bcf3eef524b95d25579e5bc233f9108
ms.sourcegitcommit: 3f4e92266737ecb70507871e87dc8e2965ad7e04
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/15/2018
ms.locfileid: "49334566"
---
# <a name="msg-structure"></a>MSG 구조체

`MSG` 구조 스레드의 메시지 큐에서 메시지 정보를 포함 합니다.

## <a name="syntax"></a>구문

```
typedef struct tagMSG {     // msg
    HWND hwnd;
    UINT message;
    WPARAM wParam;
    LPARAM lParam;
    DWORD time;
    POINT pt;
} MSG;
```

#### <a name="parameters"></a>매개 변수

*hwnd*<br/>
창 메시지를 수신 하는 창 프로시저를 식별 합니다.

*message*<br/>
메시지 번호를 지정합니다.

*wParam*<br/>
메시지에 대 한 추가 정보를 지정합니다. 값에 따라 정확한 의미는 `message` 멤버입니다.

*lParam*<br/>
메시지에 대 한 추가 정보를 지정합니다. 값에 따라 정확한 의미는 `message` 멤버입니다.

*time*<br/>
메시지가 게시 된 시간을 지정 합니다.

*(태평양 표준시)*<br/>
메시지가 게시 될 때 화면 좌표에서 커서 위치를 지정 합니다.

## <a name="requirements"></a>요구 사항

**헤더:** winuser.h

## <a name="see-also"></a>참고 항목

[구조체, 스타일, 콜백 및 메시지 맵](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)

