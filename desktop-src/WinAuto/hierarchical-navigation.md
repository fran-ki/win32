---
title: Hierarchical Navigation
description: Often clients must move between objects based on their parent-child relationships. For example, a client might already have information about a toolbar control, but not have information about the buttons contained within it.
ms.assetid: 7adf803c-140a-4f7d-8dc5-71abca706800
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Hierarchical Navigation

Often clients must move between objects based on their parent-child relationships. For example, a client might already have information about a toolbar control, but not have information about the buttons contained within it.

The [**IAccessible**](/windows/win32/oleacc/nn-oleacc-iaccessible?branch=master) interface exposes the hierarchical relationships between objects. Clients can navigate from a parent object to its children or from a child object to its parent by calling [**IAccessible::get\_accParent**](/windows/win32/Oleacc/nf-oleacc-iaccessible-get_accparent?branch=master) or [**IAccessible::get\_accChild**](/windows/win32/Oleacc/nf-oleacc-iaccessible-get_accchild?branch=master).

 

 



