---
Description: Retrieve the device associated with the sprite object.
ms.assetid: 9119b232-22c8-4b05-b584-ce176370ca97
title: ID3DX10SpriteGetDevice method
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# ID3DX10Sprite::GetDevice method

Retrieve the device associated with the sprite object.

## Syntax


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## Parameters

<dl> <dt>

*ppDevice* \[out\]
</dt> <dd>

Type: **[**ID3D10Device**](/windows/win32/D3D10/nn-d3d10-id3d10device?branch=master)\*\***

Address of a pointer to an ID3D10Device interface, representing the Direct3D device object associated with the sprite object.

</dd> </dl>

## Return value

Type: **[**HRESULT**](455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

If the method succeeds, the return value is S\_OK. If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.

## Remarks

Calling this method will increase the internal reference count on the ID3D10Device interface.

## Requirements



|                    |                                                                                       |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Library<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## See also

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 



