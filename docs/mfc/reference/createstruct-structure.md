---
title: CREATESTRUCT 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: reference
f1_keywords:
- CREATESTRUCT
dev_langs:
- C++
helpviewer_keywords:
- CREATESTRUCT structure [MFC]
ms.assetid: 028c7b5e-4fdc-48da-a550-d3e4f9e6cc85
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: db41deda6040121e3d74958f4616a1f3364f6f23
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50064813"
---
# <a name="createstruct-structure"></a>CREATESTRUCT 구조체

`CREATESTRUCT` 구조는 응용 프로그램의 창 프로시저에 전달 된 초기화 매개 변수를 정의 합니다.

## <a name="syntax"></a>구문

```
typedef struct tagCREATESTRUCT {
    LPVOID lpCreateParams;
    HANDLE hInstance;
    HMENU hMenu;
    HWND hwndParent;
    int cy;
    int cx;
    int y;
    int x;
    LONG style;
    LPCSTR lpszName;
    LPCSTR lpszClass;
    DWORD dwExStyle;
} CREATESTRUCT;
```

#### <a name="parameters"></a>매개 변수

*lpCreateParams*<br/>
창을 만들 데 사용할 데이터를 가리킵니다.

*hInstance*<br/>
새 창을 소유 하는 모듈의 모듈 인스턴스 핸들을 식별 합니다.

*hMenu*<br/>
새 창에서 사용할 메뉴를 식별 합니다. 정수 ID를 포함 하는 경우 자식 창에

*hwndParent*<br/>
새 창을 소유 하는 창을 식별 합니다. 이 멤버가 NULL 이면 새 최상위 창입니다.

*cy*<br/>
새 창의 높이 지정합니다.

*cx*<br/>
새 창의 너비를 지정합니다.

*y*<br/>
새 창의 왼쪽된 위 모퉁이의 y 좌표를 지정합니다. 새 창의 자식 창이; 면 부모 창을 기준으로 좌표는 그렇지 않은 좌표는 화면 원점을 기준으로 합니다.

*x*<br/>
새 창의 왼쪽된 위 모퉁이의 x 좌표를 지정합니다. 새 창의 자식 창이; 면 부모 창을 기준으로 좌표는 그렇지 않은 좌표는 화면 원점을 기준으로 합니다.

*style*<br/>
새 창을 지정 [스타일](../../mfc/reference/styles-used-by-mfc.md)합니다.

*lpszName*<br/>
새 창의 이름을 지정 하는 null로 끝나는 문자열을 가리킵니다.

*lpszClass*<br/>
새 창을 Windows 클래스 이름을 지정 하는 null로 끝나는 문자열을 가리키는 (한 [WNDCLASS](https://msdn.microsoft.com/library/windows/desktop/ms633576) 구조체; 자세한 내용은 Windows SDK를 참조 하세요).

*dwExStyle*<br/>
지정 된 [확장 스타일](../../mfc/reference/styles-used-by-mfc.md#extended-window-styles) 새 창에 대 한 합니다.

## <a name="requirements"></a>요구 사항

**헤더:** winuser.h

## <a name="see-also"></a>참고 항목

[구조체, 스타일, 콜백 및 메시지 맵](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)<br/>
[CWnd::OnCreate](../../mfc/reference/cwnd-class.md#oncreate)

