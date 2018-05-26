---
Description: Begins a scene.
ms.assetid: 8125c592-b985-42f7-8644-59ba93a1c517
title: ID3DXRenderToSurfaceBeginScene method
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# ID3DXRenderToSurface::BeginScene method

Begins a scene.

## Syntax


```C++
HRESULT BeginScene(
  [in]       LPDIRECT3DSURFACE9 pSurface,
  [in] const D3DVIEWPORT9       *pViewport
);
```



## Parameters

<dl> <dt>

*pSurface* \[in\]
</dt> <dd>

Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/d3d9helper/nn-d3d9-idirect3dsurface9?branch=master)**

Pointer to an [**IDirect3DSurface9**](/windows/win32/d3d9helper/nn-d3d9-idirect3dsurface9?branch=master) interface, representing the render surface.

</dd> <dt>

*pViewport* \[in\]
</dt> <dd>

Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***

Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, describing the viewport for the scene.

</dd> </dl>

## Return value

Type: **[**HRESULT**](455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

If the method succeeds, the return value is D3D\_OK. If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL.D3DERR\_OUTOFVIDEOMEMORY D3DXERR\_INVALIDDATA E\_OUTOFMEMORY

## Requirements



|                    |                                                                                        |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## See also

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> <dt>

[**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md)
</dt> </dl>

 

 



