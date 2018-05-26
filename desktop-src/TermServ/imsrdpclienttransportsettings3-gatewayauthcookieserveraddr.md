---
title: IMsRdpClientTransportSettings3 GatewayAuthCookieServerAddr property
description: The server address for cookie-based authentication.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: e00480cd-2133-42ff-8447-6c4234b56bf9
ms.prod: windows-server-dev
ms.technology: remote-desktop-services
ms.tgt_platform: multiple
keywords:
- GatewayAuthCookieServerAddr property Remote Desktop Services
- GatewayAuthCookieServerAddr property Remote Desktop Services , IMsRdpClientTransportSettings3 interface
- IMsRdpClientTransportSettings3 interface Remote Desktop Services , GatewayAuthCookieServerAddr property
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.get_GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.put_GatewayAuthCookieServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# IMsRdpClientTransportSettings3::GatewayAuthCookieServerAddr property

The server address for cookie-based authentication.

This property is read/write.

## Syntax


```C++
HRESULT put_GatewayAuthCookieServerAddr(
  [in]          BSTR bstrProxyAuthCookieServerAddr
);

HRESULT get_GatewayAuthCookieServerAddr(
  [out, retval] BSTR *pbstrProxyAuthCookieServerAddr
);
```



## Property value

The new server address for cookie-based authentication.

## Requirements



|                                     |                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 7<br/>                                                                   |
| Minimum supported server<br/> | Windows Server 2008<br/>                                                         |
| Type library<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## See also

<dl> <dt>

[**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 




