---
title: Nodes and IComponentData
description: The IComponentData interface is closely associated with the functionality of the nodes displayed in the scope pane.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: fa26a602-f27a-4244-811d-c768c9a9f94e
ms.prod: windows-server-dev
ms.technology: microsoft-management-console
ms.tgt_platform: multiple
keywords:
- nodes and IComponentData MMC
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# Nodes and IComponentData

The [**IComponentData**](icomponentdata.md) interface is closely associated with the functionality of the nodes displayed in the scope pane. A snap-in's **IComponentData** object adds items to the scope pane when it receives an [**MMCN\_EXPAND**](mmcn-expand.md) notification from the console through its [**Notify**](icomponentdata-notify.md) method.

While nodes themselves are maintained by MMC after their creation, [**IComponentData**](icomponentdata.md) handles notifications sent to it through its [**Notify**](icomponentdata-notify.md) method when the user performs an action on a particular node.

Snap-ins implement [**IComponentData**](icomponentdata.md) as COM objects. When the user loads a snap-in in an MMC console, MMC creates an instance of the snap-in by creating its **IComponentData** object. There is only one instance of **IComponentData** per instance of a stand-alone snap-in or namespace extension snap-in.

 

 



