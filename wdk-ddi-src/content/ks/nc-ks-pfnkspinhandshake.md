---
UID: NC:ks.PFNKSPINHANDSHAKE
title: PFNKSPINHANDSHAKE (ks.h)
description: An AVStream minidriver's AVStrMiniPinHandshake routine is called when AVStream receives a protocol handshake request that it does not handle.
old-location: stream\avstrminipinhandshake.htm
tech.root: stream
ms.date: 07/15/2021
keywords: ["PFNKSPINHANDSHAKE callback function"]
ms.keywords: AVStrMiniPinHandshake, AVStrMiniPinHandshake routine [Streaming Media Devices], PFNKSPINHANDSHAKE, avstclbk_3a87dcb0-5825-4ba0-b9b3-dfb6a1af20a2.xml, ks/AVStrMiniPinHandshake, stream.avstrminipinhandshake
req.header: ks.h
req.include-header: Ks.h
req.target-type: Desktop
req.target-min-winverclnt: Available in DirectX 8.0 and later versions.
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
 - PFNKSPINHANDSHAKE
 - ks/PFNKSPINHANDSHAKE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ks.h
api_name:
 - PFNKSPINHANDSHAKE
---

# PFNKSPINHANDSHAKE callback function

## -description

An AVStream minidriver's *AVStrMiniPinHandshake* routine is called when AVStream receives a protocol handshake request that it does not handle.

## -parameters

### -param Pin

### -param In

### -param Out

#### - Data [in]

Pointer to a caller-allocated buffer. If the pin supports the requested protocol, *AVStrMiniPinHandshake* should fill in this parameter with a pointer to a [**KSHANDSHAKE**](./ns-ks-kshandshake.md) structure.

#### - Irp [in]

Pointer to the IRP containing the handshake request.

#### - Request [in]

Pointer to a [**KSIDENTIFIER**](./ns-ks-ksidentifier.md) structure that contains a GUID identifying the requested protocol.

## -returns

Returns STATUS_SUCCESS if the pin supports the requested protocol. Otherwise, it should return STATUS_INVALID_DEVICE_REQUEST.

## -remarks

The minidriver specifies this routine's address in the *Handshake* parameter of a call to [**KsPinRegisterHandshakeCallback**](./nf-ks-kspinregisterhandshakecallback.md).

## -see-also

[**KSHANDSHAKE**](./ns-ks-kshandshake.md)

[**KSIDENTIFIER**](./ns-ks-ksidentifier.md)

[**KsPinRegisterHandshakeCallback**](./nf-ks-kspinregisterhandshakecallback.md)