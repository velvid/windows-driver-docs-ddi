---
UID: NF:dbgeng.IDebugSymbols2.AppendImagePath
title: IDebugSymbols2::AppendImagePath (dbgeng.h)
description: The AppendImagePath method appends directories to the executable image path. This method belongs to the IDebugSymbols2 interface.
old-location: debugger\appendimagepath.htm
tech.root: debugger
ms.date: 05/03/2018
keywords: ["IDebugSymbols2::AppendImagePath"]
ms.keywords: AppendImagePath, AppendImagePath method [Windows Debugging], AppendImagePath method [Windows Debugging],IDebugSymbols interface, AppendImagePath method [Windows Debugging],IDebugSymbols2 interface, AppendImagePath method [Windows Debugging],IDebugSymbols3 interface, IDebugSymbols interface [Windows Debugging],AppendImagePath method, IDebugSymbols2 interface [Windows Debugging],AppendImagePath method, IDebugSymbols2.AppendImagePath, IDebugSymbols2::AppendImagePath, IDebugSymbols3 interface [Windows Debugging],AppendImagePath method, IDebugSymbols3::AppendImagePath, IDebugSymbols::AppendImagePath, IDebugSymbols_ea3dc04a-42d9-4457-830d-5544f50c5a97.xml, dbgeng/IDebugSymbols2::AppendImagePath, dbgeng/IDebugSymbols3::AppendImagePath, dbgeng/IDebugSymbols::AppendImagePath, debugger.appendimagepath
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
 - IDebugSymbols2::AppendImagePath
 - dbgeng/IDebugSymbols2::AppendImagePath
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dbgeng.h
api_name:
 - IDebugSymbols2::AppendImagePath
---

# IDebugSymbols2::AppendImagePath


## -description

The <b>AppendImagePath</b>  method appends directories to the executable image path.

## -parameters

### -param Addition 

[in]
Specifies the directories to append to the executable image path.  This is a string that contains directory names separated by semicolons (;).

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
 

This method may also return error values.  See <a href="/windows-hardware/drivers/debugger/hresult-values">Return Values</a> for more details.

## -remarks

The executable image path is used by the <a href="/windows-hardware/drivers/debugger/e">engine</a> when searching for executable images.

The executable image path can consist of several directories separated by semicolons (;).  These directories are searched in order.

## -see-also

<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugsymbols3-getimagepath">GetImagePath</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugsymbols">IDebugSymbols</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugsymbols2">IDebugSymbols2</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugsymbols3">IDebugSymbols3</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugsymbols3-setimagepath">SetImagePath</a>

