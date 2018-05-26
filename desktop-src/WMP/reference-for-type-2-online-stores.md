---
title: Reference for Type 2 Online Stores
description: Reference for Type 2 Online Stores
ms.assetid: b3f580cc-b02d-4312-a7a1-a35778a222bc
keywords:
- Windows Media Player online stores,reference
- online stores,reference
- type 2 online stores,reference
- reference for type 2 online stores
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Reference for Type 2 Online Stores

> [!Note]  
> This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.

 

Windows Media Player 10 or later provides objects, interfaces, properties, and methods that support type 2 online stores. The following sections document these in detail.



| Section                                                                                                        | Description                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IWMPSubscriptionService Interface](/windows/win32/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice?branch=master)                                               | Provides methods to augment digital rights management (DRM) and initiate background processes.                                                                              |
| [IWMPSubscriptionService2 Interface](/windows/win32/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2?branch=master)                                             | Provides methods to initiate background processes, to provide information about online store activity, and to provide a pointer to the Windows Media Player core interface. |
| [IWMPSubscriptionServiceCallback Interface](/windows/win32/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback?branch=master)                               | Defines a method that online stores use to notify Windows Media Player when a background process is completed.                                                              |
| [WMPNotifySubscriptionPluginAddRemove](/windows/win32/contentpartner/nf-contentpartner-wmpnotifysubscriptionpluginaddremove?branch=master)                               | A function used to notify Windows Media Player that a plug-in has been installed or uninstalled.                                                                            |
| [DownloadCollection Object](downloadcollection-object.md)                                                     | Provides methods and properties to manage collections of download items.                                                                                                    |
| [DownloadItem Object](downloaditem-object.md)                                                                 | Provides methods and properties relating to download requests.                                                                                                              |
| [DownloadManager Object](downloadmanager-object.md)                                                           | Provides methods to manage download collections.                                                                                                                            |
| [External Object for Type 2 Online Stores](external-object-for-type-2-online-stores.md)                       | Provides properties, methods, and an event accessible from online store webpages.                                                                                           |
| [Enumerations for Type 2 Online Stores](enumerations-for-type-2-online-stores.md)                             | Describes enumerations used by online stores.                                                                                                                               |
| [Windows Media Player BITS Job Convention](windows-media-player-bits-job-convention.md)                       | Describes a convention for using the Background Intelligent Transfer Service (BITS).                                                                                        |
| [Registry Keys and Entries for a Type 2 Online Store](registry-keys-and-entries-for-a-type-2-online-store.md) | Describes registry entries that an online store must create in the registry on the user's computer.                                                                         |



 

## Related topics

<dl> <dt>

[**Type 2 Online Stores**](type-2-online-stores.md)
</dt> </dl>

 

 



