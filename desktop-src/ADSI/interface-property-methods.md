---
title: Interface Property Methods
description: Many ADSI interfaces are designed to support Automation and thus are dual interfaces in that they support client access through both IUnknown and IDispatch interfaces.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\mbaldwin
ms.assetid: b2831fa4-b58d-4b65-8deb-5fb7cd50c724
ms.prod: windows-server-dev
ms.technology: active-directory-domain-services
ms.tgt_platform: multiple
keywords:
- Interface Property Methods
- ADSI ADSI , reference, property methods explained
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# Interface Property Methods

Many ADSI interfaces are designed to support Automation and thus are dual interfaces in that they support client access through both [**IUnknown**](_com_iunknown) and [**IDispatch**](ebbff4bc-36b2-4861-9efa-ffa45e013eb5) interfaces. Non-Automation clients, such as those written in C/C++, resolve method invocation directly, using the [**IUnknown::QueryInterface**](_com_iunknown_queryinterface) method, and call the method directly. Automation clients, also known as name-bound clients, such as those written in Visual Basic, or Visual Basic Scripting Edition (VBScript), must resolve method invocation indirectly using the [**dispinterface**](https://msdn.microsoft.com/library/windows/desktop/ms221599) method.

An ADSI interface supporting Automation defines property methods for retrieving and modifying properties of an object implementing the interface. The property methods have names that have **get**\_ and **put**\_ prepended to the appropriate property names, for example, **get\_User** and **put\_Name**.

Each **get\_** method takes a single parameter as output. This parameter is a method-allocated address of a variable of the property data type. On return, this variable assumes the current value of the requested property. The caller must release the allocated memory of the variable when the property is no longer required.

Each **put\_** method takes a single parameter as input for the data type of the corresponding property. The parameter holds a new value of the property.

The following code example shows the invocation of the property methods that follow the usual procedure to call the member function of an object.


```C++
IADs *pADs;
BSTR bstrName;
pADs->get_Name(&amp;bstrName);
```



The following code example shows the invocation of the property methods in automation clients, which can be somewhat different. For example, Visual Basic uses dot notation.


```VB
Dim Obj As IADs
Dim objName As String
objName = Obj.Name
```



All parameters and return types must be of those that the VARIANT data type defines. All methods on a dual interface return an HRESULT value to indicate success or failure.

For more information about getting and setting properties on ADSI objects, see [Property Cache](property-cache-interfaces.md).

 

 



