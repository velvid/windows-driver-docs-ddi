---
UID: NF:dbgeng.IDebugControl.AddExtension
title: IDebugControl::AddExtension (dbgeng.h)
description: The AddExtension method loads an extension library into the debugger engine. This method belongs to the IDebugControl interface.
old-location: debugger\addextension.htm
tech.root: debugger
ms.date: 02/04/2021
keywords: ["IDebugControl::AddExtension"]
ms.keywords: AddExtension, AddExtension method [Windows Debugging], AddExtension method [Windows Debugging],IDebugControl interface, AddExtension method [Windows Debugging],IDebugControl2 interface, AddExtension method [Windows Debugging],IDebugControl3 interface, IDebugControl interface [Windows Debugging],AddExtension method, IDebugControl.AddExtension, IDebugControl2 interface [Windows Debugging],AddExtension method, IDebugControl2::AddExtension, IDebugControl3 interface [Windows Debugging],AddExtension method, IDebugControl3::AddExtension, IDebugControl::AddExtension, IDebugControl_9d85fcbb-1c02-4b5a-b9ab-c50b9b266d1d.xml, dbgeng/IDebugControl2::AddExtension, dbgeng/IDebugControl3::AddExtension, dbgeng/IDebugControl::AddExtension, debugger.addextension
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
 - IDebugControl::AddExtension
 - dbgeng/IDebugControl::AddExtension
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dbgeng.h
api_name:
 - IDebugControl::AddExtension
---

# IDebugControl::AddExtension


## -description

The <b>AddExtension</b>  method loads an extension library into the <a href="/windows-hardware/drivers/debugger/introduction">debugger engine</a>.

## -parameters

### -param Path 

[in]
Specifies the fully qualified path and file name of the extension library to load.

### -param Flags 

[in]
Set to zero.

### -param Handle 

[out]
Receives the handle of the loaded extension library.

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

If the extension library has already been loaded, the handle to already loaded library is returned.  The extension library is not loaded again.

The extension library is loaded into the host engine and <i>Path</i> contains a path and file name for this instance of the debugger engine.

AddExtension does not complete the process of loading and initializing the extension DLL. To make the extension available for use, make a subsequent call to the <a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugcontrol-getextensionfunction">GetExtensionFunction</a>.

For more information on using extension libraries, see <a href="/windows-hardware/drivers/debugger/calling-extensions-and-extension-functions">Calling Extensions and Extension Functions</a>.

## -see-also

<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugcontrol-getextensionfunction">GetExtensionFunction</a>

<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugcontrol-getextensionbypath">GetExtensionByPath</a>


<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugcontrol3-removeextension">RemoveExtension</a>


<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugcontrol">IDebugControl</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugcontrol2">IDebugControl2</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugcontrol3">IDebugControl3</a>


