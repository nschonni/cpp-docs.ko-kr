---
title: IRegistrar 인터페이스 | Microsoft Docs
ms.custom: ''
ms.date: 2/1/2017
ms.technology:
- cpp-atl
ms.topic: reference
f1_keywords:
- IRegistrar
- ATLIFASE/ATL::IRegistrar
- ATLIFASE/ATL::IRegistrar::ResourceRegisterSz
- ATLIFASE/ATL::IRegistrar::ResourceUnregisterSz
- ATLIFASE/ATL::IRegistrar::FileRegister
- ATLIFASE/ATL::IRegistrar::FileUnregister
- ATLIFASE/ATL::IRegistrar::StringRegister
- ATLIFASE/ATL::IRegistrar::StringUnregister
- ATLIFASE/ATL::IRegistrar::ResourceRegister
- ATLIFASE/ATL::IRegistrar::ResourceUnregister
dev_langs:
- C++
helpviewer_keywords:
- Iregistrar Interface
ms.assetid: e88c04b7-0c93-4ae8-aeb9-ecd78f87421e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 10e5a6fda373c79b85dac5cfcf19739276a5c12f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46039519"
---
# <a name="iregistrar-interface"></a>IRegistrar 인터페이스

이 인터페이스 atliface.h에 정의 되어 있으며 내부적으로 사용 됩니다 CAtlModule 멤버 함수에 의해와 같은 [UpdateRegistryFromResourceD](catlmodule-class.md#updateregistryfromresourced)합니다.

## <a name="syntax"></a>구문

```
typedef interface IRegistrar IRegistrar;
```

## <a name="remarks"></a>설명

항목을 참조 하세요 [를 사용 하 여 대체 가능 매개 변수 (The 등록자 전처리기)](../../atl/using-replaceable-parameters-the-registrar-s-preprocessor.md) 대 한 자세한 내용은 합니다.

## <a name="members"></a>멤버

### <a name="public-methods"></a>Public 메서드

|이름|설명|
|----------|-----------------|
|[IRegistrar::ResourceRegisterSz](#resourceregistersz)|리소스를 등록합니다. |
|[IRegistrar::ResourceUnregisterSz](#resourceunregistersz)| 리소스 등록을 취소 합니다.|
|[IRegistrar::FileRegister](#fileregister)|파일을 등록합니다.|
|[IRegistrar::FileUnregister](#fileunregister)|파일을 등록 취소합니다.|
|[IRegistrar::StringRegister](#stringregister)|문자열을 등록합니다.|
|[IRegistrar::StringUnregister](#stringunregister)|문자열을 등록 취소|
|[IRegistrar::ResourceRegister](#resourceregister)|리소스를 등록합니다.|
|[IRegistrar::ResourceUnregister](#resourceunregister)|리소스 등록을 취소 합니다.|

## <a name="requirements"></a>요구 사항

**헤더:** atlifase.h

##  <a name="resourceregistersz"></a>  IRegistrar::ResourceRegisterSz

리소스를 등록합니다.

```
virtual HRESULT STDMETHODCALLTYPE ResourceRegisterSz(
    /* [in] */ _In_z_ LPCOLESTR resFileName,
    /* [in] */ _In_z_ LPCOLESTR szID,
    /* [in] */ _In_z_ LPCOLESTR szType) = 0;
```

##  <a name="resourceunregistersz"></a>  IRegistrar::ResourceUnregisterSz

리소스 등록을 취소 합니다.

```
virtual HRESULT STDMETHODCALLTYPE ResourceUnregisterSz(
    /* [in] */ _In_z_ LPCOLESTR resFileName,
    /* [in] */ _In_z_ LPCOLESTR szID,
    /* [in] */ _In_z_ LPCOLESTR szType) = 0;
```

##  <a name="fileregister"></a>  IRegistrar::FileRegister

파일을 등록합니다.

```
virtual HRESULT STDMETHODCALLTYPE FileRegister(
    /* [in] */ _In_z_ LPCOLESTR fileName) = 0;
```

##  <a name="fileunregister"></a>  IRegistrar::FileUnregister

파일을 등록 취소합니다.

```
virtual HRESULT STDMETHODCALLTYPE FileUnregister(
    /* [in] */ _In_z_ LPCOLESTR fileName) = 0;
```

##  <a name="stringregister"></a>  IRegistrar::StringRegister

지정 된 문자열 데이터를 등록합니다.

```
virtual HRESULT STDMETHODCALLTYPE StringRegister(
    /* [in] */ _In_z_ LPCOLESTR data) = 0;
```

##  <a name="stringunregister"></a>  IRegistrar::StringUnregister

지정 된 문자열 데이터를 등록 취소합니다.

```
virtualHRESULT STDMETHODCALLTYPE StringUnregister(
    /* [in] */ _In_z_ LPCOLESTR data) = 0;
```

##  <a name="resourceregister"></a>  IRegistrar::ResourceRegister

리소스를 등록합니다.

```
virtual HRESULT STDMETHODCALLTYPE ResourceRegister(
    /* [in] */ _In_z_ LPCOLESTR resFileName,
    /* [in] */ _In_ UINT nID,
    /* [in] */ _In_z_ LPCOLESTR szType) = 0;
```

##  <a name="resourceunregister"></a>  IRegistrar::ResourceUnregister

리소스 등록을 취소 합니다.

```
virtualHRESULT STDMETHODCALLTYPE ResourceUnregister(
    /* [in] */ _In_z_ LPCOLESTR resFileName,
    /* [in] */ _In_ UINT nID,
    /* [in] */ _In_z_ LPCOLESTR szType) = 0;
```

## <a name="see-also"></a>참고 항목

[대체 가능 매개 변수 사용(등록자 전처리기)](../../atl/using-replaceable-parameters-the-registrar-s-preprocessor.md)<br/>
[클래스 개요](../../atl/atl-class-overview.md)<br/>
[모듈 클래스](../../atl/atl-module-classes.md)<br/>
[레지스트리 구성 요소 (등록자)](../../atl/atl-registry-component-registrar.md)
