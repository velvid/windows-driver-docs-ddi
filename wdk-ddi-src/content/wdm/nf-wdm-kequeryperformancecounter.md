---
UID: NF:wdm.KeQueryPerformanceCounter
title: KeQueryPerformanceCounter function (wdm.h)
description: The KeQueryPerformanceCounter routine in wdm.h retrieves the current value and frequency of the performance counter.
old-location: kernel\kequeryperformancecounter.htm
tech.root: kernel
ms.date: 05/18/2021
keywords: ["KeQueryPerformanceCounter function"]
ms.keywords: KeQueryPerformanceCounter, KeQueryPerformanceCounter routine [Kernel-Mode Driver Architecture], k105_39f70923-56fe-42b1-bec3-fe23ae62904d.xml, kernel.kequeryperformancecounter, wdm/KeQueryPerformanceCounter
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
req.lib: Hal.lib
req.dll: Hal.dll
req.irql: Any level
targetos: Windows
req.typenames: 
f1_keywords:
 - KeQueryPerformanceCounter
 - wdm/KeQueryPerformanceCounter
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Hal.dll
api_name:
 - KeQueryPerformanceCounter
---

# KeQueryPerformanceCounter function (wdm.h)

## -description

The **KeQueryPerformanceCounter** routine retrieves the current value and frequency of the performance counter.

Use **KeQueryPerformanceCounter** to acquire high resolution (<1&micro;s) time stamps for time interval measurements.

## -parameters

### -param PerformanceFrequency

[out, optional]
A pointer to a variable to which **KeQueryPerformanceCounter** writes the performance counter frequency, in ticks per second. This parameter is optional and can be NULL if the caller does not need the counter frequency value.

## -returns

**KeQueryPerformanceCounter** returns the performance counter value in units of ticks.

## -remarks

**KeQueryPerformanceCounter** returns a 64-bit integer that represents the current value of a high-resolution monotonically nondecreasing counter.

To obtain the frequency of the performance counter, specify a non-**NULL** pointer value for the *PerformanceFrequency* parameter. The frequency of the performance counter is fixed at system boot and is consistent across all processors. Therefore, a driver can cache the frequency of the performance counter during initialization.  

For more info about this function and its usage, see [Acquiring high-resolution time stamps](/windows/win32/sysinfo/acquiring-high-resolution-time-stamps).

## -see-also

[KeQueryInterruptTime](./nf-wdm-kequeryinterrupttime.md)

[KeQuerySystemTime](./nf-wdm-kequerysystemtime-r1.md)

[KeQueryTickCount](../ntddk/nf-ntddk-kequerytickcount.md)

[KeQueryTimeIncrement](./nf-wdm-kequerytimeincrement.md)

[QueryPerformanceCounter](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)

[QueryPerformanceFrequency](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)
