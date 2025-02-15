---
UID: NC:iddcx.PFN_IDDCXSWAPCHAININSYSTEMMEMORY
title: PFN_IDDCXSWAPCHAININSYSTEMMEMORY
ms.date: 10/20/2020
tech.root: display
targetos: Windows
description: PFN_IDDCXSWAPCHAININSYSTEMMEMORY is a pointer to an OS callback function through which to determine whether swapchain buffers are allocated in system memory.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: iddcx.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt:
req.target-min-winversvr: Windows Server 2022
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - iddcx.h
api_name:
 - PFN_IDDCXSWAPCHAININSYSTEMMEMORY
f1_keywords:
 - PFN_IDDCXSWAPCHAININSYSTEMMEMORY
 - iddcx/PFN_IDDCXSWAPCHAININSYSTEMMEMORY
dev_langs:
 - c++
---

## -description

**PFN_IDDCXSWAPCHAININSYSTEMMEMORY** is a pointer to an OS callback function through which to determine whether swapchain buffers are allocated in system memory.

## -parameters

### -param DriverGlobals

[in] Pointer to an [**IDD_DRIVER_GLOBALS**](./ns-iddcx-idd_driver_globals.md) structure containing system-defined per-driver data.

### -param SwapChainObject

[in] The [IDDCX_SWAPCHAIN](/windows-hardware/drivers/display/iddcx-objects) object passed to the [**EVT_IDD_CX_MONITOR_ASSIGN_SWAPCHAIN**](nc-iddcx-evt_idd_cx_monitor_assign_swapchain.md) call.

### -param pInSystemMemory

[out] Output arguments of the functions.

## -returns

**PFN_IDDCXSWAPCHAININSYSTEMMEMORY** returns S_OK; otherwise it returns an appropriate error code.

## -remarks

An indirect display driver (IDD) should not use this pointer to directly call the function that it points to. IDDs should instead call [**IddCxSwapChainInSystemMemory**](nc-iddcx-pfn_iddcxswapchaininsystemmemory.md).

## -see-also

[**IddCxSwapChainInSystemMemory**](nc-iddcx-pfn_iddcxswapchaininsystemmemory.md)