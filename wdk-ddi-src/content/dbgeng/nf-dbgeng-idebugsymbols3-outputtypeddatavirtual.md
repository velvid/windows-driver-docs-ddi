---
UID: NF:dbgeng.IDebugSymbols3.OutputTypedDataVirtual
title: IDebugSymbols3::OutputTypedDataVirtual (dbgeng.h)
description: The IDebugSymbols3::OutputTypedDataVirtual method formats the contents of a variable in the target's virtual memory, and sends it to the output callbacks.
old-location: debugger\outputtypeddatavirtual.htm
tech.root: debugger
ms.date: 05/03/2018
keywords: ["IDebugSymbols3::OutputTypedDataVirtual"]
ms.keywords: IDebugSymbols interface [Windows Debugging],OutputTypedDataVirtual method, IDebugSymbols2 interface [Windows Debugging],OutputTypedDataVirtual method, IDebugSymbols2::OutputTypedDataVirtual, IDebugSymbols3 interface [Windows Debugging],OutputTypedDataVirtual method, IDebugSymbols3.OutputTypedDataVirtual, IDebugSymbols3::OutputTypedDataVirtual, IDebugSymbols::OutputTypedDataVirtual, IDebugSymbols_0b8c7b9b-8e0a-4166-b474-830f662be2c6.xml, OutputTypedDataVirtual, OutputTypedDataVirtual method [Windows Debugging], OutputTypedDataVirtual method [Windows Debugging],IDebugSymbols interface, OutputTypedDataVirtual method [Windows Debugging],IDebugSymbols2 interface, OutputTypedDataVirtual method [Windows Debugging],IDebugSymbols3 interface, dbgeng/IDebugSymbols2::OutputTypedDataVirtual, dbgeng/IDebugSymbols3::OutputTypedDataVirtual, dbgeng/IDebugSymbols::OutputTypedDataVirtual, debugger.outputtypeddatavirtual
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
 - IDebugSymbols3::OutputTypedDataVirtual
 - dbgeng/IDebugSymbols3::OutputTypedDataVirtual
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dbgeng.h
api_name:
 - IDebugSymbols3::OutputTypedDataVirtual
---

# IDebugSymbols3::OutputTypedDataVirtual


## -description

The <b>OutputTypedDataVirtual</b> method formats the contents of a variable in the target's virtual memory, and then sends this to the <a href="/windows-hardware/drivers/debugger/using-input-and-output">output callbacks</a>.

## -parameters

### -param OutputControl 

[in]
Specifies the output control used to determine which output callbacks can receive the output.  See <a href="/windows-hardware/drivers/debugger/debug-outctl-xxx">DEBUG_OUTCTL_XXX</a> for possible values.

### -param Offset 

[in]
Specifies the location in the target's virtual address space of the variable.

### -param Module 

[in]
Specifies the base address of the module containing the type.

### -param TypeId 

[in]
Specifies the type ID of the type.

### -param Flags 

[in]
Specifies the formatting flags.  See <a href="/windows-hardware/drivers/debugger/debug-typeopts-xxx">DEBUG_TYPEOPTS_XXX</a> for possible values.

## -returns

This method may also return error values.  See <a href="/windows-hardware/drivers/debugger/hresult-values">Return Values</a> for more details.

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

The output produced by this method is the same as for the debugger command <b>DT</b>.  See <a href="/windows-hardware/drivers/debugger/dt--display-type-">dt (Display Type)</a>.

For more information about types, see <a href="/windows-hardware/drivers/debugger/types">Types</a>.  For more information about output, see <a href="/windows-hardware/drivers/debugger/input-and-output">Input and Output</a>.

