---
title: "CDialogEx 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CDialogEx
- AFXDIALOGEX/CDialogEx
- AFXDIALOGEX/CDialogEx::CDialogEx
- AFXDIALOGEX/CDialogEx::SetBackgroundColor
- AFXDIALOGEX/CDialogEx::SetBackgroundImage
dev_langs:
- C++
helpviewer_keywords:
- CDialogEx class
- CDialogEx::PreTranslateMessage method
ms.assetid: a6ed3b1f-aef8-4b66-ac78-2160faf63c13
caps.latest.revision: 27
author: mikeblome
ms.author: mblome
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
translationtype: Machine Translation
ms.sourcegitcommit: 040985df34f2613b4e4fae29498721aef15d50cb
ms.openlocfilehash: c12aa0152fdbf83e423b944a0100045962ddb704
ms.lasthandoff: 02/24/2017

---
# <a name="cdialogex-class"></a>CDialogEx 클래스
`CDialogEx` 클래스는 대화 상자의 배경 색과 배경 이미지를 지정합니다.  
  
## <a name="syntax"></a>구문  
  
```  
class CDialogEx : public CDialog  
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[CDialogEx::CDialogEx](#cdialogex)|`CDialogEx` 개체를 생성합니다.|  
|`CDialogEx::~CDialogEx`|소멸자|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[CDialogEx::SetBackgroundColor](#setbackgroundcolor)|대화 상자의 배경 색을 설정합니다.|  
|[CDialogEx::SetBackgroundImage](#setbackgroundimage)|대화 상자의 배경 이미지를 설정합니다.|  
  
## <a name="remarks"></a>주의  
 `CDialogEx` 클래스를 사용하려면 `CDialogEx` 클래스 대신 `CDialog` 클래스에서 대화 상자 클래스를 파생합니다.  
  
 대화 상자 이미지는 리소스 파일에 저장됩니다. 프레임워크는 리소스 파일에서 로드되는 모든 이미지를 자동으로 삭제합니다. 현재 배경 이미지를 프로그래밍 방식으로 삭제 하려면 호출의 [CDialogEx::SetBackgroundImage](#setbackgroundimage) 메서드 또는 구현 된 `OnDestroy` 이벤트 처리기입니다. 호출 하는 경우는 [CDialogEx::SetBackgroundImage](#setbackgroundimage) 메서드를 한 `HBITMAP` 이미지 핸들로 매개 변수입니다. `CDialogEx` 개체가 이미지의 소유권을 갖게 되며 `m_bAutoDestroyBmp` 플래그가 `TRUE`이면 삭제합니다.  
  
 A `CDialogEx` 개체의 부모가 될 수는 [CMFCPopupMenu 클래스](../../mfc/reference/cmfcpopupmenu-class.md) 개체입니다. [CMFCPopupMenu 클래스](../../mfc/reference/cmfcpopupmenu-class.md) 호출 개체는 `CDialogEx::SetActiveMenu` 메서드 때는 [CMFCPopupMenu 클래스](../../mfc/reference/cmfcpopupmenu-class.md) 개체가 열려 있습니다. 나중에 `CDialogEx` 개체가 처리 될 때까지 모든 메뉴 이벤트는 [CMFCPopupMenu 클래스](../../mfc/reference/cmfcpopupmenu-class.md) 개체가 닫혀 있습니다.  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CCmdTarget](../../mfc/reference/ccmdtarget-class.md)  
  
 [CWnd](../../mfc/reference/cwnd-class.md)  
  
 [CDialog](../../mfc/reference/cdialog-class.md)  
  
 [CDialogEx](../../mfc/reference/cdialogex-class.md)  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** afxdialogex.h  
  
##  <a name="cdialogex"></a>CDialogEx::CDialogEx  
 `CDialogEx` 개체를 생성합니다.  
  
```  
CDialogEx(
    UINT nIDTemplate,  
    CWnd* pParent=NULL);

 
CDialogEx(
    LPCTSTR lpszTemplateName,  
    CWnd* pParentWnd=NULL);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nIDTemplate`  
 대화 상자 템플릿 리소스 ID입니다.  
  
 [in] `lpszTemplateName`  
 대화 상자 템플릿 리소스 이름입니다.  
  
 [in] `pParent`  
 부모 창에 대 한 포인터입니다. 기본값은 `NULL`입니다.  
  
 [in] `pParentWnd`  
 부모 창에 대 한 포인터입니다. 기본값은 `NULL`입니다.  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="setbackgroundcolor"></a>CDialogEx::SetBackgroundColor  
 대화 상자의 배경 색을 설정합니다.  
  
```  
void SetBackgroundColor(
    COLORREF color,  
    BOOL bRepaint=TRUE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `color`  
 RGB 색상 값입니다.  
  
 [in] `bRepaint`  
 `TRUE`즉시; 화면을 업데이트 하려면 그렇지 않으면 `FALSE`합니다. 기본값은 `TRUE`입니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="setbackgroundimage"></a>CDialogEx::SetBackgroundImage  
 대화 상자의 배경 이미지를 설정합니다.  
  
```  
void SetBackgroundImage(
    HBITMAP hBitmap,  
    BackgroundLocation location=BACKGR_TILE,  
    BOOL bAutoDestroy=TRUE,  
    BOOL bRepaint=TRUE);

 
BOOL SetBackgroundImage(
    UINT uiBmpResId,  
    BackgroundLocation location=BACKGR_TILE,  
    BOOL bRepaint=TRUE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `hBitmap`  
 배경 이미지에 대 한 핸들입니다.  
  
 [in] `uiBmpResId`  
 배경 이미지의 리소스 ID입니다.  
  
 [in] `location`  
 중 하나는 `CDialogEx::BackgroundLocation` 이미지의 위치를 지정 하는 값입니다. 유효한 값에는 BACKGR_TILE, BACKGR_TOPLEFT, BACKGR_TOPRIGHT, BACKGR_BOTTOMLEFT, 및 BACKGR_BOTTOMRIGHT 포함 됩니다. 기본값은 BACKGR_TILE 합니다.  
  
 [in] `bAutoDestroy`  
 `TRUE`배경 이미지를 자동으로 삭제 하려면 그렇지 않으면 `FALSE`합니다.  
  
 [in] `bRepaint`  
 `TRUE`대화 상자;을 즉시 다시 그리게 그렇지 않으면 `FALSE`합니다.  
  
### <a name="return-value"></a>반환 값  
 오버 로드 구문, 두 번째 방법은 `TRUE` 방법이 고, 그렇지 않으면 경우 `FALSE`합니다.  
  
### <a name="remarks"></a>주의  
 대화 상자의 클라이언트 영역에 맞게 지정 하는 이미지 늘어나지 않습니다.  
  
## <a name="see-also"></a>참고 항목  
 [계층 구조 차트](../../mfc/hierarchy-chart.md)   
 [클래스](../../mfc/reference/mfc-classes.md)   
 [CMFCPopupMenu 클래스](../../mfc/reference/cmfcpopupmenu-class.md)   
 [CContextMenuManager 클래스](../../mfc/reference/ccontextmenumanager-class.md)
