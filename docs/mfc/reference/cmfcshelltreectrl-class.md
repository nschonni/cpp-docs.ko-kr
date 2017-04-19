---
title: "CMFCShellTreeCtrl 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CMFCShellTreeCtrl
- AFXSHELLTREECTRL/CMFCShellTreeCtrl
- AFXSHELLTREECTRL/CMFCShellTreeCtrl::EnableShellContextMenu
- AFXSHELLTREECTRL/CMFCShellTreeCtrl::GetFlags
- AFXSHELLTREECTRL/CMFCShellTreeCtrl::GetItemPath
- AFXSHELLTREECTRL/CMFCShellTreeCtrl::GetRelatedList
- AFXSHELLTREECTRL/CMFCShellTreeCtrl::OnChildNotify
- AFXSHELLTREECTRL/CMFCShellTreeCtrl::OnGetItemIcon
- AFXSHELLTREECTRL/CMFCShellTreeCtrl::OnGetItemText
- AFXSHELLTREECTRL/CMFCShellTreeCtrl::Refresh
- AFXSHELLTREECTRL/CMFCShellTreeCtrl::SelectPath
- AFXSHELLTREECTRL/CMFCShellTreeCtrl::SetFlags
- AFXSHELLTREECTRL/CMFCShellTreeCtrl::SetRelatedList
dev_langs:
- C++
helpviewer_keywords:
- CMFCShellTreeCtrl class
ms.assetid: 3d1da715-9554-4ed7-968c-055c48146267
caps.latest.revision: 30
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
ms.sourcegitcommit: 0e0c08ddc57d437c51872b5186ae3fc983bb0199
ms.openlocfilehash: cf9c7c3577646895546c443c975a92431194d3f4
ms.lasthandoff: 02/24/2017

---
# <a name="cmfcshelltreectrl-class"></a>CMFCShellTreeCtrl 클래스
`CMFCShellTreeCtrl` 클래스 확장 [CTreeCtrl 클래스](../../mfc/reference/ctreectrl-class.md) 셸 항목의 계층 구조를 표시 하 여 기능 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
class CMFCShellTreeCtrl : public CTreeCtrl  
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[CMFCShellTreeCtrl::EnableShellContextMenu](#enableshellcontextmenu)|바로 가기 메뉴를 사용 하지 않도록 설정 하거나 사용 합니다.|  
|[CMFCShellTreeCtrl::GetFlags](#getflags)|에 전달 되는 플래그의 조합을 반환 [IShellFolder::EnumObjects](http://msdn.microsoft.com/library/windows/desktop/bb775066)합니다.|  
|[CMFCShellTreeCtrl::GetItemPath](#getitempath)|항목에 대 한 경로 검색합니다.|  
|[CMFCShellTreeCtrl::GetRelatedList](#getrelatedlist)|에 대 한 포인터를 반환 된 [CMFCShellListCtrl 클래스](../../mfc/reference/cmfcshelllistctrl-class.md) 이 함께 사용 되는 개체 `CMFCShellTreeCtrl` 개체 탐색기와 유사한 창을 만들 수 있습니다.|  
|[CMFCShellTreeCtrl::OnChildNotify](#onchildnotify)|이 멤버 함수는이 창에 적용 되는 알림 메시지를 받을 때이 창의 부모 창에서 호출 됩니다. (재정의 [cwnd:: Onchildnotify](../../mfc/reference/cwnd-class.md#onchildnotify).)|  
|[CMFCShellTreeCtrl::OnGetItemIcon](#ongetitemicon)||  
|[CMFCShellTreeCtrl::OnGetItemText](#ongetitemtext)||  
|[CMFCShellTreeCtrl::Refresh](#refresh)|현재 다시 표시를 새로 고치고 `CMFCShellTreeCtrl` 개체입니다.|  
|[CMFCShellTreeCtrl::SelectPath](#selectpath)|제공 된 PIDL 또는 문자열 경로에 따라 적절 한 트리 컨트롤 항목을 선택 합니다.|  
|[CMFCShellTreeCtrl::SetFlags](#setflags)|트리 컨텍스트를 필터링 하는 플래그를 설정 (사용 하는 플래그와 유사한 `IShellFolder::EnumObjects`).|  
|[CMFCShellTreeCtrl::SetRelatedList](#setrelatedlist)|현재 간에 관계를 설정 하는 `CMFCShellTreeCtrl` 개체 및 `CMFCShellListCtrl` 개체입니다.|  
  
## <a name="remarks"></a>주의  
 이 클래스 확장은 `CTreeCtrl` 트리에서 Windows 셸 항목을 포함 하 여 프로그램을 사용 하 여 클래스입니다. 이 클래스와 연결 될 수는 `CMFCShellListCtrl` 개체 전체 탐색기 창을 만들 수 있습니다. 그런 다음 트리에서 항목을 선택 하면 관련된 목록에 Windows 셸 항목의 목록이 표시 됩니다.  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CCmdTarget](../../mfc/reference/ccmdtarget-class.md)  
  
 [CWnd](../../mfc/reference/cwnd-class.md)  
  
 [CTreeCtrl](../../mfc/reference/ctreectrl-class.md)  
  
 `CMFCShellTreeCtrl`  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** afxshelltreeCtrl.h  
  
## <a name="example"></a>예제  
 다음 예제에서는 `CMFCShellTreeCtrl` 클래스의 개체를 만드는 방법을 보여 줍니다. 이 코드 조각은의 일부인는 [탐색기 샘플](../../visual-cpp-samples.md)합니다.  
  
 [!code-cpp[NVC_MFC_Explorer #&4;](../../mfc/reference/codesnippet/cpp/cmfcshelltreectrl-class_1.h)]  
[!code-cpp[NVC_MFC_Explorer #&5;](../../mfc/reference/codesnippet/cpp/cmfcshelltreectrl-class_2.cpp)]  
  
##  <a name="enableshellcontextmenu"></a>CMFCShellTreeCtrl::EnableShellContextMenu  
 바로 가기 메뉴를 수 있습니다.  
  
```  
void EnableShellContextMenu(BOOL bEnable = TRUE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bEnable`  
 바로 가기 메뉴를 사용 하도록 설정할지 여부를 지정 하는 부울입니다.  
  
##  <a name="getflags"></a>CMFCShellTreeCtrl::GetFlags  
 설정에 대 한 플래그를 반환 하는 [CMFCShellTreeCtrl 클래스](../../mfc/reference/cmfcshelltreectrl-class.md) 개체입니다.  
  
```  
DWORD GetFlags() const;  
```  
  
### <a name="return-value"></a>반환 값  
 A `DWORD` 현재 플래그의 조합을 지정 하는 값을 설정 합니다.  
  
### <a name="remarks"></a>주의  
 설정 된 플래그는 `CMFCShellTreeCtrl` 메서드에 보내집니다 [IShellFolder::EnumObjects](http://msdn.microsoft.com/library/windows/desktop/bb775066) 개체를 새로 고칠 때마다 합니다. 플래그를 변경할 수는 [CMFCShellTreeCtrl::SetFlags](#setflags) 메서드.  
  
##  <a name="getitempath"></a>CMFCShellTreeCtrl::GetItemPath  
 에 있는 항목의 경로 검색 된 [CMFCShellTreeCtrl 클래스](../../mfc/reference/cmfcshelltreectrl-class.md) 개체입니다.  
  
```  
BOOL GetItemPath(
    CString& strPath,  
    HTREEITEM htreeItem = NULL) const;  
```  
  
### <a name="parameters"></a>매개 변수  
 [out] `strPath`  
 문자열 매개 변수에 대 한 참조입니다. 메서드는이 매개 변수를 항목의 경로 씁니다.  
  
 [in] `htreeItem`  
 메서드는이 트리 컨트롤 항목에 대 한 경로 검색합니다.  
  
### <a name="return-value"></a>반환 값  
 성공 하면 0이 아니고 그렇지 않으면 0입니다.  
  
### <a name="remarks"></a>주의  
 이 방법이 실패 하면, `strPath` 빈 문자열이 포함 되어 있습니다.  
  
 지정 하지 않으면 `hTreeItem`,이 메서드는 현재 선택한 항목에 대 한 문자열을 얻을 하려고 합니다. 선택 된 항목이 없는 경우 및 `hTreeItem` 는 `NULL`,이 메서드는 실패 합니다.  
  
##  <a name="getrelatedlist"></a>CMFCShellTreeCtrl::GetRelatedList  
 에 대 한 포인터를 반환 된 [CMFCShellListCtrl 클래스](../../mfc/reference/cmfcshelllistctrl-class.md) 이 연관 된 개체 [CMFCShellTreeCtrl](../../mfc/reference/cmfcshelltreectrl-class.md) 개체입니다.  
  
```  
CMFCShellListCtrl* GetRelatedList() const;  
```  
  
### <a name="return-value"></a>반환 값  
 에 대 한 포인터는 `CMFCShellListCtrl` 이 트리 컨트롤 개체와 연결 된 개체입니다.  
  
### <a name="remarks"></a>주의  
 사용 하 여 한 `CMFCShellListCtrl` 와 함께 개체는 `CMFCShellTreeCtrl` 개체 탐색기와 유사한 창을 만들 수 있습니다. 메서드를 사용 하 여 [CMFCShellTreeCtrl::SetRelatedList](#setrelatedlist) 두 클래스를 연결 합니다. 프레임 워크를 자동으로 업데이트 연결 후는 `CMFCShellListCtrl` 경우의 선택은 `CMFCShellTreeCtrl` 변경 합니다.  
  
##  <a name="onchildnotify"></a>CMFCShellTreeCtrl::OnChildNotify  
 [!INCLUDE[cpp_fp_under_construction](../../mfc/reference/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual BOOL OnChildNotify(
    UINT message,  
    WPARAM wParam,  
    LPARAM lParam,  
    LRESULT* pLResult);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `message`  
 [in] `wParam`  
 [in] `lParam`  
 [in] `pLResult`  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="ongetitemicon"></a>CMFCShellTreeCtrl::OnGetItemIcon  
 [!INCLUDE[cpp_fp_under_construction](../../mfc/reference/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual int OnGetItemIcon(
    LPAFX_SHELLITEMINFO pItem,  
    BOOL bSelected);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pItem`  
 [in] `bSelected`  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="ongetitemtext"></a>CMFCShellTreeCtrl::OnGetItemText  
 [!INCLUDE[cpp_fp_under_construction](../../mfc/reference/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual CString OnGetItemText(LPAFX_SHELLITEMINFO pItem);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pItem`  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="refresh"></a>CMFCShellTreeCtrl::Refresh  
 새로 고쳐지고 다시 표시는 [CMFCShellTreeCtrl](../../mfc/reference/cmfcshelltreectrl-class.md)합니다.  
  
```  
void Refresh();
```  
  
### <a name="remarks"></a>주의  
 에 표시 된 항목의 계층 구조를 새로 고치려면이 메서드를 호출 하는 `CMFCShellTreeCtrl`합니다.  
  
##  <a name="selectpath"></a>CMFCShellTreeCtrl::SelectPath  
 선택 항목에는 [CMFCShellTreeCtrl 클래스](../../mfc/reference/cmfcshelltreectrl-class.md) 제공 된 경로 기반 합니다.  
  
```  
BOOL SelectPath(LPCTSTR lpszPath);
BOOL SelectPath(LPCITEMIDLIST lpidl);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `lpszPath`  
 항목의 경로 지정 하는 문자열입니다.  
  
 [in] `lpidl`  
 항목을 지정 하는 PIDL  
  
### <a name="return-value"></a>반환 값  
 `S_OK`성공 하면 `E_FAIL` 그렇지 않은 경우.  
  
##  <a name="setflags"></a>CMFCShellTreeCtrl::SetFlags  
 트리 컨텍스트를 필터링 하는 플래그를 설정 합니다.  
  
```  
void SetFlags(
    DWORD dwFlags,  
    BOOL bRefresh = TRUE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `dwFlags`  
 설정할 플래그입니다.  
  
 [in] `bRefresh`  
 지정 하는 부울 여부는 `CMFCShellTreeCtrl` 즉시 새로 고쳐져 야 합니다.  
  
### <a name="remarks"></a>주의  
 `CMFCShellTreeCtrl` 모든으로 플래그를 설정 하는 전달 [IShellFolder::EnumObjects](http://msdn.microsoft.com/library/windows/desktop/bb775066)합니다. 다른 플래그의 값에 대 한 자세한 내용은 참조 [IShellFolder::EnumObjects](http://msdn.microsoft.com/library/windows/desktop/bb775066)합니다.  
  
##  <a name="setrelatedlist"></a>CMFCShellTreeCtrl::SetRelatedList  
 연결 된 [CMFCShellListCtrl](../../mfc/reference/cmfcshelllistctrl-class.md) 개체는 [CMFCShellTreeCtrl](../../mfc/reference/cmfcshelltreectrl-class.md) 개체입니다.  
  
```  
void SetRelatedList(CMFCShellListCtrl* pShellList);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pShellList`  
 에 대 한 포인터는 `CMFCShellListCtrl` 개체입니다.  
  
### <a name="remarks"></a>주의  
 이 메서드를 연결 된 `CMFCShellListCtrl` 와 `CMFCShellTreeCtrl`합니다. 이러한 개체 탐색기와 유사한 창으로 표시 될 수 있습니다: 사용자가에 있는 개체를 선택 하는 경우는 `CMFCShellTreeCtrl`, 연결 된 항목에는 `CMFCShellListCtrl` 자동으로 업데이트 됩니다.  
  
 메서드를 사용 하 여 [CMFCShellTreeCtrl::GetRelatedList](#getrelatedlist) 를 검색 하는 `CMFCShellListCtrl` 연관는 `CMFCShellTreeCtrl`합니다.  
  
## <a name="see-also"></a>참고 항목  
 [계층 구조 차트](../../mfc/hierarchy-chart.md)   
 [클래스](../../mfc/reference/mfc-classes.md)   
 [CTreeCtrl 클래스](../../mfc/reference/ctreectrl-class.md)   
 [CMFCShellListCtrl 클래스](../../mfc/reference/cmfcshelllistctrl-class.md)
