---
title: "문자열 변환 매크로 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: reference
dev_langs:
- C++
ms.assetid: 2ff7c0b6-2bde-45fe-897f-6128e18e0c27
caps.latest.revision: 16
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
ms.sourcegitcommit: bb94e24657d16b2a3eda3a770c2b6ae734c6006f
ms.openlocfilehash: e322c3af297c288ec6c9ccdb1c04e58d0a5759ff
ms.lasthandoff: 04/12/2017

---
# <a name="string-conversion-macros"></a>문자열 변환 매크로
이러한 매크로 문자열 변환 기능을 제공합니다.  
  
 
##  <a name="atl_and_mfc_string_conversion_macros"></a>ATL 및 MFC 문자열 변환 매크로  
 이 항목에서 설명하는 문자열 변환 매크로는 ATL과 MFC에 모두 사용 가능합니다. MFC 문자열 변환에 대 한 자세한 내용은 참조 하십시오. [TN059: MFC MBCS/유니코드 변환 매크로 사용 하 여](../../mfc/tn059-using-mfc-mbcs-unicode-conversion-macros.md) 및 [MFC 매크로 및 전역](../../mfc/reference/mfc-macros-and-globals.md)합니다.  
  
##  <a name="devmode_and_textmetric_string_conversion_macros"></a>DEVMODE 및 TEXTMETRIC 문자열 변환 매크로  
 이러한 매크로의 복사본을 만들고는 [DEVMODE](http://msdn.microsoft.com/library/windows/desktop/dd183565) 또는 [TEXTMETRIC](http://msdn.microsoft.com/library/windows/desktop/dd145132) 구조체이 고 새 구조 내의 문자열을 새 문자열 형식으로 변환 합니다. 매크로 새 구조에 대 한 스택에 메모리를 할당 하 고 새 구조에 대 한 포인터를 반환 합니다.  
  
```
MACRONAME( address_of_structure )
```  
  
### <a name="remarks"></a>주의  
 예:  
  
 [!code-cpp[NVC_ATL_Utilities # 128](../../atl/codesnippet/cpp/string-conversion-macros_1.cpp)]  
  
 and:  
  
 [!code-cpp[NVC_ATL_Utilities # 129](../../atl/codesnippet/cpp/string-conversion-macros_2.cpp)]  
  
 왼쪽에는 원본 구조에 있는 문자열 형식의 매크로 이름 (예를 들어 **A**) 및 대상 구조에 있는 문자열 형식의 오른쪽에 표시 됩니다 (예를 들어 **W**). **A** stands for **LPSTR**, **OLE** stands for `LPOLESTR`, **T** stands for `LPTSTR`, and **W** stands for `LPWSTR`.  
  
 따라서 `DEVMODEA2W` 복사본은 `DEVMODE` 구조체를 **LPSTR** 에 문자열는 `DEVMODE` 구조체를 `LPWSTR` 문자열 `TEXTMETRICOLE2T` 복사본은 `TEXTMETRIC` 구조체를 `LPOLESTR` 문자열에 `TEXTMETRIC` 구조체를 `LPTSTR` 문자열 및 등입니다.  
  
 변환 하는 두 문자열의 `DEVMODE` 구조는 장치 이름 ( **dmDeviceName**) 및 양식 이름 ( **dmFormName**). `DEVMODE` 문자열 변환 매크로 구조 크기를 업데이트할 ( **dmSize**).  
  
 변환에서 4 개의 문자열은 `TEXTMETRIC` 구조는 첫 번째 문자 ( **tmFirstChar**), 마지막 문자 ( **tmLastChar**), 기본 문자 ( **tmDefaultChar**), 및 줄바꿈 문자 ( **tmBreakChar**).  
  
 동작은 `DEVMODE` 및 `TEXTMETRIC` 있는 경우 문자열 변환 매크로 적용 중인 컴파일러 지시문에 따라 다릅니다. 소스와 대상 형식이 같으면 변환이 수행되지 않습니다. 컴파일러 지시문 변경 **T** 및 **OLE** 다음과 같습니다.  
  
|적용되는 컴파일러 지시문|T의 변경 결과|OLE의 변경 결과|  
|----------------------------------|---------------|-----------------|  
|없음|**A**|**W**|  
|**_UNICODE**|**W**|**W**|  
|**OLE2ANSI**|**A**|**A**|  
|**_UNICODE** 및 **OLE2ANSI**|**W**|**A**|  
  
 다음 표에 `DEVMODE` 및 `TEXTMETRIC` 문자열 변환 매크로입니다.  
  
|||  
|-|-|  
|`DEVMODEA2W`|`TEXTMETRICA2W`|  
|`DEVMODEOLE2T`|`TEXTMETRICOLE2T`|  
|`DEVMODET2OLE`|`TEXTMETRICT2OLE`|  
|`DEVMODEW2A`|`TEXTMETRICW2A`|  
  
## <a name="see-also"></a>참고 항목  
 [매크로](../../atl/reference/atl-macros.md)

