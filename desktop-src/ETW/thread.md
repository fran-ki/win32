---
Description: This class is the parent class for thread events. The following syntax is simplified from MOF code.
ms.assetid: 861ab070-5536-4897-b523-9b09a7d59b3e
title: Thread class
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Thread class

This class is the parent class for thread events.

The following syntax is simplified from MOF code.

## Syntax

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Thread : MSNT_SystemTrace
{
};
```

## Members

The **Thread** class does not define any members.

## Remarks

To enable thread events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_THREAD** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](event-trace-properties.md) structure when calling the [**StartTrace**](starttrace.md) function.

Event trace consumers can implement special processing for thread events by calling the [**SetTraceCallback**](settracecallback.md) function and specifying [**ThreadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter. Use the following event types to identify the actual thread event when consuming events.



| Event type                                                      | Description                                                                                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT\_TRACE\_TYPE\_END**(Event type value is 2)<br/>   | End thread event. The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.                                                                                                        |
| **EVENT\_TRACE\_TYPE\_START**(Event type value is 1)<br/> | Start thread event. The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.                                                                                                      |
| Event type value, 3                                             | Start data collection thread event. Enumerates threads that are currently running at the time the kernel session starts. The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event. |
| Event type value, 4                                             | End data collection thread event. Enumerates threads that are currently running at the time the kernel session ends. The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.     |



 

Process and thread start events may be logged in the context of the parent process or thread. As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](event-trace-header.md) may not correspond to the process and thread being created. This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).

## Requirements



|                                     |                                                      |
|-------------------------------------|------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>       |
| Minimum supported server<br/> | Windows Server 2008 \[desktop apps only\]<br/> |



## See also

<dl> <dt>

[**MSNT\_SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Thread\_TypeGroup1**](thread-typegroup1.md)
</dt> <dt>

[**Thread\_V0**](thread-v0.md)
</dt> <dt>

[**Thread\_V1**](thread-v1.md)
</dt> <dt>

[**Thread\_V2**](thread-v2.md)
</dt> </dl>

 

 



