---
title: Functions
description: This section contains functions for Windows Touch input.
ms.assetid: 6c64ed75-37ac-47ae-b39e-bdf10d2b5211
keywords:
- Windows Touch,functions
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Functions

This section contains functions for Windows Touch input.

The following functions are used for Windows Touch input.



| Function                                                                                               | Description                                                                                                                             |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**CloseTouchInputHandle**](/windows/win32/winuser/nf-winuser-closetouchinputhandle?branch=master)                                                 | Closes a touch input handle, frees process memory associated with it, and invalidates the handle.                                       |
| [**GetTouchInputInfo**](/windows/win32/winuser/nf-winuser-gettouchinputinfo?branch=master)                                                         | Retrieves detailed information about touch inputs associated with a specific touch input handle.                                        |
| [**IsTouchWindow**](/windows/win32/winuser/nf-winuser-istouchwindow?branch=master)                                                                 | Checks whether a specified window is touch-capable and, optionally, retrieves the modifier flags set for the window's touch capability. |
| [**RegisterTouchWindow**](/windows/win32/winuser/nf-winuser-registertouchwindow?branch=master)                                                     | Registers a window as being touch-capable.                                                                                              |
| [**UnregisterTouchWindow**](/windows/win32/winuser/nf-winuser-unregistertouchwindow?branch=master)                                                 | Registers a window as no longer being touch-capable.                                                                                    |
| [SendMessage, PostMessage, and Related Functions](sendmessage--postmessage--and-related-functions.md) | Contains considerations about forwarding messages.                                                                                      |



 

## Related topics

<dl> <dt>

[Windows Touch Input](multi-touch-input.md)
</dt> <dt>

[Windows Touch Input Programming Guide](guide-multi-touch-input.md)
</dt> </dl>

 

 



