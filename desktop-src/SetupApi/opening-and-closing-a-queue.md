---
Description: Before you can queue file operations, you must open a file queue. Calling the SetupOpenFileQueue function returns a handle to a queue file. This handle is used by subsequent queue functions to reference the open queue and add operations to it or scan it.
ms.assetid: 3eeb4f34-c89e-4733-8a8c-54e470a1fd30
title: Opening and Closing a Queue
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Opening and Closing a Queue

Before you can queue file operations, you must open a file queue. Calling the [**SetupOpenFileQueue**](/windows/win32/Setupapi/nf-setupapi-setupopenfilequeue?branch=master) function returns a handle to a queue file. This handle is used by subsequent queue functions to reference the open queue and add operations to it or scan it.

After all the specified file operations have been queued and committed, you must call the [**SetupCloseFileQueue**](/windows/win32/Setupapi/nf-setupapi-setupclosefilequeue?branch=master) function to release resources allocated during the call to [**SetupOpenFileQueue**](/windows/win32/Setupapi/nf-setupapi-setupopenfilequeue?branch=master).

> [!Note]  
> The [**SetupCloseFileQueue**](/windows/win32/Setupapi/nf-setupapi-setupclosefilequeue?branch=master) function does not commit the file queue. Any operations that are uncommitted when **SetupCloseFileQueue** is called will not be performed.

 

 

 


