---
title: HTTP.SYS/IIS Web Server
ms.assetid: 1e9632fc-1f07-46c3-83fd-96f9321427f8
description: 
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# HTTP.SYS/IIS Web Server

Components may utilize http.sys or their own object hosted by IIS. The following rule is required for this:

dir="in" protocol="6" lport="&lt;*SPECIFY PORT USED HERE: CAN BE 80, 443, or CUSTOM*&gt;" binary="System"

 

 



