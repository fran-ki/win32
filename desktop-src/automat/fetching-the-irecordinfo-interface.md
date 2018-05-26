---
title: Fetching the IRecordInfo Interface
description: For passing a safearray of UDTs the type library is necessary for fetching the IRecordInfo Interface.
ms.assetid: 9d25139a-a1b2-4681-afe6-9d5b5bd04caf
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Fetching the IRecordInfo Interface

For passing a safearray of UDTs the type library is necessary for fetching the [**IRecordInfo**](/windows/previous-versions/oaidl/nn-oaidl-irecordinfo?branch=master) Interface. For v-table binding you can retrieve the **IRecordinfo** interface from the type library. For late binding the **IRecordInfo** interface can be retrieved from the default type information.

The following is an example of loading the type library and retrieving the [**IRecordInfo**](/windows/previous-versions/oaidl/nn-oaidl-irecordinfo?branch=master) interface:


```C++
ITypeLib * pTypeLib;
hr = LoadTypeLib(OLESTR("udt.tlb"), &amp;pTypeLib);
if (FAILED(hr))
    goto ErrorOut;

ITypeInfo * pTypeInfo;
hr = pTypeLib->GetTypeInfoOfGuid(<guid of udt>, &amp;pTypeInfo)
if (FAILED(hr))
   goto ErrorOut;

hr = pTypeLib->GetTypeInfo(0, &amp;pTypeInfo);
if (FAILED(hr))
   goto ErrorOut;

pTypeLib->Release();
IRecordInfo * pRecInfo;
hr = GetRecordInfoFromTypeInfo(pTypeInfo, &amp;pRecInfo);
pTypeInfo->Release();
if (FAILED(hr)) {
   printf("GetRecordInfoFromTypeInfo failed [0x%x]\n", hr);
   goto ErrorOut;
}
// Use record info

ErrorOut:;
// Put error handling code here
```



The type library containing the definition of the UDT is first loaded by calling [**LoadTypeLib**](/windows/previous-versions/OleAuto/nf-oleauto-loadtypelib?branch=master) and the type information of the UDT is obtained with [**GetTypeInfoOfGuid**](/windows/previous-versions/oaidl/nf-oaidl-itypelib-gettypeinfoofguid?branch=master). The [**GetRecordInfoFromTypeInfo**](/windows/previous-versions/OleAuto/nf-oleauto-getrecordinfofromtypeinfo?branch=master) is then called to obtain the record information from the type information of the UDT. At this point the record information is returned to *pRecInfo*.

The following example demonstrates fetching the [**IRecordInfo**](/windows/previous-versions/oaidl/nn-oaidl-irecordinfo?branch=master) interface from the default type information for late-binding. Error checking and variable declarations have been omitted for brevity.


```C++
hr = pdisp->GetTypeInfo(0, GetUserDefaultLCID(), &amp;pTypeInfo);
_ASSERT(SUCCEEDED(hr) &amp;&amp; pTypeInfo);
hr = pTypeInfo->GetContainingTypeLib(&amp;pTypelib, &amp;index);
_ASSERT(SUCCEEDED(hr) &amp;&amp; pTypelib);
hr = pTypelib->GetTypeInfoOfGuid(UUID_StudentStruct, &amp;pTypeInfo2);
_ASSERT(SUCCEEDED(hr) &amp;&amp; pTypeInfo2);
hr = GetRecordInfoFromTypeInfo(pTypeInfo2, &amp;pRecInfo);
```



 

 



