---
Description: Creates a context.
ms.assetid: f972ab40-c9e9-4d2a-88f6-4c7817d5533f
title: NtGdiD3DContextCreate function
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# NtGdiD3DContextCreate function

\[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]

Creates a context.

## Syntax


```C++
BOOL APIENTRY NtGdiD3DContextCreate(
  _In_    HANDLE                  hDirectDrawLocal,
  _In_    HANDLE                  hSurfColor,
  _In_    HANDLE                  hSurfZ,
  _Inout_ D3DNTHAL_CONTEXTCREATEI *pdcci
);
```



## Parameters

<dl> <dt>

*hDirectDrawLocal* \[in\]
</dt> <dd>

Handle to a kernel-mode DirectDraw object, previously created with [**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md), representing the device on which the Direct3D context is to be created.

</dd> <dt>

*hSurfColor* \[in\]
</dt> <dd>

Handle to a [**DD\_SURFACE\_LOCAL**](ddstrcts_07a504fc-c8bb-4b48-b825-4da3012e4f95.xml) structure that describes the DirectDraw surface to be used as the rendering target.

</dd> <dt>

*hSurfZ* \[in\]
</dt> <dd>

Handle to a [**DD\_SURFACE\_LOCAL**](ddstrcts_07a504fc-c8bb-4b48-b825-4da3012e4f95.xml) structure that describes the DirectDraw surface to be used as a depth buffer. If this member is **NULL**, no depth buffering is to be performed.

</dd> <dt>

*pdcci* \[in, out\]
</dt> <dd>

Pointer to a [**D3DNTHAL\_CONTEXTCREATEDATA**](d3dstrct_ec3a38f0-8f36-4d40-9974-ba434f0aa42e.xml) structure that contains the information required to create a context and the data that the driver should store in the new context.

</dd> </dl>

## Return value

**NtGdiD3DContextCreate** returns one of the following callback codes.



| Return code                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DDHAL\_DRIVER\_HANDLED**</dt> </dl>    | The driver has performed the operation and returned a valid return code for that operation. If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function. Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.<br/>                                                                                 |
| <dl> <dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt> </dl> | The driver has no comment on the requested operation. If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition. Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.<br/> |



 

## Requirements



|                                     |                                                                                    |
|-------------------------------------|------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 2000 Professional \[desktop apps only\]<br/>                         |
| Minimum supported server<br/> | Windows 2000 Server \[desktop apps only\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## See also

<dl> <dt>

[Graphics Low Level Client Support](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 



