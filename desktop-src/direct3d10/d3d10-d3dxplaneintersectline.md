---
Description: Finds the intersection between a plane and a line.
ms.assetid: aea1c4e1-f8c0-46df-bb33-2b517396d69e
title: D3DXPlaneIntersectLine function
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# D3DXPlaneIntersectLine function

Finds the intersection between a plane and a line.

## Syntax


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## Parameters

<dl> <dt>

*pOut* \[in, out\]
</dt> <dd>

Type: **[**D3DXVECTOR3**](direct3d9.d3dxvector3)\***

Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), identifying the intersection between the specified plane and line.

</dd> <dt>

*pP* \[in\]
</dt> <dd>

Type: **const [**D3DXPLANE**](direct3d9.d3dxplane)\***

Pointer to the source [**D3DXPLANE**](d3d10-d3dxplane.md).

</dd> <dt>

*pV1* \[in\]
</dt> <dd>

Type: **const [**D3DXVECTOR3**](direct3d9.d3dxvector3)\***

Pointer to a source D3DXVECTOR3 structure, defining a line starting point.

</dd> <dt>

*pV2* \[in\]
</dt> <dd>

Type: **const [**D3DXVECTOR3**](direct3d9.d3dxvector3)\***

Pointer to a source D3DXVECTOR3 structure, defining a line ending point.

</dd> </dl>

## Return value

Type: **[**D3DXVECTOR3**](direct3d9.d3dxvector3)\***

Pointer to a D3DXVECTOR3 structure that is the intersection between the specified plane and line.

## Remarks

If the line is parallel to the plane, **NULL** is returned.

The return value for this function is the same value returned in the pOut parameter. In this way, the D3DXPlaneIntersectLine function can be used as a parameter for another function.

## Requirements



|                    |                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## See also

<dl> <dt>

[Math Functions](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 



