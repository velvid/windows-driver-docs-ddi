---
UID: NF:dbgeng.IDebugEventCallbacks.CreateThread
title: IDebugEventCallbacks::CreateThread (dbgeng.h)
description: The CreateThread callback method is called by the engine when a create-threaddebugging event occurs in the target. This method belongs to IDebugEventCallbacks.
old-location: debugger\idebugeventcallbacks_createthread.htm
tech.root: debugger
ms.date: 05/03/2018
keywords: ["IDebugEventCallbacks::CreateThread"]
ms.keywords: ComCallbacks_db1fe5dc-8392-4c79-a1ed-9752170eed3c.xml, CreateThread, CreateThread method [Windows Debugging], CreateThread method [Windows Debugging],IDebugEventCallbacks interface, IDebugEventCallbacks interface [Windows Debugging],CreateThread method, IDebugEventCallbacks.CreateThread, IDebugEventCallbacks::CreateThread, dbgeng/IDebugEventCallbacks::CreateThread, debugger.idebugeventcallbacks_createthread
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
 - IDebugEventCallbacks::CreateThread
 - dbgeng/IDebugEventCallbacks::CreateThread
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dbgeng.h
api_name:
 - IDebugEventCallbacks::CreateThread
---

# IDebugEventCallbacks::CreateThread


## -description

The <b>CreateThread</b> callback method is called by the engine when a create-threaddebugging event occurs in the target.

## -parameters

### -param Handle 

[in]
Specifies the handle for the thread whose creation caused the event.  If this information is not available, <i>Handle</i> will be <b>NULL</b>.

### -param DataOffset 

[in]
Specifies a block of data that the operating system maintains for this thread. The actual data in the block is operating system-specific.  If the operating system does not have such a block, <i>DataOffset</i> will be <b>NULL</b>.

### -param StartOffset 

[in]
Specifies the starting location in the target's virtual address space of the thread.  If this information is not available, <i>StartOffset</i> will be <b>NULL</b>.

## -returns

This method returns a <a href="/windows-hardware/drivers/debugger/debug-status-xxx">DEBUG_STATUS_XXX</a> value, which indicates how the execution of the target should proceed after the engine processes this event.  For details on how the engine treats this value, see <a href="/windows-hardware/drivers/debugger/monitoring-events">Monitoring Events</a>.

## -remarks

This method is only called by the engine if the DEBUG_EVENT_CREATE_THREAD flag is set in the mask returned by <a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugeventcallbacks-getinterestmask">IDebugEventCallbacks::GetInterestMask</a>.

For more information about handling events, see <a href="/windows-hardware/drivers/debugger/monitoring-events">Monitoring Events</a>.  For information about threads, see <a href="/windows-hardware/drivers/debugger/threads-and-processes">Threads and Processes</a>.

