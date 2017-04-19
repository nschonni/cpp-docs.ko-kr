---
title: "fread | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
apiname: 
  - "fread"
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
  - "api-ms-win-crt-stdio-l1-1-0.dll"
apitype: "DLLExport"
f1_keywords: 
  - "fread"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "데이터[C++], 입력 스트림에서 읽기"
  - "fread 함수"
  - "데이터 읽기[C++], 입력 스트림에서"
  - "스트림[C++], 데이터 읽기"
ms.assetid: 9a3c1538-93dd-455e-ae48-77c1e23c53f0
caps.latest.revision: 17
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 17
---
# fread
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

스트림에서 데이터를 읽습니다.  
  
## 구문  
  
```  
size_t fread(   
   void *buffer,  
   size_t size,  
   size_t count,  
   FILE *stream   
);  
```  
  
#### 매개 변수  
 `buffer`  
 출력을 위한 저장소 위치  
  
 `size`  
 바이트에서 항목의 크기입니다.  
  
 `count`  
 읽을 수 있는 항목의 최대 수입니다.  
  
 `stream`  
 `FILE` 구조체에 대한 포인터입니다.  
  
## 반환 값  
 실제로 읽을 수 있는 최대 항목의 수를 `fread` 로 반환하는데, 이것은 오류가 발생하거나 `count`*.* 에 도달하기 전에 파일의 끝에 맞닥뜨린 경우 `count` 보다 더 적을 수 있습니다. 파일의 끝에 대한 조건으로 읽기 오류를 구별하기 위해 `feof` 또는 `ferror` 함수를 사용합니다.  만일 `size` 또는 `count` 이 0 이라면 `fread` 는 0을 반환하고 버퍼의 내용을 바꾸지않습니다.  만일 `stream` 또는 `buffer` 가 null 포인터인 경우, [매개 변수 유효성 검사](../../c-runtime-library/parameter-validation.md) 에 설명된대로 `fread` 가 잘못된 매개변수 처리기를 호출합니다.  계속해서 실행하도록 허용된 경우, 함수는 `errno` 를 `EINVAL` 로 설정하고 0을 반환합니다.  
  
 이러한 오류 코드 및 기타 오류 코드에 대한 자세한 내용은 [\_doserrno, errno, \_sys\_errlist 및 \_sys\_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md)을 참조하십시오.  
  
## 설명  
 `fread` 함수는 입력 `stream` 으로부터 `size` 바이트들의 `count` 항목들을 읽고 `buffer`*.*에 저장합니다. \(만일 있는 경우\) `stream` 과 연결된 파일 포인터는 실제로 읽은 바이트의 수만큼 증가합니다.  만일 텍스트 모드에서 주어진 스트림이 열린 경우, 캐리지는 반환합니다– 줄 바꿈 쌍은 단일 줄 바꿈 문자로 바뀝니다.  이 교체는 파일 포인터 또는 반환 값에는 영향을 미치지 않습니다.  파일 포인터 위치는 만일 오류가 발생하는 경우 결정되지 않습니다.  부분적으로 읽은 항목의 값은 결정될 수 없습니다.  
  
 이 함수는 다른 스레드를 잠급니다.  만일 비잠금 버전이 필요한 경우, `_fread_nolock`을 사용하세요.  
  
## 요구 사항  
  
|Function|필수 헤더|  
|--------------|-----------|  
|`fread`|\<stdio.h\>|  
  
 호환성에 대한 자세한 내용은 소개 단원의 [호환성](../../c-runtime-library/compatibility.md) 부분을 참조하십시오.  
  
## 예제  
  
```  
// crt_fread.c  
// This program opens a file named FREAD.OUT and  
// writes 25 characters to the file. It then tries to open  
// FREAD.OUT and read in 25 characters. If the attempt succeeds,  
// the program displays the number of actual items read.  
  
#include <stdio.h>  
  
int main( void )  
{  
   FILE *stream;  
   char list[30];  
   int  i, numread, numwritten;  
  
   // Open file in text mode:  
   if( fopen_s( &stream, "fread.out", "w+t" ) == 0 )  
   {  
      for ( i = 0; i < 25; i++ )  
         list[i] = (char)('z' - i);  
      // Write 25 characters to stream   
      numwritten = fwrite( list, sizeof( char ), 25, stream );  
      printf( "Wrote %d items\n", numwritten );  
      fclose( stream );  
  
   }  
   else  
      printf( "Problem opening the file\n" );  
  
   if( fopen_s( &stream, "fread.out", "r+t" ) == 0 )  
   {  
      // Attempt to read in 25 characters   
      numread = fread( list, sizeof( char ), 25, stream );  
      printf( "Number of items read = %d\n", numread );  
      printf( "Contents of buffer = %.25s\n", list );  
      fclose( stream );  
   }  
   else  
      printf( "File could not be opened\n" );  
}  
```  
  
  **25개 항목 작성했습니다.**  
**읽은 항목 수 \= 25**  
**버퍼의 내용 \= zyxwvutsrqponmlkjihgfedcb**   
## 해당 .NET Framework 항목  
 [System::IO::FileStream::Read](https://msdn.microsoft.com/en-us/library/system.io.filestream.read.aspx)  
  
## 참고 항목  
 [스트림 I\/O](../../c-runtime-library/stream-i-o.md)   
 [fwrite](../../c-runtime-library/reference/fwrite.md)   
 [\_read](../../c-runtime-library/reference/read.md)