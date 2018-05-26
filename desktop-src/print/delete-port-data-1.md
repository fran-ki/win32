---
Description: The XcvData function uses a DELETE\_PORT\_DATA\_1 structure when it deletes a port.
ms.assetid: d4fb5bf9-7982-4abd-91ba-59b7798a18c7
title: DELETE\_PORT\_DATA\_1 structure
ms.date: 05/31/2018
ms.topic: structure
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# DELETE\_PORT\_DATA\_1 structure

The [**XcvData**](print.xcvdata) function uses a DELETE\_PORT\_DATA\_1 structure when it deletes a port.

## Syntax


```C++
typedef struct _DELETE_PORT_DATA_1 {
  WCHAR psztPortName[MAX_PORTNAME_LEN];
  BYTE  Reserved[98];
  DWORD dwVersion;
  DWORD dwReserved;
} DELETE_PORT_DATA_1, *PDELETE_PORT_DATA_1;
```



## Members

<dl> <dt>

**psztPortName**
</dt> <dd>

Specifies the name of the port to be deleted. The MAX\_PORTNAME\_LEN constant is defined in tcpxcv.h.

</dd> <dt>

**Reserved**
</dt> <dd>

Is reserved for system use.

</dd> <dt>

**dwVersion**
</dt> <dd>

Specifies the version of this structure, which is currently 1.

</dd> <dt>

**dwReserved**
</dt> <dd>

Is obsolete, and must be set to 0.

</dd> </dl>

## Remarks

When the [**XcvData**](print.xcvdata) function is called to delete a port, its *pInputData* parameter must be set with the address of a DELETE\_PORT\_DATA\_1 structure. Set this function's *pszDataName* parameter to the string L"DeletePort".

See [TCPMON Xcv Interface](print.tcpmon_xcv_interface) for more information.

## Requirements



|                   |                                                                                                        |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Tcpxcv.h (include Tcpxcv.h)</dt> </dl> |



## See also

<dl> <dt>

[**XcvData**](print.xcvdata)
</dt> </dl>

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bprint\print%5D:%20DELETE_PORT_DATA_1%20structure%20%20RELEASE:%20%285/12/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/en-us/default.aspx. "Send comments about this topic to Microsoft")




