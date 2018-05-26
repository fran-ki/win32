---
Description: Remapping is the process of converting the colors in an image according to a color remap table. The color remap table is an array of ColorMap structures. Each ColorMap structure in the array has an oldColor member and a newColor member.
ms.assetid: 2b56ccd5-b9f3-4c5e-8a0b-4b3d1f2b7122
title: Using a Color Remap Table
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Using a Color Remap Table

Remapping is the process of converting the colors in an image according to a color remap table. The color remap table is an array of [**ColorMap**](/windows/win32/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap?branch=master) structures. Each **ColorMap** structure in the array has an **oldColor** member and a **newColor** member.

When GDI+ draws an image, each pixel of the image is compared to the array of old colors. If a pixel's color matches an old color, its color is changed to the corresponding new color. The colors are changed only for rendering — the color values of the image itself (stored in an [**Image**](/windows/win32/gdiplusheaders/nl-gdiplusheaders-image?branch=master) or [**Bitmap**](/windows/win32/gdiplusheaders/nl-gdiplusheaders-bitmap?branch=master) object) are not changed.

To draw a remapped image, initialize an array of [**ColorMap**](/windows/win32/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap?branch=master) structures. Pass the address of that array to the [**ImageAttributes::SetRemapTable**](/windows/win32/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable?branch=master) method of an [**ImageAttributes**](/windows/win32/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes?branch=master) object, and then pass the address of the **ImageAttributes** object to the [DrawImage Methods](/windows/win32/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(in image,in const point &)?branch=master) method of a [**Graphics**](/windows/win32/gdiplusgraphics/nl-gdiplusgraphics-graphics?branch=master) object.

The following example creates an [**Image**](/windows/win32/gdiplusheaders/nl-gdiplusheaders-image?branch=master) object from the file RemapInput.bmp. The code creates a color remap table that consists of a single [**ColorMap**](/windows/win32/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap?branch=master) structure. The **oldColor** member of the **ColorMap** structure is red, and the **newColor** member is blue. The image is drawn once without remapping and once with remapping. The remapping process changes all the red pixels to blue.


```
Image            image(L"RemapInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
ColorMap         colorMap[1];

colorMap[0].oldColor = Color(255, 255, 0, 0);  // opaque red
colorMap[0].newColor = Color(255, 0, 0, 255);  // opaque blue

imageAttributes.SetRemapTable(1, colorMap, ColorAdjustTypeBitmap);

graphics.DrawImage(&amp;image, 10, 10, width, height);

graphics.DrawImage(
   &amp;image, 
   Rect(150, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &amp;imageAttributes);
```



The following illustration shows the original image on the left and the remapped image on the right.

![illustration showing two versions of a multicolored image; the red region in the first version is blue in the second version](images/colortrans7.png)

 

 


