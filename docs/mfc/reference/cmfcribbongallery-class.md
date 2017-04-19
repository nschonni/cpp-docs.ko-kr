---
title: "CMFCRibbonGallery 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CMFCRibbonGallery
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::CMFCRibbonGallery
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::AddGroup
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::AddSubItem
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::Clear
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::EnableMenuResize
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::EnableMenuSideBar
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::GetCompactSize
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::GetDroppedDown
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::GetGroupName
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::GetGroupOffset
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::GetIconsInRow
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::GetItemToolTip
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::GetLastSelectedItem
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::GetPaletteID
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::GetRegularSize
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::GetSelectedItem
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::HasMenu
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::IsButtonMode
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::IsMenuResizeEnabled
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::IsMenuResizeVertical
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::IsMenuSideBar
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::OnAfterChangeRect
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::OnDraw
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::OnEnable
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::OnRTLChanged
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::RedrawIcons
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::RemoveItemToolTips
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::SelectItem
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::SetACCData
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::SetButtonMode
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::SetGroupName
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::SetIconsInRow
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::SetItemToolTip
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::SetPalette
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::SetPaletteID
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::OnDrawPaletteIcon
dev_langs:
- C++
helpviewer_keywords:
- CMFCRibbonGallery class
ms.assetid: 9734c9c9-981c-4b3f-8c59-264fd41811b4
caps.latest.revision: 28
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
ms.openlocfilehash: c4eadb9820f2d7318131cc4d197dbe28d65491c0
ms.lasthandoff: 02/24/2017

---
# <a name="cmfcribbongallery-class"></a>CMFCRibbonGallery 클래스
Office 2007 스타일의 리본 갤러리를 구현합니다.  
  
## <a name="syntax"></a>구문  
  
```  
class CMFCRibbonGallery : public CMFCRibbonButton  
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[CMFCRibbonGallery::CMFCRibbonGallery](#cmfcribbongallery)|`CMFCRibbonGallery` 개체를 생성하고 초기화합니다.|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[CMFCRibbonGallery::AddGroup](#addgroup)|갤러리에 새 그룹을 추가합니다.|  
|[CMFCRibbonGallery::AddSubItem](#addsubitem)|드롭다운 메뉴에 새 메뉴 항목을 추가합니다.|  
|[CMFCRibbonGallery::Clear](#clear)|갤러리의 콘텐츠를 지웁니다.|  
|[CMFCRibbonGallery::EnableMenuResize](#enablemenuresize)|메뉴 패널의 크기를 조정 하지 않도록 설정 하거나 사용 합니다.|  
|[CMFCRibbonGallery::EnableMenuSideBar](#enablemenusidebar)|팝업 메뉴의 왼쪽 세로 막대를 사용 하지 않도록 설정 하거나 사용 합니다.|  
|[CMFCRibbonGallery::GetCompactSize](#getcompactsize)|(재정의 [CMFCRibbonButton::GetCompactSize](../../mfc/reference/cmfcribbonbutton-class.md#getcompactsize).)|  
|[CMFCRibbonGallery::GetDroppedDown](#getdroppeddown)|(재정의 [CMFCRibbonBaseElement::GetDroppedDown](../../mfc/reference/cmfcribbonbaseelement-class.md#getdroppeddown).)|  
|[CMFCRibbonGallery::GetGroupName](#getgroupname)|지정된 된 인덱스에 있는 그룹의 이름을 반환 합니다.|  
|[CMFCRibbonGallery::GetGroupOffset](#getgroupoffset)||  
|[CMFCRibbonGallery::GetIconsInRow](#geticonsinrow)|행의 리본 갤러리 항목의 수를 반환합니다.|  
|[CMFCRibbonGallery::GetItemToolTip](#getitemtooltip)|갤러리의 항목과 연결 된 도구 설명 텍스트를 반환 합니다.|  
|[CMFCRibbonGallery::GetLastSelectedItem](#getlastselecteditem)|사용자가 선택한 갤러리에 있는 마지막 항목의 인덱스를 반환 합니다.|  
|[CMFCRibbonGallery::GetPaletteID](#getpaletteid)|현재 갤러리의 명령 ID를 반환합니다.|  
|[CMFCRibbonGallery::GetRegularSize](#getregularsize)|(재정의 [CMFCRibbonButton::GetRegularSize](../../mfc/reference/cmfcribbonbutton-class.md#getregularsize).)|  
|[CMFCRibbonGallery::GetSelectedItem](#getselecteditem)||  
|[CMFCRibbonGallery::HasMenu](#hasmenu)|(재정의 [CMFCRibbonButton::HasMenu](../../mfc/reference/cmfcribbonbutton-class.md#hasmenu).)|  
|[CMFCRibbonGallery::IsButtonMode](#isbuttonmode)|갤러리 갤러리 단추에 포함 되는지 여부를 지정 합니다.|  
|[CMFCRibbonGallery::IsMenuResizeEnabled](#ismenuresizeenabled)|메뉴 크기 조정의 활성화 여부를 지정 합니다.|  
|[CMFCRibbonGallery::IsMenuResizeVertical](#ismenuresizevertical)||  
|[CMFCRibbonGallery::IsMenuSideBar](#ismenusidebar)|세로 막대 사용 되는지 여부를 지정 합니다.|  
|[CMFCRibbonGallery::OnAfterChangeRect](#onafterchangerect)|(`CMFCRibbonButton::OnAfterChangeRect`를 재정의합니다.)|  
|[CMFCRibbonGallery::OnDraw](#ondraw)|(재정의 [CMFCRibbonButton::OnDraw](../../mfc/reference/cmfcribbonbutton-class.md#ondraw).)|  
|[CMFCRibbonGallery::OnEnable](#onenable)|(`CMFCRibbonBaseElement::OnEnable`를 재정의합니다.)|  
|[CMFCRibbonGallery::OnRTLChanged](#onrtlchanged)|(재정의 [CMFCRibbonBaseElement::OnRTLChanged](../../mfc/reference/cmfcribbonbaseelement-class.md#onrtlchanged).)|  
|[CMFCRibbonGallery::RedrawIcons](#redrawicons)|갤러리를 다시 그립니다.|  
|[CMFCRibbonGallery::RemoveItemToolTips](#removeitemtooltips)|갤러리에 있는 모든 항목에서 도구 설명을 제거합니다.|  
|[CMFCRibbonGallery::SelectItem](#selectitem)||  
|[CMFCRibbonGallery::SetACCData](#setaccdata)|(재정의 [CMFCRibbonButton::SetACCData](../../mfc/reference/cmfcribbonbutton-class.md#setaccdata).)|  
|[CMFCRibbonGallery::SetButtonMode](#setbuttonmode)|드롭 다운 단추 또는 리본에서 직접 팔레트도 리본 갤러리를 표시할지 여부를 지정 합니다.|  
|[CMFCRibbonGallery::SetGroupName](#setgroupname)|그룹의 이름을 설정합니다.|  
|[CMFCRibbonGallery::SetIconsInRow](#seticonsinrow)|갤러리의 각 행의 항목 수를 정의합니다.|  
|[CMFCRibbonGallery::SetItemToolTip](#setitemtooltip)|갤러리에서 항목에 대 한 도구 설명 텍스트를 설정합니다.|  
|[CMFCRibbonGallery::SetPalette](#setpalette)|리본 갤러리를 색상표를 연결합니다.|  
|[CMFCRibbonGallery::SetPaletteID](#setpaletteid)|전송 된 명령 ID를 정의 `WM_COMMAND` 갤러리 항목을 선택 하는 경우 메시지입니다.|  
  
### <a name="protected-methods"></a>Protected 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[CMFCRibbonGallery::OnDrawPaletteIcon](#ondrawpaletteicon)|갤러리 아이콘을 그릴 때 프레임 워크에 의해 호출 됩니다.|  
  
## <a name="remarks"></a>주의  
 갤러리 단추를 사용자가 열 때 갤러리를 표시 한다는 점을 제외 하면 일반 메뉴 단추 처럼 동작 합니다. 갤러리에서 항목을 선택 하면 프레임 워크는 전송 된 `WM_COMMAND` 단추의 명령 ID와 함께 메시지입니다. 메시지를 처리 하는 경우를 호출 해야 [CMFCRibbonGallery::GetLastSelectedItem](#getlastselecteditem) 갤러리에서 선택 된 항목을 확인 하려면.  
  
## <a name="example"></a>예제  
 다음 예제에서 다양 한 메서드를 사용 하는 방법을 보여 줍니다는 `CMFCRibbonGallery` 를 구성 하는 클래스는 `CMFCRibbonGallery` 개체입니다. 이 예제에는 갤러리의 행당 항목의 수를 지정, 메뉴 패널의 크기 조정 설정, 팝업 메뉴의 왼쪽에 세로 막대를 사용 하도록 설정 및 리본 모음에 직접 팔레트와 리본 갤러리를 표시 하는 방법을 보여 줍니다. 이 코드 조각은의 일부인는 [그리기 클라이언트 샘플](../../visual-cpp-samples.md)합니다.  
  
 [!code-cpp[NVC_MFC_DrawClient #&6;](../../mfc/reference/codesnippet/cpp/cmfcribbongallery-class_1.cpp)]  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 [CObject](../../mfc/reference/cobject-class.md) [CMFCRibbonBaseElement](../../mfc/reference/cmfcribbonbaseelement-class.md) [CMFCRibbonButton](../../mfc/reference/cmfcribbonbutton-class.md)  
  
 [CMFCRibbonGallery](../../mfc/reference/cmfcribbongallery-class.md)  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** afxRibbonPaletteGallery.h  
  
##  <a name="addgroup"></a>CMFCRibbonGallery::AddGroup  
 갤러리에 새 그룹을 추가합니다.  
  
```  
void AddGroup(
    LPCTSTR lpszGroupName,  
    UINT uiImagesPaletteResID,  
    int cxPaletteImage);

 
void AddGroup(
    LPCTSTR lpszGroupName,  
    CMFCToolBarImages& imagesGroup);

 
void AddGroup(
    LPCTSTR lpszGroupName,  
    int nIconsNum);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `lpszGroupName`  
 그룹의 이름을 지정합니다.  
  
 [in] `uiImagesPaletteResID`  
 그룹에 대 한 이미지가 포함 된 이미지 목록의 리소스 ID를 지정 합니다.  
  
 [in] `cxPaletteImage`  
 이미지의 픽셀에서 너비를 지정합니다.  
  
 [in] `imagesGroup`  
 그룹 이미지를 포함 하는 이미지 목록에 대 한 참조입니다.  
  
 [in] `nIconsNum`  
 그룹의 아이콘 수를 지정합니다. 사용자 지정 (소유자 그리기)에 대해서만이 매개 변수를 지정 해야 그룹입니다.  
  
### <a name="remarks"></a>주의  
 이 메서드를 호출 하 여 리본 갤러리에 있는 항목이 여러 그룹으로 나눌 수 있습니다. 각 그룹에는 캡션을 가질 수 있습니다.  
  
##  <a name="addsubitem"></a>CMFCRibbonGallery::AddSubItem  
 드롭다운 메뉴에 새 메뉴 항목을 추가합니다.  
  
```  
void AddSubItem(
    CMFCRibbonBaseElement* pSubItem,  
    int nIndex=-1,  
    BOOL bOnTop=FALSE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pSubItem`  
 메뉴에 추가할 항목에 대 한 포인터입니다.  
  
 [in] `nIndex`  
 위치의&0;부터 시작 하는 인덱스 항목을 삽입 하는 위치를 지정 합니다.  
  
 [in] `bOnTop`  
 `TRUE`리본 갤러리; 하기 전에 항목을 삽입할 지정 하려면 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>주의  
 이 메서드를 호출 하 여 팝업 메뉴 항목 팝업 갤러리를 결합할 수 있습니다. 앞 이나 뒤의 갤러리에는 메뉴 항목을 배치할 수 있습니다.  
  
 갤러리 앞에 나오는 항목을 삽입 하려면 설정 `bOnTop` 를 `TRUE`합니다. 설정 `bOnTop` 를 `FALSE` 갤러리 아래 항목을 삽입 하 합니다.  
  
> [!NOTE]
>  매개 변수 `nIndex` 갤러리 맨 위에 있는 및 갤러리의 맨 아래에 삽입 하는 인덱스를 지정 합니다. 갤러리 하기 전에 항목 한 위치를 삽입 해야 하는 경우 설정 하는 예를 들어 `nIndex` 1 및 `bOnTop` 를 `TRUE`합니다. 갤러리 아래쪽에 항목 한 위치를 삽입 하는 경우 설정 하는 마찬가지로 `nIndex` 1 및 `bOnTop` 를 `FALSE`합니다.  
  
##  <a name="clear"></a>CMFCRibbonGallery::Clear  
 갤러리의 콘텐츠를 지웁니다.  
  
```  
virtual void Clear();
```  
  
### <a name="remarks"></a>주의  
 리본 갤러리에서 모든 콘텐츠를 제거 하려면이 메서드를 호출 합니다. 리본 갤러리에는 새로운 리본 갤러리 또는 그룹 집합을 연결 하기 전에 수행 되어야 합니다.  
  
##  <a name="cmfcribbongallery"></a>CMFCRibbonGallery::CMFCRibbonGallery  
 생성 하 고 초기화는 [CMFCRibbonGallery](../../mfc/reference/cmfcribbongallery-class.md) 개체입니다.  
  
```  
CMFCRibbonGallery (
    UINT nID,  
    LPCTSTR lpszText,  
    int nSmallImageIndex,  
    int nLargeImageIndex,  
    CMFCToolBarImages& imagesPalette);

 
CMFCRibbonGallery (
    UINT nID,  
    LPCTSTR lpszText,  
    int nSmallImageIndex,  
    int nLargeImageIndex,  
    UINT uiImagesPaletteResID=0,  
    int cxPaletteImage=0);

 
CMFCRibbonGallery (
    UINT nID,  
    LPCTSTR lpszText,  
    int nSmallImageIndex,  
    int nLargeImageIndex,  
    CSize sizeIcon,  
    int nIconsNum,  
    BOOL bDefaultButtonStyle=TRUE);
```  
  
### <a name="parameters"></a>매개 변수  
 `nID`  
 단추를 클릭할 때 실행할 명령의 명령 ID를 지정 합니다.  
  
 `lpszText`  
 단추에 표시할 텍스트를 지정 합니다.  
  
 `nSmallImageIndex`  
 단추에 작은 이미지의&0;부터 시작 하는 인덱스입니다.  
  
 `nLargeImageIndex`  
 큰 단추에 표시할 이미지의&0;부터 시작 하는 인덱스입니다.  
  
 `imagesPalette`  
 에 대 한 참조는 [CMFCToolBarImages](../../mfc/reference/cmfctoolbarimages-class.md) 갤러리에 표시할 이미지를 포함 하는 개체입니다.  
  
 `uiImagesPaletteResID`  
 갤러리에 표시할 이미지의 목록의 리소스 ID입니다.  
  
 `cxPaletteImage`  
 갤러리에서 이미지의 픽셀에서 너비를 지정합니다.  
  
 `sizeIcon`  
 갤러리 이미지의 픽셀에서 크기를 지정 합니다.  
  
 `nIconsNum`  
 갤러리의 아이콘 수를 지정합니다.  
  
 `bDefaultButtonStyle`  
 기본값 또는 소유자가 그린 단추 스타일을 사용할지 여부를 지정 합니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="enablemenuresize"></a>CMFCRibbonGallery::EnableMenuResize  
 메뉴 패널의 크기를 조정 하지 않도록 설정 하거나 사용 합니다.  
  
```  
void EnableMenuResize(
    BOOL bEnable = TRUE,  
    BOOL bVertcalOnly = FALSE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bEnable`  
 `TRUE`메뉴; 크기 조정을 사용 하도록 설정 하려면 그렇지 않으면 `FALSE`합니다.  
  
 [in] `bVertcalOnly`  
 `TRUE`갤러리를 세로로; 조정할 수 있는 지정 하려면 `FALSE` 갤러리 수를 지정 하려면 크기를 조정할 모두 세로 및 가로로 합니다.  
  
### <a name="remarks"></a>주의  
 이 메서드를 사용 하 여 사용할지 여부를 리본 갤러리를 크기 조정 합니다. 크기를 조정할 때 리본 갤러리 사용자 크기를 조정 하는 데 사용할 수 있는 위치 조정 막대를 표시 합니다.  
  
##  <a name="enablemenusidebar"></a>CMFCRibbonGallery::EnableMenuSideBar  
 팝업 메뉴의 왼쪽 세로 막대를 사용 하지 않도록 설정 하거나 사용 합니다.  
  
```  
void EnablMenuSideBar(BOOL bEnable=TRUE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bEnable`  
 `TRUE`세로 막대를 사용할 수 있음을; 지정 하려면 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>주의  
 메뉴의 왼쪽에 Office XP 스타일 세로 막대를 사용 하지 않도록 설정 하거나 사용 하려면이 메서드를 호출 합니다.  
  
##  <a name="getcompactsize"></a>CMFCRibbonGallery::GetCompactSize  
 [!INCLUDE[cpp_fp_under_construction](../../mfc/reference/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual CSize GetCompactSize(CDC* pDC);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDC`  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="getdroppeddown"></a>CMFCRibbonGallery::GetDroppedDown  
 [!INCLUDE[cpp_fp_under_construction](../../mfc/reference/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual CMFCRibbonBaseElement* GetDroppedDown();
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="getgroupname"></a>CMFCRibbonGallery::GetGroupName  
 지정된 된 인덱스에 있는 그룹의 이름을 반환 합니다.  
  
```  
LPCTSTR GetGroupName(int nGroupIndex) const;  
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nGroupIndex`  
 검색 하려는 이름이 그룹에 대 한 인덱스를 지정 합니다.  
  
### <a name="return-value"></a>반환 값  
 지정된 된 인덱스에 있는 그룹의 이름입니다. 잘못 된 인덱스가 전달 실패 한 어설션이 발생 합니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="getgroupoffset"></a>CMFCRibbonGallery::GetGroupOffset  
 [!INCLUDE[cpp_fp_under_construction](../../mfc/reference/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual int GetGroupOffset() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="geticonsinrow"></a>CMFCRibbonGallery::GetIconsInRow  
 행의 리본 갤러리 항목의 수를 반환합니다.  
  
```  
int GetIconsInRow() const;  
```  
  
### <a name="return-value"></a>반환 값  
 행에 있는 항목의 수입니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="getitemtooltip"></a>CMFCRibbonGallery::GetItemToolTip  
 갤러리의 항목과 연결 된 도구 설명 텍스트를 반환 합니다.  
  
```  
LPCTSTR GetItemToolTip(int nItemIndex) const;  
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nItemIndex`  
 도구 설명 텍스트를 검색할 항목의&0;부터 시작 하는 인덱스를 지정 합니다.  
  
### <a name="return-value"></a>반환 값  
 포인터의 리본 갤러리 항목에 할당 된 도구 설명 문자열입니다. 수 `NULL` 도구 설명이 해당 항목에 할당 된 경우.  
  
### <a name="remarks"></a>주의  
  
##  <a name="getlastselecteditem"></a>CMFCRibbonGallery::GetLastSelectedItem  
 사용자가 선택한 리본 갤러리에 있는 마지막 항목의 인덱스를 반환 합니다.  
  
```  
static int GetLastSelectedItem(UINT uiCmdID);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `uiCmdID`  
 리본 갤러리를 열에 있는 메뉴 항목의 명령 ID를 지정 합니다.  
  
### <a name="return-value"></a>반환 값  
 사용자가 리본 갤러리의 모든 항목을 선택 하면 라이브러리 보냅니다는 `WM_COMMAND` 리본 갤러리를 연 메뉴 단추의 명령 ID와 함께 메시지입니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="getpaletteid"></a>CMFCRibbonGallery::GetPaletteID  
 현재 팔레트의 명령 ID를 반환합니다.  
  
```  
int GetPaletteID() const;  
```  
  
### <a name="return-value"></a>반환 값  
 현재 선택 된 색상표의 명령 ID입니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="getregularsize"></a>CMFCRibbonGallery::GetRegularSize  
 [!INCLUDE[cpp_fp_under_construction](../../mfc/reference/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual CSize GetRegularSize(CDC* pDC);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDC`  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="getselecteditem"></a>CMFCRibbonGallery::GetSelectedItem  
 [!INCLUDE[cpp_fp_under_construction](../../mfc/reference/includes/cpp_fp_under_construction_md.md)]  
  
```  
int GetSelectedItem() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="hasmenu"></a>CMFCRibbonGallery::HasMenu  
 [!INCLUDE[cpp_fp_under_construction](../../mfc/reference/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual BOOL HasMenu() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="isbuttonmode"></a>CMFCRibbonGallery::IsButtonMode  
 색상표 갤러리 단추에 포함 되는지 여부를 지정 합니다.  
  
```  
BOOL IsButtonMode() const;  
```  
  
### <a name="return-value"></a>반환 값  
 `TRUE`색상표 드롭 다운 메뉴 단추;로 표시 되는 경우 `FALSE` 이면 색상표 리본 메뉴에 직접 표시 됩니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="ismenuresizeenabled"></a>CMFCRibbonGallery::IsMenuResizeEnabled  
 메뉴 크기 조정 사용 되는지 여부를 지정 합니다.  
  
```  
BOOL IsMenuResizeEnabled() const;  
```  
  
### <a name="return-value"></a>반환 값  
 `TRUE`메뉴 크기 조정 설정한 경우입니다. 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="ismenuresizevertical"></a>CMFCRibbonGallery::IsMenuResizeVertical  
 [!INCLUDE[cpp_fp_under_construction](../../mfc/reference/includes/cpp_fp_under_construction_md.md)]  
  
```  
BOOL IsMenuResizeVertical() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
  
##  <a name="ismenusidebar"></a>CMFCRibbonGallery::IsMenuSideBar  
 세로 막대 사용 되는지 여부를 지정 합니다.  
  
```  
BOOL IsMenuSideBar() const;  
```  
  
### <a name="return-value"></a>반환 값  
 `TRUE`Office XP 스타일 세로 막대는 팝업 메뉴;의 왼쪽에 그려지는 경우 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="onafterchangerect"></a>CMFCRibbonGallery::OnAfterChangeRect  
 [!INCLUDE[cpp_fp_under_construction](../../mfc/reference/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual void OnAfterChangeRect(CDC* pDC);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDC`  
  
### <a name="remarks"></a>주의  
  
##  <a name="ondraw"></a>CMFCRibbonGallery::OnDraw  
 [!INCLUDE[cpp_fp_under_construction](../../mfc/reference/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual void OnDraw(CDC* pDC);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDC`  
  
### <a name="remarks"></a>주의  
  
##  <a name="ondrawpaletteicon"></a>CMFCRibbonGallery::OnDrawPaletteIcon  
 갤러리 아이콘을 그릴 때 프레임 워크에 의해 호출 됩니다.  
  
```  
virtual void OnDrawPaletteIcon(
    CDC* pDC,  
    CRect rectIcon,  
    int nIconIndex,  
    CMFCRibbonGalleryIcon* pIcon,  
    COLORREF clrText);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDC`  
 그리기에 사용 되는 장치 컨텍스트에 대 한 포인터입니다.  
  
 [in] `rectIcon`  
 그릴 아이콘의 경계 사각형을 지정 합니다.  
  
 [in] `nIconIndex`  
 갤러리 아이콘을 그리는 아이콘의 이미지 목록에서&0;부터 시작 인덱스를 지정 합니다.  
  
 [in] `pIcon`  
 그리고 아이콘에 대 한 포인터입니다.  
  
 [in] `clrText`  
 그릴 항목의 텍스트의 색을 지정 합니다.  
  
### <a name="remarks"></a>주의  
 리본 갤러리의 모양을 사용자 지정 하려면 파생된 클래스에서이 메서드를 재정의할 수 있습니다.  
  
##  <a name="onenable"></a>CMFCRibbonGallery::OnEnable  
 [!INCLUDE[cpp_fp_under_construction](../../mfc/reference/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual void OnEnable(BOOL bEnable);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bEnable`  
  
### <a name="remarks"></a>주의  
  
##  <a name="onrtlchanged"></a>CMFCRibbonGallery::OnRTLChanged  
 [!INCLUDE[cpp_fp_under_construction](../../mfc/reference/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual void OnRTLChanged(BOOL bIsRTL);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bIsRTL`  
  
### <a name="remarks"></a>주의  
  
##  <a name="redrawicons"></a>CMFCRibbonGallery::RedrawIcons  
 갤러리를 다시 그립니다.  
  
```  
void RedrawIcons();
```  
  
### <a name="remarks"></a>주의  
 갤러리를 다시 그리도록 하려면이 함수를 호출 합니다. 런타임 시 갤러리의 내용을 변경 하면이 메서드를 호출 해야 합니다.  
  
##  <a name="removeitemtooltips"></a>CMFCRibbonGallery::RemoveItemToolTips  
 갤러리에 있는 모든 항목에서 도구 설명을 제거합니다.  
  
```  
void RemoveItemToolTips();
```  
  
### <a name="remarks"></a>주의  
  
##  <a name="selectitem"></a>CMFCRibbonGallery::SelectItem  
 [!INCLUDE[cpp_fp_under_construction](../../mfc/reference/includes/cpp_fp_under_construction_md.md)]  
  
```  
void SelectItem(int nItemIndex);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nItemIndex`  
  
### <a name="remarks"></a>주의  
  
##  <a name="setaccdata"></a>CMFCRibbonGallery::SetACCData  
 리본 갤러리에서 내게 필요한 옵션 데이터를 사용하여 지정된 `CAccessibilityData` 개체를 채웁니다.  
  
```  
virtual BOOL SetACCData(
    CWnd* pParent,   
    CAccessibilityData& data);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pParent`  
 리본 갤러리 창의 부모 창입니다.  
  
 [out] `data`  
 리본 갤러리에서 내게 필요한 옵션 데이터를 받는 `CAccessibilityData` 개체입니다.  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>주의  
 해당 메서드에 성공하면 `TRUE`이고, 그렇지 않으면 `FALSE`입니다.  
  
##  <a name="setbuttonmode"></a>CMFCRibbonGallery::SetButtonMode  
 드롭 다운 단추 또는 리본에서 직접 팔레트도 리본 갤러리를 표시할지 여부를 결정 합니다.  
  
```  
void SetButtonMode(BOOL bSet=TRUE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bSet`  
 `TRUE`드롭다운 메뉴 단추;으로 리본 갤러리를 표시 하려면 `FALSE` 리본에서 직접 리본 갤러리의 내용을 표시 합니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="setgroupname"></a>CMFCRibbonGallery::SetGroupName  
 그룹의 이름을 설정합니다.  
  
```  
void SetGroupName(
    int nGroupIndex,  
    LPCTSTR lpszGroupName);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nGroupIndex`  
 이름이 변경 되는 그룹에 대 한 인덱스를 지정 합니다.  
  
 [in] `lpszGroupName`  
 그룹에 대 한 새 이름을 지정합니다.  
  
### <a name="remarks"></a>주의  
 이름이 변경 되는 그룹 추가 해 두어야를 사용 하 여 [CMFCRibbonGallery::AddGroup](#addgroup) 메서드.  
  
##  <a name="seticonsinrow"></a>CMFCRibbonGallery::SetIconsInRow  
 갤러리의 각 행의 항목 수를 지정합니다.  
  
```  
void SetIconsInRow(int nIconsInRow);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nIconsInRow`  
 갤러리의 각 행에 표시할 항목 수를 지정 합니다.  
  
### <a name="remarks"></a>주의  
 이 메서드를 사용 하 여 리본 갤러리의 너비를 지정 합니다.  
  
##  <a name="setitemtooltip"></a>CMFCRibbonGallery::SetItemToolTip  
 갤러리에서 항목에 대 한 도구 설명 텍스트를 설정합니다.  
  
```  
void SetItemToolTip(
    int nItemIndex,  
    LPCTSTR lpszToolTip);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nItemIndex`  
 도구 설명을 연결할 색상표 항목의&0;부터 시작 하는 인덱스입니다.  
  
 [in] `lpszToolTip`  
 도구 설명에 표시할 텍스트입니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="setpalette"></a>CMFCRibbonGallery::SetPalette  
 리본 갤러리를 색상표를 연결합니다.  
  
```  
void SetPalette(CMFCToolBarImages& imagesPalette);

 
void SetPalette(
    UINT uiImagesPaletteResID,  
    int cxPaletteImage);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `imagesPalette`  
 갤러리에 표시할 아이콘이 포함 된 이미지 목록을 지정 합니다.  
  
 [in] `uiImagesPaletteResID`  
 갤러리에 표시할 아이콘을 포함 하는 이미지 목록의 리소스 ID를 지정 합니다.  
  
 [in] `cxPaletteImage`  
 갤러리에서 이미지의 픽셀에서 너비를 지정합니다.  
  
### <a name="remarks"></a>주의  
  
##  <a name="setpaletteid"></a>CMFCRibbonGallery::SetPaletteID  
 전송 된 명령 ID를 정의 **WM_COMMAND** 메시지는 사용자가 갤러리 항목을 선택 합니다.  
  
```  
void SetPaletteID(UINT nID);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nID`  
 전송 된 명령 ID를 지정 된 **WM_COMMAND** 갤러리 항목을 선택할 경우 메시지입니다.  
  
### <a name="remarks"></a>주의  
 사용자가 선택한 갤러리에서 특정 항목을 확인 하려면 호출의 [CMFCRibbonGallery::GetLastSelectedItem](#getlastselecteditem) 정적 메서드입니다.  
  
## <a name="see-also"></a>참고 항목  
 [계층 구조 차트](../../mfc/hierarchy-chart.md)   
 [클래스](../../mfc/reference/mfc-classes.md)   
 [CMFCRibbonButton 클래스](../../mfc/reference/cmfcribbonbutton-class.md)   
 [CMFCRibbonGalleryMenuButton 클래스](../../mfc/reference/cmfcribbongallerymenubutton-class.md)
