---
UID: NF:dbgeng.IDebugSystemObjects2.GetCurrentThreadDataOffset
title: IDebugSystemObjects2::GetCurrentThreadDataOffset (dbgeng.h)
description: The GetCurrentThreadDataOffset method returns the location of the system data structure for the current thread. This method belongs to IDebugSystemObjects2.
old-location: debugger\getcurrentthreaddataoffset.htm
tech.root: debugger
ms.date: 05/03/2018
keywords: ["IDebugSystemObjects2::GetCurrentThreadDataOffset"]
ms.keywords: GetCurrentThreadDataOffset, GetCurrentThreadDataOffset method [Windows Debugging], GetCurrentThreadDataOffset method [Windows Debugging],IDebugSystemObjects interface, GetCurrentThreadDataOffset method [Windows Debugging],IDebugSystemObjects2 interface, GetCurrentThreadDataOffset method [Windows Debugging],IDebugSystemObjects3 interface, GetCurrentThreadDataOffset method [Windows Debugging],IDebugSystemObjects4 interface, IDebugSystemObjects interface [Windows Debugging],GetCurrentThreadDataOffset method, IDebugSystemObjects2 interface [Windows Debugging],GetCurrentThreadDataOffset method, IDebugSystemObjects2.GetCurrentThreadDataOffset, IDebugSystemObjects2::GetCurrentThreadDataOffset, IDebugSystemObjects3 interface [Windows Debugging],GetCurrentThreadDataOffset method, IDebugSystemObjects3::GetCurrentThreadDataOffset, IDebugSystemObjects4 interface [Windows Debugging],GetCurrentThreadDataOffset method, IDebugSystemObjects4::GetCurrentThreadDataOffset, IDebugSystemObjects::GetCurrentThreadDataOffset, IDebugSystemObjects_5d09a9f7-d6a3-49ed-b872-1b9ee5173d28.xml, dbgeng/IDebugSystemObjects2::GetCurrentThreadDataOffset, dbgeng/IDebugSystemObjects3::GetCurrentThreadDataOffset, dbgeng/IDebugSystemObjects4::GetCurrentThreadDataOffset, dbgeng/IDebugSystemObjects::GetCurrentThreadDataOffset, debugger.getcurrentthreaddataoffset
req.header: dbgeng.h
req.include-header: Dbgeng.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
f1_keywords:
 - IDebugSystemObjects2::GetCurrentThreadDataOffset
 - dbgeng/IDebugSystemObjects2::GetCurrentThreadDataOffset
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dbgeng.h
api_name:
 - IDebugSystemObjects2::GetCurrentThreadDataOffset
---

# IDebugSystemObjects2::GetCurrentThreadDataOffset


## -description

The <b>GetCurrentThreadDataOffset</b> method returns the location of the system data structure for the current thread.

## -parameters

### -param Offset 

[out]
Receives the location of the system data structure for the current thread.

## -returns

This method may also return error values.  See <a href="/windows-hardware/drivers/debugger/hresult-values">Return Values</a> for more details.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>

## -remarks

In user-mode debugging, the location returned is of the thread environment block (TEB) for the current thread.  This is the same location returned by <a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugsystemobjects4-getcurrentthreadteb">GetCurrentThreadTeb</a>.

In kernel-mode debugging, the location returned is of the KTHREAD structure of the system thread that was executing on the processor represented by the current thread when the last event occurred.

<div class="alert"><b>Note</b>    In kernel mode debugging, the current thread is always a virtual thread the <a href="/windows-hardware/drivers/debugger/introduction">debugger engine</a> created for a processor in the target computer.  Because events may occur in different system threads, the KTHREAD location for a virtual thread may change.</div>
<div> </div>
For more information about threads, see <a href="/windows-hardware/drivers/debugger/threads-and-processes">Threads and Processes</a>.  For details on the KTHREAD and TEB structures, see <i>Microsoft Windows Internals</i> by David Solomon and Mark Russinovich.

