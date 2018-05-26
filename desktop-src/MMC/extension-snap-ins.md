---
title: Extension Snap-ins
description: An extension snap-in can support any or all of the following extension types
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: cc084730-091f-4132-a25b-deab5aa3d9c4
ms.prod: windows-server-dev
ms.technology: microsoft-management-console
ms.tgt_platform: multiple
keywords:
- extension snap-ins MMC
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# Extension Snap-ins

An extension snap-in can support any or all of the following extension types:

-   Namespace extension
-   Context menu extension
-   Toolbar extension
-   Menu button extension
-   Property page extension
-   Taskpad extension

Namespace extensions add scope items to a primary snap-in's scope pane. Namespace extensions must implement the [**IComponentData**](icomponentdata.md) interface. Non-namespace extensions — context menu, toolbar, menu button, property page, and taskpad extensions — do not add scope items to a primary snap-in's scope pane, and consequently they do not need to implement **IComponentData**.

Context menu extensions implement [**IExtendContextMenu**](iextendcontextmenu.md); toolbar and menu button extensions implement [**IControlbar**](icontrolbar.md). Property page extensions implement [**IExtendPropertySheet2**](iextendpropertysheet2.md). Finally, taskpad extensions implement the [**IExtendTaskpad**](iextendtaskpad.md) interface.

For detailed information about interface and other requirements for extension snap-ins, see [Working with Extension Snap-ins](working-with-extension-snap-ins.md).

 

 



