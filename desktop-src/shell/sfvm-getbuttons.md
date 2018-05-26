---
Description: Allows the callback object to specify the buttons to be added to the toolbar. Used by IShellFolderViewCBMessageSFVCB.
ms.assetid: 0c0dbf61-9da9-4bcc-bad9-92c3f78db78f
title: SFVM\_GETBUTTONS message
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# SFVM\_GETBUTTONS message

Allows the callback object to specify the buttons to be added to the toolbar. Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/Shlobj/?branch=master).


```C++
SFVM_GETBUTTONS 

    wParam = (WPARAM)(DWORD) idCmdFirst,cbtnMax;

    lParam = (LPARAM)(LPTBBUTTON) pbtn;

            
```



## Parameters

<dl> <dt>

*idCmdFirst\_cbtnMax* \[in\]
</dt> <dd>

Contains two 16-bit values packed into the parameter with the [**MAKEWPARAM**](winmsg.makewparam) macro. The low-order word contains the initial command ID. The high-order word contains the number of buttons to be added, as specified in the preceding [**SFVM\_GETBUTTONINFO**](sfvm-getbuttoninfo.md) message.

</dd> <dt>

*pbtn* \[out\]
</dt> <dd>

The address of an array of [**TBBUTTON**](controls.TBBUTTON) structures, one for each button to be added to the toolbar.

</dd> </dl>

## Remarks

This message is preceded by a [**SFVM\_GETBUTTONINFO**](sfvm-getbuttoninfo.md) message. The callback object must handle that message to specify the number of buttons and where they are to be placed on the toolbar. Depending on how the callback object responds to the **SFVM\_GETBUTTONINFO** message, the buttons specified by *pbtn* parameter will be appended or prepended to the system folder view object's standard buttons, or replace the standard set.

## Requirements



|                                     |                                                                                     |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 2000 Professional \[desktop apps only\]<br/>                          |
| Minimum supported server<br/> | Windows 2000 Server \[desktop apps only\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 



