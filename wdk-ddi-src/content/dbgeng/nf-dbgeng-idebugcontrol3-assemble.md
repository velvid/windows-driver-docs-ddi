---
UID: NF:dbgeng.IDebugControl3.Assemble
title: IDebugControl3::Assemble (dbgeng.h)
description: The Assemble method assembles a single processor instruction. The assembled instruction is placed in the target's memory. This method belongs to IDebugControl3.
old-location: debugger\assemble.htm
tech.root: debugger
ms.date: 05/03/2018
keywords: ["IDebugControl3::Assemble"]
ms.keywords: Assemble, Assemble method [Windows Debugging], Assemble method [Windows Debugging],IDebugControl interface, Assemble method [Windows Debugging],IDebugControl2 interface, Assemble method [Windows Debugging],IDebugControl3 interface, IDebugControl interface [Windows Debugging],Assemble method, IDebugControl2 interface [Windows Debugging],Assemble method, IDebugControl2::Assemble, IDebugControl3 interface [Windows Debugging],Assemble method, IDebugControl3.Assemble, IDebugControl3::Assemble, IDebugControl::Assemble, IDebugControl_99336950-ba0b-46e1-871d-582f08ab5519.xml, dbgeng/IDebugControl2::Assemble, dbgeng/IDebugControl3::Assemble, dbgeng/IDebugControl::Assemble, debugger.assemble
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
 - IDebugControl3::Assemble
 - dbgeng/IDebugControl3::Assemble
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dbgeng.h
api_name:
 - IDebugControl3::Assemble
---

# IDebugControl3::Assemble


## -description

The <b>Assemble</b> method assembles a single processor instruction.  The assembled instruction is placed in the target's memory.

## -parameters

### -param Offset 

[in]
Specifies the location in the target's memory to place the assembled instruction.

### -param Instr 

[in]
Specifies the instruction to assemble.  The instruction is assembled according to the target's effective processor type (returned by <a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugcontrol3-seteffectiveprocessortype">SetEffectiveProcessorType</a>).

### -param EndOffset 

[out]
Receives the location in the target's memory immediately following the assembled instruction.  <i>EndOffset</i> can be used when assembling multiple instructions.

## -returns

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
 

This method can also return error values.  See <a href="/windows-hardware/drivers/debugger/hresult-values">Return Values</a> for more details.

## -remarks

The assembly language depends on the effective processor type of the target machine.  For information about the assembly language, see the processor documentation.

<div class="alert"><b>Note</b>  
      The <b>Assemble</b> and <a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugcontrol4-assemblewide">AssembleWide</a> methods are not supported on some architectures, and on some other architectures not all instructions are supported.</div>
<div> </div>
The assembly language options--returned by <a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugcontrol3-getassemblyoptions">GetAssemblyOptions</a>--affect the operation of this method.

For an overview of using assembly in debugger applications, see <a href="/windows-hardware/drivers/debugger/debugging-in-assembly-mode">Debugging in Assembly Mode</a>.  For more information about using assembly with the <a href="/windows-hardware/drivers/debugger/d">debugger engine API</a>, see <a href="/windows-hardware/drivers/debugger/assembling-and-disassembling-instructions">Assembling and Disassembling Instructions</a>.

## -see-also

<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugcontrol3-disassemble">Disassemble</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugcontrol3-getassemblyoptions">GetAssemblyOptions</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugcontrol">IDebugControl</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugcontrol2">IDebugControl2</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugcontrol3">IDebugControl3</a>

