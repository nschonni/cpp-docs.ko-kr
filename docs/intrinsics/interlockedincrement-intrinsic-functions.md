---
title: "_InterlockedIncrement Intrinsic Functions | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "_InterlockedIncrement_acq"
  - "_InterlockedIncrement16_rel_cpp"
  - "_InterlockedIncrement16_cpp"
  - "_InterlockedIncrement64_rel"
  - "_InterlockedIncrement_rel"
  - "_InterlockedIncrement64_nf"
  - "_InterlockedIncrement16_acq_cpp"
  - "_InterlockedIncrement_rel_cpp"
  - "_InterlockedIncrement64"
  - "_InterlockedIncrement64_rel_cpp"
  - "_InterlockedIncrement16_nf"
  - "_InterlockedIncrement16_rel"
  - "_InterlockedIncrement16_acq"
  - "_InterlockedIncrement_nf"
  - "_InterlockedIncrement_acq_cpp"
  - "_InterlockedIncrement64_cpp"
  - "_InterlockedIncrement64_acq_cpp"
  - "_InterlockedIncrement"
  - "_InterlockedIncrement_cpp"
  - "_InterlockedIncrement64_acq"
  - "_InterlockedIncrement16"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "_InterlockedIncrement intrinsic"
  - "_InterlockedIncrement_acq intrinsic"
  - "_InterlockedIncrement_nf intrinsic"
  - "_InterlockedIncrement_rel intrinsic"
  - "_InterlockedIncrement16 intrinsic"
  - "_InterlockedIncrement16_acq intrinsic"
  - "_InterlockedIncrement16_nf intrinsic"
  - "_InterlockedIncrement16_rel intrinsic"
  - "_InterlockedIncrement64 intrinsic"
  - "_InterlockedIncrement64_acq intrinsic"
  - "_InterlockedIncrement64_nf intrinsic"
  - "_InterlockedIncrement64_rel intrinsic"
  - "InterlockedIncrement intrinsic"
  - "InterlockedIncrement_acq intrinsic"
  - "InterlockedIncrement_rel intrinsic"
  - "InterlockedIncrement16 intrinsic"
  - "InterlockedIncrement64 intrinsic"
  - "InterlockedIncrement64_acq intrinsic"
  - "InterlockedIncrement64_rel intrinsic"
ms.assetid: 37700615-f372-438b-bcef-d76e11839482
caps.latest.revision: 17
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 17
---
# _InterlockedIncrement Intrinsic Functions
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

**Microsoft 전용**  
  
 Win32 [!INCLUDE[winsdkshort](../atl/reference/includes/winsdkshort_md.md)] [InterlockedIncrement](http://msdn.microsoft.com/library/ms683614.aspx) 함수에 대한 컴파일러 내장 지원을 제공합니다.  
  
## 구문  
  
```  
long _InterlockedIncrement(  
   long * lpAddend  
);  
long _InterlockedIncrement_acq(  
   long * lpAddend  
);  
long _InterlockedIncrement_rel(  
   long * lpAddend  
);  
long _InterlockedIncrement_nf(  
   long * lpAddend  
);  
short _InterlockedIncrement16(  
   short * lpAddend  
);  
short _InterlockedIncrement16_acq(  
   short * lpAddend  
);  
short _InterlockedIncrement16_rel(  
   short * lpAddend  
);  
short _InterlockedIncrement16_nf (  
   short * lpAddend  
);  
__int64 _InterlockedIncrement64(  
   __int64 * lpAddend  
);  
__int64 _InterlockedIncrement64_acq(  
   __int64 * lpAddend  
);  
__int64 _InterlockedIncrement64_rel(  
   __int64 * lpAddend  
);   
__int64 _InterlockedIncrement64_nf(  
   __int64 * lpAddend  
);  
```  
  
#### 매개 변수  
 \[in, out\] `lpAddend`  
 증가시킬 변수에 대한 포인터입니다.  
  
## 반환 값  
 반환 값은 증가된 결과 값입니다.  
  
## 요구 사항  
  
|내장 함수|아키텍처|머리글|  
|-----------|----------|---------|  
|`_InterlockedIncrement`, `_InterlockedIncrement16`, `_InterlockedIncrement64`|x86, ARM, [!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]|\<intrin.h\>|  
|`_InterlockedIncrement_acq`, `_InterlockedIncrement_rel`, `_InterlockedIncrement_nf`, `_InterlockedIncrement16_acq`, `_InterlockedIncrement16_rel`, `_InterlockedIncrement16_nf`, `_InterlockedIncrement64_acq`, `_InterlockedIncrement64_rel`, `_InterlockedIncrement64_nf`|ARM|\<intrin.h\>|  
  
## 설명  
 사용되는 데이터 형식과 프로세서별 획득 또는 해제 의미 체계에 따라 다른 `_InterlockedIncrement`의 여러 변형이 있습니다.  
  
 `_InterlockedIncrement` 함수는 32비트 정수 값에 대해 작동하는 반면 `_InterlockedIncrement16`은 16비트 정수 값에 대해, `_InterlockedIncrement64`는 64비트 정수 값에 대해 작동합니다.  
  
 ARM 플랫폼에서는 임계 영역의 시작 및 끝과 같은 위치에서 의미 체계를 획득하고 해제하려면 `_acq` 및 `_rel` 접미사가 포함된 내장 함수를 사용합니다.  `_nf`\("no fence"의 약어\) 접미사가 포함된 내장 함수는 메모리 장벽으로 작동하지 않습니다.  
  
 `lpAddend` 매개 변수가 가리키는 변수는 32비트 경계에 정렬되어야 합니다. 그렇지 않으면 다중 프로세서 x86 시스템과 x86이 아닌 시스템에서 이 함수가 실패합니다.  자세한 내용은 [align](../cpp/align-cpp.md)을 참조하세요.  
  
 Win32 함수는 `Wdm.h` 또는 `Ntddk.h`에서 선언됩니다.  
  
 이러한 루틴은 내장 함수로만 사용할 수 있습니다.  
  
## 예제  
 `_InterlockedIncrement`를 사용하는 방법의 샘플은 [\_InterlockedDecrement](../intrinsics/interlockeddecrement-intrinsic-functions.md)를 참조하세요.  
  
## Microsoft 전용 종료  
  
## 참고 항목  
 [컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)   
 [C\+\+ 키워드](../cpp/keywords-cpp.md)   
 [x86 컴파일러와 충돌](../build/conflicts-with-the-x86-compiler.md)