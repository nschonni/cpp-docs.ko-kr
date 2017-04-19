---
title: "_bittestandcomplement, _bittestandcomplement64 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "_bittestandcomplement64"
  - "_bittestandcomplement64_cpp"
  - "_bittestandcomplement_cpp"
  - "_bittestandcomplement"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "_bittestandcomplement 내장"
  - "_bittestandcomplement64 내장"
  - "btc 명령"
ms.assetid: 53fa12dd-835e-4e5d-baec-a431c8678806
caps.latest.revision: 15
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 15
---
# _bittestandcomplement, _bittestandcomplement64
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

**Microsoft 전용**  
  
 주소 `a`의 비트 `b`를 검사하고 현재 값을 반환한 다음 비트를 보수로 설정하는 명령을 생성합니다.  
  
## 구문  
  
```  
unsigned char _bittestandcomplement(    long *a,    long b ); unsigned char _bittestandcomplement64(    __int64 *a,    __int64 b );  
```  
  
#### 매개 변수  
 \[in, out\] `a`  
 검사할 메모리에 대한 포인터입니다.  
  
 \[in\] `b`  
 테스트할 비트 위치입니다.  
  
## 반환 값  
 지정한 위치에 있는 비트입니다.  
  
## 요구 사항  
  
|내장 함수|아키텍처|  
|-----------|----------|  
|`_bittestandcomplement`|x86, ARM, [!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]|  
|`_bittestandcomplement64`|[!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]|  
  
 **헤더 파일** \<intrin.h\>  
  
## 설명  
 이 루틴은 내장 루틴으로만 사용할 수 있습니다.  
  
## 예제  
  
```  
// bittestandcomplement.cpp  
// processor: x86, IPF, x64  
#include <stdio.h>  
#include <intrin.h>  
  
#pragma intrinsic(_bittestandcomplement)  
#ifdef _M_AMD64  
#pragma intrinsic(_bittestandcomplement64)  
#endif  
  
int main()  
{  
   long i = 1;  
   __int64 i64 = 0x1I64;  
   unsigned char result;  
   printf("Initial value: %d\n", i);  
   printf("Testing bit 1\n");  
   result = _bittestandcomplement(&i, 1);  
   printf("Value changed to %d, Result: %d\n", i, result);  
#ifdef _M_AMD64  
   printf("Testing bit 0\n");  
   result = _bittestandcomplement64(&i64, 0);  
   printf("Value changed to %I64d, Result: %d\n", i64, result);  
#endif  
}  
```  
  
## 샘플 출력  
  
```  
Initial value: 1  
Testing bit 1  
Value changed to 3, Result: 0  
Testing bit 0  
Value changed to 0, Result: 1  
```  
  
### Microsoft 전용 종료  
  
## 참고 항목  
 [컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)