---
title: Pragma Directives
description: RC does not support the pragma directives supported by the C/C++ compiler.
ms.assetid: c7a944c0-a3d4-4568-a9ac-c338f0eaa427
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Pragma Directives

RC does not support the pragma directives supported by the C/C++ compiler. However, RC does support the following pragma directive for changing the code page:

``` syntax
#pragma code_page( [ DEFAULT | CodePageNum ] )
```

This pragma is not supported in an included resource file (.rc). Therefore, if you have a parent .rc file and it includes .rc files for multiple languages, use this pragma before including another .rc file rather than using it in the included .rc file itself. This is demonstrated in the following example.

``` syntax
#include "English.rc"
#pragma code_page(932)
#include "Japanese.rc"
```

For a list of values for CodePageNum, see [Code Page Identifiers](_win32_code_page_identifiers).

 

 



