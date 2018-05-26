---
Description: Refreshes FaxSecurity2 object information from the fax server.
ms.assetid: 49a5e89d-26af-4f78-b220-b3a539c28959
title: FaxSecurity2.Refresh method
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# FaxSecurity2.Refresh method

Refreshes [**FaxSecurity2**](-mfax-faxsecurity2.md) object information from the fax server.

## Syntax


```VB
FaxSecurity2.Refresh() As Long
```



## Parameters

This method has no parameters.

## Remarks

When the **Refresh** method is called, any configuration changes made after the last [**Save**](-mfax-faxsecurity2-save-vb.md) method call are lost.

To use this method, a user must have the [****far2QUERY\_CONFIG****](/windows/previous-versions/FaxComex/ne-faxcomex-fax_access_rights_enum_2?branch=master) access right.

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>                                          |
| Minimum supported server<br/> | Windows Server 2008 \[desktop apps only\]<br/>                                    |
| Header<br/>                   | <dl> <dt>FaxComex.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Fxscomex.dll</dt> </dl> |



## See also

<dl> <dt>

[**FaxSecurity2**](-mfax-faxsecurity2.md)
</dt> <dt>

[**IFaxSecurity2**](/windows/previous-versions/FaxComex/nn-faxcomex-ifaxsecurity2?branch=master)
</dt> </dl>

 

 



