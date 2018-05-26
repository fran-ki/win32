---
title: PROPSETFLAG Constants
description: Define characteristics of a property set.
ms.assetid: 6f865c8f-bbca-4122-b076-14f2bc56f292
topic_type:
- apiref
api_name:
- PROPSETFLAG_DEFAULT
- PROPSETFLAG_NONSIMPLE
- PROPSETFLAG_ANSI
- PROPSETFLAG_UNBUFFERED
- PROPSETFLAG_CASE_SENSITIVE
api_location:
- Propidl.h
api_type:
- HeaderDef
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# PROPSETFLAG Constants

The PROPSETFLAG constants define characteristics of a property set. The values, listed in the following table, are used in the *grfFlags* parameter of [**IPropertySetStorage**](/windows/win32/Propidl/nn-propidl-ipropertysetstorage?branch=master) methods, the [**StgCreatePropStg**](/windows/win32/coml2api/nf-coml2api-stgcreatepropstg?branch=master) function, and the [**StgOpenPropStg**](/windows/win32/coml2api/nf-coml2api-stgopenpropstg?branch=master) function.



| Constant/value                                                                                                                                                                                                                                               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROPSETFLAG_DEFAULT"></span><span id="propsetflag_default"></span><dl> <dt>**PROPSETFLAG\_DEFAULT**</dt> <dt>0</dt> </dl>                       | If left unspecified, by default only simple property values may be written to the property set. Using simple property values prevents property sets from being transacted in the compound file and stand-alone implementations of [**IPropertySetStorage**](/windows/win32/Propidl/nn-propidl-ipropertysetstorage?branch=master). Non-e property values must be used for this purpose.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="PROPSETFLAG_NONSIMPLE"></span><span id="propsetflag_nonsimple"></span><dl> <dt>**PROPSETFLAG\_NONSIMPLE**</dt> <dt>1</dt> </dl>                 | If specified, nonsimple property values can be written to the property set and the property set is saved in a storage object. Non-simple property values include those with a VARTYPE of VT\_STORAGE, VT\_STREAM, VT\_STORED\_OBJECT, or VT\_STREAMED\_OBJECT. If this flag is not specified, non-simple types cannot be written into the property set. In the compound file and stand-alone implementations, property sets may be transacted only if **PROPSETFLAG\_NONSIMPLE** is specified.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="PROPSETFLAG_ANSI"></span><span id="propsetflag_ansi"></span><dl> <dt>**PROPSETFLAG\_ANSI**</dt> <dt>2</dt> </dl>                                | If specified, all string values in the property set that are not explicitly Unicode, that is, those other than VT\_LPWSTR, are stored with the current system ANSI code page. For more information, see [**GetACP**](https://msdn.microsoft.com/library/windows/desktop/dd318070). Use of this value is not recommended. For more information, see Remarks.<br/> If this value is absent, string values in the new property set are stored in Unicode. The degree of control that this value provides is necessary so that clients using the property-related interfaces can interoperate with standard property sets such as the OLE2 summary information, which may exist in the ANSI code page.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="PROPSETFLAG_UNBUFFERED"></span><span id="propsetflag_unbuffered"></span><dl> <dt>**PROPSETFLAG\_UNBUFFERED**</dt> <dt>4</dt> </dl>              | Used only with the [**StgCreatePropStg**](/windows/win32/coml2api/nf-coml2api-stgcreatepropstg?branch=master) and [**StgOpenPropStg**](/windows/win32/coml2api/nf-coml2api-stgopenpropstg?branch=master) functions; that is, in the stand-alone implementations of property set interfaces. If specified in these functions, changes to the property set are not buffered. Instead, changes are always written directly to the property set. Calls to a property set [**IPropertyStorage**](/windows/win32/Propidl/nn-propidl-ipropertystorage?branch=master) methods will change it. However, by default, changes are buffered in an internal property set cache and are subsequently written to the property set when the [**IPropertyStorage::Commit**](/windows/win32/Propidl/nf-propidl-ipropertystorage-commit?branch=master) method is called. <br/> Setting **PROPSETFLAG\_UNBUFFERED** decreases performance because the property set internal buffer is automatically flushed after every change to the property set. However, writing changes directly will prevent coordination problems. For example, if the storage object is opened in transacted mode, and the property set is buffered. Then, if you call the [**IStorage::Commit**](/windows/win32/Objidl/nf-objidl-istorage-commit?branch=master) method on the storage object, the property set changes will not be picked up as part of the transaction, because they are in a buffer that has not been flushed yet. You must call [**IPropertyStorage::Commit**](/windows/win32/Propidl/nf-propidl-ipropertystorage-commit?branch=master) prior to calling **IStorage::Commit** to flush the property set buffer before committing changes to the storage. As an alternative to making two calls, you can set **PROPSETFLAG\_UNBUFFERED** so that changes are always written directly to the property set and are never buffered in the property set's internal cache. Then, the changes will be picked up when the transacted storage is committed.<br/> |
| <span id="PROPSETFLAG_CASE_SENSITIVE"></span><span id="propsetflag_case_sensitive"></span><dl> <dt>**PROPSETFLAG\_CASE\_SENSITIVE**</dt> <dt>8</dt> </dl> | If specified, property names are case sensitive. Case-sensitive property names are only possible in the version 1 property set serialization format. For more information, see [Property Set Serialization](version-0-vs--version-1-property-set-serialization.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



## Remarks

These values can be set and checked using bitwise operations that determine how property sets are created and opened. Property sets are created using the [**IPropertySetStorage::Create**](/windows/win32/Propidl/nf-propidl-ipropertysetstorage-create?branch=master) method or the [**StgCreatePropStg**](/windows/win32/coml2api/nf-coml2api-stgcreatepropstg?branch=master) function. They are opened using the [**IPropertySetStorage::Open**](/windows/win32/Propidl/nf-propidl-ipropertysetstorage-open?branch=master) method or the [**StgOpenPropStg**](/windows/win32/coml2api/nf-coml2api-stgopenpropstg?branch=master) function.

It is recommended that property sets be created as Unicode by not setting the **PROPSETFLAG\_ANSI** flag in the *grfFlags* parameter. It is also recommended that you avoid using VT\_LPSTR values, and use VT\_LPWSTR values instead. When the property set code page is Unicode, VT\_LPSTR string values are converted to Unicode when stored, and converted back to multibyte string values when retrieved. When the code page of the property set is not Unicode, property names, VT\_BSTR strings, and nonsimple property values are converted to multibyte strings when stored, and converted back to Unicode when retrieved, all using the current system ANSI code page.

## Requirements



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 2000 Professional \[desktop apps only\]<br/>                           |
| Minimum supported server<br/> | Windows 2000 Server \[desktop apps only\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Propidl.h</dt> </dl> |



## See also

<dl> <dt>

[**FmtIdToPropStgName**](/windows/win32/coml2api/nf-coml2api-fmtidtopropstgname?branch=master)
</dt> <dt>

[**IPropertySetStorage::Create**](/windows/win32/Propidl/nf-propidl-ipropertysetstorage-create?branch=master)
</dt> <dt>

[**IPropertySetStorage::Open**](/windows/win32/Propidl/nf-propidl-ipropertysetstorage-open?branch=master)
</dt> <dt>

[**PropStgNameToFmtId**](/windows/win32/coml2api/nf-coml2api-propstgnametofmtid?branch=master)
</dt> <dt>

[**StgCreatePropSetStg**](/windows/win32/coml2api/nf-coml2api-stgcreatepropsetstg?branch=master)
</dt> <dt>

[**StgCreatePropStg**](/windows/win32/coml2api/nf-coml2api-stgcreatepropstg?branch=master)
</dt> <dt>

[**StgOpenPropStg**](/windows/win32/coml2api/nf-coml2api-stgopenpropstg?branch=master)
</dt> </dl>

 

 




