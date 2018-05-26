---
Description: Multiple Render Targets (MRT) refers to the ability to render to multiple surfaces (see IDirect3D9Surface) with a single draw call.
ms.assetid: ae48c5ce-b7f5-4189-8b04-880836be3fe0
title: Multiple Render Targets (Direct3D 9)
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Multiple Render Targets (Direct3D 9)

Multiple Render Targets (MRT) refers to the ability to render to multiple surfaces (see [**IDirect3D9Surface**](/windows/win32/d3d9helper/nn-d3d9-idirect3dsurface9?branch=master)) with a single draw call. These surfaces can be created independently of each other. Render targets can be set using [**IDirect3DDevice9::SetRenderTarget**](/windows/win32/d3d9helper/nf-d3d9-idirect3ddevice9-setrendertarget?branch=master).

Multiple render targets have the following restrictions:

-   All render target surfaces used together must have the same bit depth but can be of different formats, unless the D3DPMISCCAPS\_MRTINDEPENDENTBITDEPTHS cap is set.
-   All surfaces of a multiple render target should have the same width and height.
-   Some implementations cannot perform post-pixel shader operations on multiple render targets, including: no dithering, alpha test, no fogging, no blending or masking, except the z-test and stencil test. Devices that can support post-pixel shader operations set the cap bit to D3DPMISCCAPS\_MRTPOSTPIXELSHADERBLENDING.

    When the D3DPMISCCAPS\_MRTPOSTPIXELSHADERBLENDING cap is set, you must first consult the [**IDirect3D9::CheckDeviceFormat**](/windows/win32/d3d9helper/nf-d3d9-idirect3d9-checkdeviceformat?branch=master) with the USAGE\_QUERY\_POSTPIXELSHADER\_BLENDING result for the specific surface format. If false, no post-pixel shader blending operations will be available for that specific surface format. If true, the device is expected to apply the same state to all simultaneous render targets as follows:

    -   Alpha blend: The color value in oCi is blended with the ith render target.
    -   Alpha test: Comparison will happen with oC0. If the comparison fails, the pixel test is terminated for all render targets.
    -   Fog: Render target 0 will get fogged. Other render targets are undefined. Implementations can choose to fog them all using the same state.
    -   Dithering: Undefined.

-   No antialiasing is supported.
-   Some of the implementations do not apply the output write mask (D3DRS\_COLORWRITEENABLE). Those that can, have independent color write masks. This is expressed using a new capability bit. The number of independent color write masks available will be equal to the maximum number of elements the device is capable of.

New hardware caps:


```
D3DCAPS9.NumSimultaneousRTs         
// The value is 1 for all hardware except those that  
//   can support this feature. It is never 0.
D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS - True if the hardware can support it
D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING - True if the hardware can support it
```



## Related topics

<dl> <dt>

[Pixel Pipeline](pixel-pipeline.md)
</dt> </dl>

 

 


