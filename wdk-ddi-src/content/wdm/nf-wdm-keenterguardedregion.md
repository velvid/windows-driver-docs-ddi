---
UID: NF:wdm.KeEnterGuardedRegion
title: KeEnterGuardedRegion function (wdm.h)
description: The KeEnterGuardedRegion function (wdm.h) enters a guarded region, which disables all kernel-mode APC delivery to the current thread.
old-location: kernel\keenterguardedregion.htm
tech.root: kernel
ms.date: 04/30/2018
keywords: ["KeEnterGuardedRegion function"]
ms.keywords: KeEnterGuardedRegion, KeEnterGuardedRegion routine [Kernel-Mode Driver Architecture], k105_0f632d64-85dc-4c0f-8a26-8b4710673ab5.xml, kernel.keenterguardedregion, wdm/KeEnterGuardedRegion
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows Server 2003 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: GuardedRegions, IrqlKeApcLte2, WithinCriticalRegion, HwStorPortProhibitedDDIs
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: <= APC_LEVEL
targetos: Windows
req.typenames: 
f1_keywords:
 - KeEnterGuardedRegion
 - wdm/KeEnterGuardedRegion
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - KeEnterGuardedRegion
---

# KeEnterGuardedRegion function (wdm.h)


## -description

The <b>KeEnterGuardedRegion</b> routine enters a guarded region, which disables all kernel-mode APC delivery to the current thread.

## -parameters

## -remarks

To exit a guarded region entered with <b>KeEnterGuardedRegion</b>, call the <b>KeLeaveGuardedRegion</b> routine. Guarded regions can be nested. APCs are not reenabled until the thread exits the outermost guarded region.

For more information about guarded regions, see <a href="/windows-hardware/drivers/kernel/critical-regions-and-guarded-regions">Critical Regions and Guarded Regions</a>.

## -see-also

<a href="/windows-hardware/drivers/ddi/ntddk/nf-ntddk-keleaveguardedregion">KeLeaveGuardedRegion</a>
