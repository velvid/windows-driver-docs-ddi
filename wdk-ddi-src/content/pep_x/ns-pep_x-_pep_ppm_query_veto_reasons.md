---
UID: NS:pep_x._PEP_PPM_QUERY_VETO_REASONS
title: _PEP_PPM_QUERY_VETO_REASONS (pep_x.h)
description: Learn how the PEP_PPM_QUERY_VETO_REASONS structure specifies the total number of veto reasons that the PEP uses in calls to the ProcessorIdleVeto and PlatformIdleVeto routines.
old-location: kernel\pep_ppm_query_veto_reasons.htm
tech.root: kernel
ms.date: 04/30/2018
keywords: ["PEP_PPM_QUERY_VETO_REASONS structure"]
ms.keywords: "*PPEP_PPM_QUERY_VETO_REASONS, PEP_PPM_QUERY_VETO_REASONS, PEP_PPM_QUERY_VETO_REASONS structure [Kernel-Mode Driver Architecture], PPEP_PPM_QUERY_VETO_REASONS, PPEP_PPM_QUERY_VETO_REASONS structure pointer [Kernel-Mode Driver Architecture], _PEP_PPM_QUERY_VETO_REASONS, kernel.pep_ppm_query_veto_reasons, pepfx/PEP_PPM_QUERY_VETO_REASONS, pepfx/PPEP_PPM_QUERY_VETO_REASONS"
req.header: pep_x.h
req.include-header: Pep_x.h
req.target-type: Windows
req.target-min-winverclnt: Supported starting with Windows 10.
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
req.typenames: PEP_PPM_QUERY_VETO_REASONS, *PPEP_PPM_QUERY_VETO_REASONS
f1_keywords:
 - _PEP_PPM_QUERY_VETO_REASONS
 - pep_x/_PEP_PPM_QUERY_VETO_REASONS
 - PPEP_PPM_QUERY_VETO_REASONS
 - pep_x/PPEP_PPM_QUERY_VETO_REASONS
 - PEP_PPM_QUERY_VETO_REASONS
 - pep_x/PEP_PPM_QUERY_VETO_REASONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - pepfx.h
api_name:
 - _PEP_PPM_QUERY_VETO_REASONS
 - PPEP_PPM_QUERY_VETO_REASONS
 - PEP_PPM_QUERY_VETO_REASONS
---

# _PEP_PPM_QUERY_VETO_REASONS structure (pep_x.h)


## -description

The <b>PEP_PPM_QUERY_VETO_REASONS</b> structure specifies the total number of veto reasons that the PEP uses in calls to the <a href="/windows-hardware/drivers/ddi/pepfx/nc-pepfx-pofxcallbackprocessoridleveto">ProcessorIdleVeto</a> and <a href="/windows-hardware/drivers/ddi/pepfx/nc-pepfx-pofxcallbackplatformidleveto">PlatformIdleVeto</a> routines.

## -struct-fields

### -field VetoReasonCount

[out] The number of veto codes used by the PEP.

## -remarks

This structure is used by the <a href="/windows-hardware/drivers/ddi/pepfx/ns-pepfx-_pep_ppm_query_veto_reason">PEP_NOTIFY_PPM_QUERY_VETO_REASONS</a> notification. The <b>VetoReasonCount</b> member contains an output value that the PEP writes to this member in response to the notification.

## -see-also

<a href="/windows-hardware/drivers/ddi/pepfx/ns-pepfx-_pep_ppm_query_veto_reason">PEP_NOTIFY_PPM_QUERY_VETO_REASONS</a>

