---
UID: NF:miniport.InterlockedDecrement
title: InterlockedDecrement function (miniport.h)
description: The InterlockedDecrement function (miniport.h) decrements a caller-supplied variable of type LONG as an atomic operation.
old-location: kernel\interlockeddecrement.htm
tech.root: kernel
ms.date: 04/30/2018
keywords: ["InterlockedDecrement function"]
ms.keywords: InterlockedDecrement, InterlockedDecrement routine [Kernel-Mode Driver Architecture], k102_cc85e517-f056-413e-a095-671867632613.xml, kernel.interlockeddecrement, wdm/InterlockedDecrement
req.header: miniport.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h, Miniport.h
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
req.lib: OneCoreUAP.lib on Windows 10
req.dll: 
req.irql: Any level
targetos: Windows
req.typenames: 
f1_keywords:
 - InterlockedDecrement
 - miniport/InterlockedDecrement
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OneCoreUAP.lib
 - OneCoreUAP.dll
 - API-MS-Win-Core-Interlocked-l1-1-0.dll
 - API-MS-Win-Core-Interlocked-l1-2-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
api_name:
 - InterlockedDecrement
---

# InterlockedDecrement function (miniport.h)


## -description

The <b>InterlockedDecrement</b> routine decrements a caller-supplied variable of type LONG as an atomic operation.

## -parameters

### -param Addend 

[in, out]
A pointer to a variable to be decremented.

## -returns

<b>InterlockedDecrement</b> returns the decremented value.

## -remarks

<b>InterlockedDecrement</b> should be used instead of <b>ExInterlockedDecrementLong</b> because it is both more efficient and faster. 

<b>InterlockedDecrement</b> is implemented inline by the compiler when appropriate and possible. It does not require a spin lock and can therefore be safely used on pageable data.

<b>InterlockedDecrement</b> is atomic only with respect to other <b>Interlocked<i>Xxx</i></b> calls. 

Interlocked operations cannot be used on non-cached memory.

## -see-also

<a href="/previous-versions/ff545335(v=vs.85)">ExInterlockedAddLargeInteger</a>



<a href="/previous-versions/ff545343(v=vs.85)">ExInterlockedAddUlong</a>



<a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-interlockedexchange">InterlockedExchange</a>



<a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-interlockedincrement">InterlockedIncrement</a>
