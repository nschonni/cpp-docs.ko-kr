---
title: "날짜 및 시간 선택 컨트롤에서 콜백 필드 사용 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "DTN_FORMATQUERY"
  - "DTN_FORMAT"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CDateTimeCtrl 클래스의 콜백 필드"
  - "CDateTimeCtrl 클래스, 콜백 필드"
  - "CDateTimeCtrl 클래스, DTN_FORMAT 및 DTN_FORMATQ 처리"
  - "DateTimePicker 컨트롤[MFC]"
  - "DateTimePicker 컨트롤[MFC], 콜백 필드"
  - "DTN_FORMAT 알림"
  - "DTN_FORMATQUERY 알림"
ms.assetid: 404f4ba9-cba7-4718-9faa-bc6b274a723f
caps.latest.revision: 11
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 7
---
# 날짜 및 시간 선택 컨트롤에서 콜백 필드 사용
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

In addition to the standard format characters that define date and time picker fields, you can customize your output by specifying certain parts of a custom format string as callback fields.  To declare a callback field, include one or more "X" characters \(ASCII Code 88\) anywhere in the body of the format string.  For example, the following string "'Today is: 'yy'\/'MM'\/'dd' \(Day 'X'\)'"causes the date and time picker control to display the current value as the year followed by the month, date, and finally the day of the year.  
  
> [!NOTE]
>  The number of X's in a callback field does not correspond to the number of characters that will be displayed.  
  
 You can distinguish between multiple callback fields in a custom string by repeating the "X" character.  Thus, the format string "XXddddMMMdd', 'yyyXXX" contains two unique callback fields, "XX" and "XXX".  
  
> [!NOTE]
>  Callback fields are treated as valid fields, so your application must be prepared to handle **DTN\_WMKEYDOWN** notification messages.  
  
 Implementing callback fields in your date and time picker control consists of three parts:  
  
-   Initializing the custom format string  
  
-   Handling the **DTN\_FORMATQUERY** notification  
  
-   Handling the **DTN\_FORMAT** notification  
  
## Initializing the Custom Format String  
 Initialize the custom string with a call to `CDateTimeCtrl::SetFormat`.  For more information, see [Using Custom Format Strings in a Date and Time Picker Control](../mfc/using-custom-format-strings-in-a-date-and-time-picker-control.md).  A common place to set the custom format string is in the `OnInitDialog` function of your containing dialog class or `OnInitialUpdate` function of your containing view class.  
  
## Handling the DTN\_FORMATQUERY Notification  
 When the control parses the format string and encounters a callback field, the application sends **DTN\_FORMAT** and **DTN\_FORMATQUERY** notification messages.  The callback field string is included with the notifications so you can determine which callback field is being queried.  
  
 The **DTN\_FORMATQUERY** notification is sent to retrieve the maximum allowable size in pixels of the string that will be displayed in the current callback field.  
  
 To properly calculate this value, you must calculate the height and width of the string, to be substituted for the field, using the control's display font.  The actual calculation of the string is easily achieved with a call to the [GetTextExtentPoint32](http://msdn.microsoft.com/library/windows/desktop/dd144938) Win32 function.  Once the size is determined, pass the value back to the application and exit the handler function.  
  
 The following example is one method of supplying the size of the callback string:  
  
 [!code-cpp[NVC_MFCControlLadenDialog#8](../mfc/codesnippet/CPP/using-callback-fields-in-a-date-and-time-picker-control_1.cpp)]  
  
 Once the size of the current callback field has been calculated, you must supply a value for the field.  This is done in the handler for the **DTN\_FORMAT** notification.  
  
## Handling the DTN\_FORMAT Notification  
 The **DTN\_FORMAT** notification is used by the application to request the character string that will be substituted.  The following example demonstrates one possible method:  
  
 [!code-cpp[NVC_MFCControlLadenDialog#9](../mfc/codesnippet/CPP/using-callback-fields-in-a-date-and-time-picker-control_2.cpp)]  
  
> [!NOTE]
>  The pointer to the **NMDATETIMEFORMAT** structure is found by casting the first parameter of the notification handler to the proper type.  
  
## 참고 항목  
 [CDateTimeCtrl 사용](../mfc/using-cdatetimectrl.md)   
 [컨트롤](../mfc/controls-mfc.md)