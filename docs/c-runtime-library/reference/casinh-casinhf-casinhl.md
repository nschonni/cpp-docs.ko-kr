---
title: "casinh, casinhf, casinhl | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "cpp"
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
apiname: 
  - "casinh"
  - "casinhl"
  - "casinhf"
apilocation: 
  - "msvcrt.dll"
  - "msvcr80.dll"
  - "msvcr90.dll"
  - "msvcr100.dll"
  - "msvcr100_clr0400.dll"
  - "msvcr110.dll"
  - "msvcr110_clr0400.dll"
  - "msvcr120.dll"
  - "msvcr120_clr0400.dll"
  - "ucrtbase.dll"
  - "api-ms-win-crt-math-l1-1-0.dll"
apitype: "DLLExport"
f1_keywords: 
  - "casinh"
  - "casinhf"
  - "casinhl"
  - "complex/casinh"
  - "complex/casinhf"
  - "complex/casinhl"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "casinh 함수"
  - "casinhf 함수"
  - "casinhl 함수"
ms.assetid: bd18340b-21dd-4c86-a14e-e8e15dd97e3b
caps.latest.revision: 10
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 10
---
# casinh, casinhf, casinhl
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

간격에서 벗어난 분기 컷 복소수 역 하이퍼볼릭 사인 값 검색 \[−i, \+ i\] 허수 축을 따라 합니다.  
  
## 구문  
  
```  
_Dcomplex casinh(   
   _Dcomplex z   
);  
_Fcomplex casinh(   
   _Fcomplex z   
);  // C++ only  
_Lcomplex casinh(   
   _Lcomplex z   
);  // C++ only  
_Fcomplex casinhf(   
   _Fcomplex z   
);  
_Lcomplex casinhl(   
   _Lcomplex z   
);  
```  
  
#### 매개 변수  
 `z`  
 라디안에서 각도 나타내는 복소수.  
  
## 반환 값  
 역 쌍 곡 사인 `z`, 라디안에서입니다. 결과 축에 실제 및 가상 축 간격 \[−iπ\/2 \+ iπ\/2\]에 바인딩되어 있지 않습니다.  
  
## 설명  
 C\+\+에서는 오버로드를 허용하므로 `casinh` 및 `_Fcomplex` 값을 사용 및 반환하는 `_Lcomplex`의 오버로드를 호출할 수 있습니다. C 프로그램에서 `casinh` 항상 사용 하 고 반환 된 `_Dcomplex` 값입니다.  
  
## 요구 사항  
  
|루틴|C 헤더|C\+\+ 헤더|  
|--------|----------|--------------|  
|`casinh`, `casinhf`, `casinhl`|\<complex.h\>|\< ccomplex \>|  
  
 호환성에 대한 자세한 내용은 소개 단원의 [호환성](../../c-runtime-library/compatibility.md) 부분을 참조하세요.  
  
## 참고 항목  
 [사전순 함수 참조](../../c-runtime-library/reference/crt-alphabetical-function-reference.md)   
 [catanh, catanhf, catanhl](../../c-runtime-library/reference/catanh-catanhf-catanhl.md)   
 [ctanh, ctanhf, ctanhl](../../c-runtime-library/reference/ctanh-ctanhf-ctanhl.md)   
 [catan, catanf, catanl](../../c-runtime-library/reference/catan-catanf-catanl.md)   
 [csinh를, csinhf csinhl](../../c-runtime-library/reference/csinh-csinhf-csinhl.md)   
 [ccosh를, ccoshf ccoshl](../../c-runtime-library/reference/ccosh-ccoshf-ccoshl.md)   
 [cacosh, cacoshf, cacoshl](../../c-runtime-library/reference/cacosh-cacoshf-cacoshl.md)   
 [cacos, cacosf, cacosl](../../c-runtime-library/reference/cacos-cacosf-cacosl.md)   
 [ctan, ctanf, ctanl](../../c-runtime-library/reference/ctan-ctanf-ctanl.md)   
 [csin, csinf, csinl](../../c-runtime-library/reference/csin-csinf-csinl.md)   
 [casin, casinf, casinl](../../c-runtime-library/reference/casin-casinf-casinl.md)   
 [ccos, ccosf, ccosl](../../c-runtime-library/reference/ccos-ccosf-ccosl.md)   
 [csqrt, csqrtf, csqrtl](../../c-runtime-library/reference/csqrt-csqrtf-csqrtl.md)