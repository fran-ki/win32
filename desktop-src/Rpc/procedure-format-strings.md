---
title: Procedure Format Strings
description: The following is a complete format string description. It assembles all layers related to different stages of the interpreter evolution.
ms.assetid: fab603ed-1f68-4e0b-9c8d-b9730b8cd389
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Procedure Format Strings

The following is a complete format string description. It assembles all layers related to different stages of the interpreter evolution.

## Procedure Descriptor Overview

A procedure descriptor consists of the header descriptors and the parameter descriptors. The [**–Oi**](https://msdn.microsoft.com/library/windows/desktop/aa367352) style description is considered outdated, in terms of common usage in current RPC programming. The **–Oif** is considered more current.

## The –Oi Style Description

This description consists of the following:

``` syntax
-Oi_style_header_descriptor<>
{-Oi_style_parameter_descriptor<>}*
```

The header would have from 6 to 16 bytes.

The complete description is generated when compiling in [**–Oi**](https://msdn.microsoft.com/library/windows/desktop/aa367352) mode. In [**–Os**](https://msdn.microsoft.com/library/windows/desktop/aa367356) mode, only the parameter descriptors are generated, which are used for conversion. The pickling interpreter uses old style parameter descriptors.

## The –Oif Style Description

The description consists of the following:

``` syntax
-Oif_style_header_descriptor<>
{-Oif_style_parameter_descriptor<6>}*
```

The [**–Oif**](https://msdn.microsoft.com/library/windows/desktop/aa367352) style header descriptor consists of

The –Oif style description is generated when compiling in [**–Oif**](https://msdn.microsoft.com/library/windows/desktop/aa367352) or **–Oicf** mode of the compiler.

``` syntax
-Oi_style_header_descriptor<>
-Oif_extensions_to_the_old_header<6>
```

Some more recent features like pipe, async, and [**/robust**](https://msdn.microsoft.com/library/windows/desktop/aa367363) force the [**–Oicf**](https://msdn.microsoft.com/library/windows/desktop/aa367352) mode of the compiler, when used.

## The Extended –Oif Description

The description consists of the following:

``` syntax
-Oif_style_header_descriptor<>
extensions_to_the_-Oif_header<8>
{-Oif style parameter descriptors<6>}*
```

 

 



