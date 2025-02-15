---
UID: NF:wdm.PoUnregisterSystemState
title: PoUnregisterSystemState function (wdm.h)
description: The PoUnregisterSystemState routine in wdm.h cancels a system state registration created by PoRegisterSystemState.
old-location: kernel\pounregistersystemstate.htm
tech.root: kernel
ms.date: 04/30/2018
keywords: ["PoUnregisterSystemState function"]
ms.keywords: PoUnregisterSystemState, PoUnregisterSystemState routine [Kernel-Mode Driver Architecture], kernel.pounregistersystemstate, portn_b6118bd0-5fe1-4e75-8c17-e81d1f26814c.xml, wdm/PoUnregisterSystemState
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows 2000.
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
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: <=APC_LEVEL
targetos: Windows
req.typenames: 
f1_keywords:
 - PoUnregisterSystemState
 - wdm/PoUnregisterSystemState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - PoUnregisterSystemState
---

# PoUnregisterSystemState function (wdm.h)


## -description

The <b>PoUnregisterSystemState</b> routine cancels a system state registration created by <a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-poregistersystemstate">PoRegisterSystemState</a>.

## -parameters

### -param StateHandle 

[in, out]
A pointer to a handle previously returned by <b>PoRegisterSystemState</b>.

## -remarks

This routine cancels a system busy state registration established by <b>PoRegisterSystemState</b> and frees the associated <i>StateHandle</i>.

## -see-also

<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-poregistersystemstate">PoRegisterSystemState</a>
