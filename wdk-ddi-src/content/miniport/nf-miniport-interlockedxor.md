---
UID: NF:miniport.InterlockedXor
title: InterlockedXor function (miniport.h)
description: The InterlockedXor function (miniport.h) atomically computes a bitwise exclusive OR operation with the specified variable and specified value.
old-location: kernel\interlockedxor.htm
tech.root: kernel
ms.date: 04/30/2018
keywords: ["InterlockedXor function"]
ms.keywords: InterlockedXor, InterlockedXor routine [Kernel-Mode Driver Architecture], k102_7b4b6df0-2179-4a6a-941d-5aaa95609cd8.xml, kernel.interlockedxor, wdm/InterlockedXor
req.header: miniport.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h, Miniport.h
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
req.irql: Any level
targetos: Windows
req.typenames: 
f1_keywords:
 - InterlockedXor
 - miniport/InterlockedXor
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wdm.h
api_name:
 - InterlockedXor
---

# InterlockedXor function (miniport.h)


## -description

The <b>InterlockedOr</b> routine atomically computes a bitwise exclusive OR operation.

## -parameters

### -param Destination 

[in, out]
A pointer to the variable to be exclusive ORed with <i>Value</i>. The result of the operation is stored in the variable.

### -param Value 

[in]
Specifies the value to be exclusive ORed with the variable that is pointed to by <i>Destination</i>.

## -returns

<b>InterlockedXor</b> returns the original value stored in the variable pointed to by <i>Destination</i>.

## -remarks

<b>InterlockedXor</b> atomically computes <b>*</b><i>Destination</i><b>^=</b><i>Value</i>. 

Interlocked operations cannot be used on non-cached memory.

## -see-also

<a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-interlockedand">InterlockedAnd</a>



<a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-interlockedor">InterlockedOr</a>
