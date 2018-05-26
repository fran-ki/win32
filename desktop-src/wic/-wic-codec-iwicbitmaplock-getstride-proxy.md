---
Description: Proxy function for the GetStride method.
ms.assetid: 243439f3-2267-4632-b312-75c5ae5eddaa
title: IWICBitmapLock\_GetStride\_Proxy function
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# IWICBitmapLock\_GetStride\_Proxy function

Proxy function for the [**GetStride**](/windows/win32/Wincodec/nf-wincodec-iwicbitmaplock-getstride?branch=master) method.

## Syntax


```C++
HRESULT IWICBitmapLock_GetStride_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbStride
);
```



## Parameters

<dl> <dt>

*THIS\_PTR* \[in\]
</dt> <dd>

Type: **[**IWICBitmapLock**](/windows/win32/Wincodec/nn-wincodec-iwicbitmaplock?branch=master)\***

Pointer to this [**IWICBitmapLock**](/windows/win32/Wincodec/nn-wincodec-iwicbitmaplock?branch=master) object.

</dd> <dt>

*pcbStride* \[out\]
</dt> <dd>

Type: **UINT\***

The bitmap stride.

</dd> </dl>

## Return value

Type: **HRESULT**

If this function succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Remarks

## Requirements



|                                     |                                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows XP with SP2, Windows Vista \[desktop apps only\]<br/>                                                                                              |
| Minimum supported server<br/> | Windows Server 2008 \[desktop apps only\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 



