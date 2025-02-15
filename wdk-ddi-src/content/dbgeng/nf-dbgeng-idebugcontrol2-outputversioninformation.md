---
UID: NF:dbgeng.IDebugControl2.OutputVersionInformation
title: IDebugControl2::OutputVersionInformation (dbgeng.h)
description: Learn about the OutputVersionInformation method, which prints version information about the debugger engine to the debugger console.
old-location: debugger\outputversioninformation.htm
tech.root: debugger
ms.date: 05/03/2018
keywords: ["IDebugControl2::OutputVersionInformation"]
ms.keywords: IDebugControl interface [Windows Debugging],OutputVersionInformation method, IDebugControl2 interface [Windows Debugging],OutputVersionInformation method, IDebugControl2.OutputVersionInformation, IDebugControl2::OutputVersionInformation, IDebugControl3 interface [Windows Debugging],OutputVersionInformation method, IDebugControl3::OutputVersionInformation, IDebugControl::OutputVersionInformation, IDebugControl_ea568b24-944d-4ed8-abd6-24b7c7771a1e.xml, OutputVersionInformation, OutputVersionInformation method [Windows Debugging], OutputVersionInformation method [Windows Debugging],IDebugControl interface, OutputVersionInformation method [Windows Debugging],IDebugControl2 interface, OutputVersionInformation method [Windows Debugging],IDebugControl3 interface, dbgeng/IDebugControl2::OutputVersionInformation, dbgeng/IDebugControl3::OutputVersionInformation, dbgeng/IDebugControl::OutputVersionInformation, debugger.outputversioninformation
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
 - IDebugControl2::OutputVersionInformation
 - dbgeng/IDebugControl2::OutputVersionInformation
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dbgeng.h
api_name:
 - IDebugControl2::OutputVersionInformation
---

# IDebugControl2::OutputVersionInformation


## -description

The <b>OutputVersionInformation</b> method prints version information about the <a href="/windows-hardware/drivers/debugger/introduction">debugger engine</a> to the debugger console.

## -parameters

### -param OutputControl 

[in]
Specifies where to send the output.  For possible values, see <a href="/windows-hardware/drivers/debugger/debug-outctl-xxx">DEBUG_OUTCTL_XXX</a>.

## -returns

This method may also return other error values, including error values caused by the engine being busy.  See <a href="/windows-hardware/drivers/debugger/hresult-values">Return Values</a> for more details.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>

## -remarks

The information that is sent to the output can include the mode of the debugger, the path and version of the debugger DLLs, the extension DLL search path, the extension DLL chain, and the version of the operating system that is running on the host computer.

For more information, see <a href="/windows-hardware/drivers/debugger/target-information">Target Information</a>.

