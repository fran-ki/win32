---
title: VML Orientation Attribute
description: VML Orientation Attribute
ms.assetid: 62298908-6e88-470d-bca2-0cfc1a38c2eb
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# VML Orientation Attribute

This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9. Webpages and applications that rely on VML should be [migrated to SVG](http://go.microsoft.com/fwlink/p/?LinkID=236964) or other widely supported standards.

> [!Note]  
> As of December 2011, this topic has been archived. As a result, it is no longer actively maintained. For more information, see [Archived Content](https://msdn.microsoft.com/library/hh772377). For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](http://go.microsoft.com/fwlink/p/?linkid=204313).

 

Specifies the vector around which a shape can be rotated. Read/write. **VgVector3D**.

**Applies To**

[Extrusion](msdn-online-vml-extrusion-element.md)

**Tag Syntax**

&lt;o: *element* orientation=" *expression* "&gt;

**Script Syntax**

*element* .orientation="*expression*"

*expression*=*element*.orientation

**Remarks**

Use the [OrientationAngle](msdn-online-vml-orientationangle-attribute.md) attribute to specify the amount of rotation around this vector. Default value is 100,0,0.

*Microsoft Office Extensions Attribute*

 

 



