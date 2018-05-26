---
Description: The Folders property accesses a FaxFolders configuration object. You can use the object to access the folders, jobs, and messages on a connected fax server.
ms.assetid: 9541c67e-e257-4a74-a4a2-d718cd2260d2
title: FaxServer.Folders property
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# FaxServer.Folders property

The **Folders** property accesses a [**FaxFolders**](-mfax-faxfolders.md) configuration object. You can use the object to access the folders, jobs, and messages on a connected fax server.

This property is read-only.

## Syntax


```VB
Property Folders As FaxFolders
```



## Property value

A [**FaxFolders**](-mfax-faxfolders.md) object.

## Remarks

The folders that are accessible will depend on which privileges the user has. Users can always see their own inbound and outbound faxes. The tables below show what other faxes they can access depending on their privilege level.



Windows Server 2003

[**farQUERY\_IN\_ARCHIVE**](/windows/previous-versions/FaxComex/ne-faxcomex-fax_access_rights_enum?branch=master)

The user can view all fax messages in the incoming archive.

[**farMANAGE\_IN\_ARCHIVE**](/windows/previous-versions/FaxComex/ne-faxcomex-fax_access_rights_enum?branch=master)

The user can manage all fax messages in the incoming archive.

[**farQUERY\_OUT\_ARCHIVE**](/windows/previous-versions/FaxComex/ne-faxcomex-fax_access_rights_enum?branch=master)

The user can view all fax messages in the outgoing archive.

[**farMANAGE\_OUT\_ARCHIVE**](/windows/previous-versions/FaxComex/ne-faxcomex-fax_access_rights_enum?branch=master)

The user can manage all fax messages in the outgoing archive.



 



Windows Vista

[**far2MANAGE\_RECEIVE\_FOLDER**](/windows/previous-versions/FaxComex/ne-faxcomex-fax_access_rights_enum_2?branch=master)

The user can view and manage fax messages in the incoming archive that includes his own messages and unassigned messages.

[**farQUERY\_IN\_ARCHIVE**](/windows/previous-versions/FaxComex/ne-faxcomex-fax_access_rights_enum?branch=master) or [**far2QUERY\_ARCHIVES**](/windows/previous-versions/FaxComex/ne-faxcomex-fax_access_rights_enum_2?branch=master)

The user can view all fax messages in the incoming archive, including his own messages, unassigned messages, and messages assigned to others.

[**farMANAGE\_IN\_ARCHIVE**](/windows/previous-versions/FaxComex/ne-faxcomex-fax_access_rights_enum?branch=master) or [**far2MANAGE\_ARCHIVES**](/windows/previous-versions/FaxComex/ne-faxcomex-fax_access_rights_enum_2?branch=master)

The user can manage all fax messages in the incoming archive, including his own messages, unassigned messages, and messages assigned to others.

[**farQUERY\_OUT\_ARCHIVE**](/windows/previous-versions/FaxComex/ne-faxcomex-fax_access_rights_enum?branch=master) or [**far2QUERY\_OUT\_JOBS**](/windows/previous-versions/FaxComex/ne-faxcomex-fax_access_rights_enum_2?branch=master)

The user can view all fax messages in the outgoing archive, including his own messages, unassigned messages, and messages assigned to others.

[**farMANAGE\_OUT\_ARCHIVE**](/windows/previous-versions/FaxComex/ne-faxcomex-fax_access_rights_enum?branch=master) or [**far2MANAGE\_OUT\_JOBS**](/windows/previous-versions/FaxComex/ne-faxcomex-fax_access_rights_enum_2?branch=master)

The user can manage all fax messages in the outgoing archive, including his own messages, unassigned messages, and messages assigned to others.



 

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows XP \[desktop apps only\]<br/>                                             |
| Minimum supported server<br/> | Windows Server 2003 \[desktop apps only\]<br/>                                    |
| Header<br/>                   | <dl> <dt>FaxComex.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Fxscomex.dll</dt> </dl> |



## See also

<dl> <dt>

[Visual Basic Example](-mfax-opening-a-fax-from-the-incoming-archive.md)
</dt> <dt>

[**FaxServer**](-mfax-faxserver.md)
</dt> <dt>

[**IFaxServer**](/windows/previous-versions/FaxComex/nn-faxcomex-ifaxserver?branch=master)
</dt> </dl>

 

 



