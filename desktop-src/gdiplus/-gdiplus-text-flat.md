---
Description: Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.
ms.assetid: 70d35c08-08d9-46a6-a6df-76d989551866
title: Text Functions
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Text Functions

Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h. The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes. It is recommended that you do not directly call the functions in the flat API. Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers. Microsoft Product Support Services will not provide support for code that calls the flat API directly. For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md). The following flat API functions are wrapped by the [**Graphics**](/windows/win32/gdiplusgraphics/nl-gdiplusgraphics-graphics?branch=master) Text C++ class.

## Text Functions and Corresponding Wrapper Methods



| Flat function                                                                                                                                                                                                                                                                   | Wrapper method                                                                                                                                                                                                                                                                                                                                                                        | Remarks                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipDrawString( GpGraphics \*graphics, GDIPCONST WCHAR \*string, INT length, GDIPCONST GpFont \*font, GDIPCONST RectF \*layoutRect, GDIPCONST GpStringFormat \*stringFormat, GDIPCONST GpBrush \*brush )<br/>                                         | [**Status Graphics::DrawString( IN const WCHAR \*string, IN INT length, IN const Font \*font, IN const RectF &layoutRect, IN const StringFormat \*stringFormat, IN const Brush \*brush )**](/windows/win32/Gdiplusgraphics/?branch=master)<br/>                                                                                      | Draws a string based on a font, a layout rectangle, and a format.                                                                                                                                                 |
| GpStatus WINGDIPAPI GdipMeasureString( GpGraphics \*graphics, GDIPCONST WCHAR \*string, INT length, GDIPCONST GpFont \*font, GDIPCONST RectF \*layoutRect, GDIPCONST GpStringFormat \*stringFormat, RectF \*boundingBox, INT \*codepointsFitted, INT \*linesFilled )<br/> | [**Status Graphics::MeasureString( IN const WCHAR \*string, IN INT length, IN const Font \*font, IN const RectF &layoutRect, IN const StringFormat \*stringFormat, OUT RectF \*boundingBox, OUT INT \*codepointsFitted = 0, OUT INT \*linesFilled = 0 ) const**](/windows/win32/Gdiplusgraphics/?branch=master)<br/> | Measures the extent of the string in the specified font, format, and layout rectangle.                                                                                                                            |
| GpStatus WINGDIPAPI GdipMeasureCharacterRanges( GpGraphics \*graphics, GDIPCONST WCHAR \*string, INT length, GDIPCONST GpFont \*font, GDIPCONST RectF &layoutRect, GDIPCONST GpStringFormat \*stringFormat, INT regionCount, GpRegion \*\*regions )<br/>                  | [**Status Graphics::MeasureCharacterRanges( IN const WCHAR \*string, IN INT length, IN const Font \*font, IN const RectF &layoutRect, IN const StringFormat \*stringFormat, IN INT regionCount, OUT Region \*regions ) const**](/windows/win32/Gdiplusgraphics/nf-gdiplusgraphics-graphics-measurecharacterranges?branch=master)<br/>                                  | Gets a set of regions each of which bounds a range of character positions within a string.                                                                                                                        |
| GpStatus WINGDIPAPI GdipDrawDriverString( GpGraphics \*graphics, GDIPCONST UINT16 \*text, INT length, GDIPCONST GpFont \*font, GDIPCONST GpBrush \*brush, GDIPCONST PointF \*positions, INT flags, GDIPCONST GpMatrix \*matrix )<br/>                                     | [**Status Graphics::DrawDriverString( IN const UINT16 \*text, IN INT length, IN const Font \*font, IN const Brush \*brush, IN const PointF \*positions, IN INT flags, IN const Matrix \*matrix )**](/windows/win32/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawdriverstring?branch=master)<br/>                                                                           | Draws characters at the specified positions. The method gives the client complete control over the appearance of text. The method assumes that the client has already set up the format and layout to be applied. |
| GpStatus WINGDIPAPI GdipMeasureDriverString( GpGraphics \*graphics, GDIPCONST UINT16 \*text, INT length, GDIPCONST GpFont \*font, GDIPCONST PointF \*positions, INT flags, GDIPCONST GpMatrix \*matrix, RectF \*boundingBox )<br/>                                        | [**Status Graphics::MeasureDriverString( IN const UINT16 \*text, IN INT length, IN const Font \*font, IN const PointF \*positions, IN INT flags, IN const Matrix \*matrix, OUT RectF \*boundingBox ) const**](/windows/win32/Gdiplusgraphics/nf-gdiplusgraphics-graphics-measuredriverstring?branch=master)<br/>                                                        | Measures the bounding box for the specified characters and their corresponding positions.                                                                                                                         |



 

 

 



