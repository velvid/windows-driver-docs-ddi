---
UID: NF:miniport.READ_PORT_BUFFER_UCHAR
title: READ_PORT_BUFFER_UCHAR function (miniport.h)
description: The READ_PORT_BUFFER_UCHAR function (miniport.h) reads a number of bytes from the specified port address into a buffer.
old-location: kernel\read_port_buffer_uchar.htm
tech.root: kernel
ms.date: 04/30/2018
keywords: ["READ_PORT_BUFFER_UCHAR function"]
ms.keywords: READ_PORT_BUFFER_UCHAR, READ_PORT_BUFFER_UCHAR routine [Kernel-Mode Driver Architecture], k103_020afa73-5210-42d8-a2a5-dc9ac663af2c.xml, kernel.read_port_buffer_uchar, wdm/READ_PORT_BUFFER_UCHAR
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
req.lib: Hal.lib
req.dll: 
req.irql: Any level (see Remarks section)
targetos: Windows
req.typenames: 
f1_keywords:
 - READ_PORT_BUFFER_UCHAR
 - miniport/READ_PORT_BUFFER_UCHAR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Hal.lib
 - Hal.dll
api_name:
 - READ_PORT_BUFFER_UCHAR
---

# READ_PORT_BUFFER_UCHAR function (miniport.h)


## -description

The <b>READ_PORT_BUFFER_UCHAR</b> routine reads a number of bytes from the specified port address into a buffer.

## -parameters

### -param Port 

[in]
Specifies the port address, which must be a mapped memory range in I/O space.

### -param Buffer 

[out]
Pointer to a buffer into which an array of UCHAR values is read.

### -param Count 

[in]
Specifies the number of bytes to be read into the buffer.

## -remarks

The size of the buffer must be large enough to contain at least the specified number of bytes.

Callers of <b>READ_PORT_BUFFER_UCHAR</b> can be running at any IRQL, assuming the <i>Buffer</i> is resident and the <i>Port</i> is resident, mapped device memory.

