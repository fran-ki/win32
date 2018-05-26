---
title: ID3DX11EffectClassInstanceVariable GetClassInstance method
description: Gets a class instance.
ms.assetid: dec00a6b-0587-40cf-abae-dd110a639fe0
keywords:
- GetClassInstance method Direct3D 11
- GetClassInstance method Direct3D 11 , ID3DX11EffectClassInstanceVariable interface
- ID3DX11EffectClassInstanceVariable interface Direct3D 11 , GetClassInstance method
topic_type:
- apiref
api_name:
- ID3DX11EffectClassInstanceVariable.GetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# ID3DX11EffectClassInstanceVariable::GetClassInstance method

Gets a class instance.

## Syntax


```C++
HRESULT GetClassInstance(
   ID3D11ClassInstance **ppClassInstance
);
```



## Parameters

<dl> <dt>

*ppClassInstance* 
</dt> <dd>

Type: **[**ID3D11ClassInstance**](/windows/win32/D3D11/nn-d3d11-id3d11classinstance?branch=master)\*\***

Pointer to an [**ID3D11ClassInstance**](/windows/win32/D3D11/nn-d3d11-id3d11classinstance?branch=master) pointer that will be set to class instance.

</dd> </dl>

## Return value

Type: **[**HRESULT**](455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).

## Remarks

> [!Note]  
> The DirectX SDK does not supply any compiled binaries for effects. You must use Effects 11 source to build your effects-type application. For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## Requirements



|                    |                                                                                                                                              |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Library<br/> | <dl> <dt>N/A (An Effects 11 library is available online as shared source.)</dt> </dl> |



## See also

<dl> <dt>

[ID3DX11EffectClassInstanceVariable](id3dx11effectclassinstancevariable.md)
</dt> </dl>

 

 




