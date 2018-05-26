---
title: Assembling Query Strings
description: In Active Directory, using specific filtering criteria can boost search performance. This is because Active Directory evaluates all predicates, identifies the indices, and then selects one index likely to yield the smallest set of returned values.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\mbaldwin
ms.assetid: 4139eedb-1383-4654-9b40-5e294a71be24
ms.prod: windows-server-dev
ms.technology: active-directory-domain-services
ms.tgt_platform: multiple
keywords:
- Assembling Query Strings ADSI
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# Assembling Query Strings

In Active Directory, using specific filtering criteria can boost search performance. This is because Active Directory evaluates all predicates, identifies the indices, and then selects one index likely to yield the smallest set of returned values.

Avoid searching for text in the middle or the end of a string, for example, "cn=\*hille\*" or "cn=\*larouse".

When possible, search for indexed attributes. Indexed attributes are stored on all domain controllers, so the query will most likely be faster than searching for a non-indexed attribute.

 

 



