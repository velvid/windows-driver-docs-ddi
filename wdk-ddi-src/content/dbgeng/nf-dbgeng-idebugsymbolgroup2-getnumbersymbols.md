---
UID: NF:dbgeng.IDebugSymbolGroup2.GetNumberSymbols
title: IDebugSymbolGroup2::GetNumberSymbols (dbgeng.h)
description: The GetNumberSymbols method returns the number of symbols that are contained in a symbol group. This method belongs to the IDebugSymbolGroup2 interface.
old-location: debugger\getnumbersymbols.htm
tech.root: debugger
ms.date: 05/03/2018
keywords: ["IDebugSymbolGroup2::GetNumberSymbols"]
ms.keywords: ComOther_e355317f-ba58-4d2a-a8f7-ad3cf4b17607.xml, GetNumberSymbols, GetNumberSymbols method [Windows Debugging], GetNumberSymbols method [Windows Debugging],IDebugSymbolGroup interface, GetNumberSymbols method [Windows Debugging],IDebugSymbolGroup2 interface, IDebugSymbolGroup interface [Windows Debugging],GetNumberSymbols method, IDebugSymbolGroup2 interface [Windows Debugging],GetNumberSymbols method, IDebugSymbolGroup2.GetNumberSymbols, IDebugSymbolGroup2::GetNumberSymbols, IDebugSymbolGroup::GetNumberSymbols, dbgeng/IDebugSymbolGroup2::GetNumberSymbols, dbgeng/IDebugSymbolGroup::GetNumberSymbols, debugger.getnumbersymbols
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
 - IDebugSymbolGroup2::GetNumberSymbols
 - dbgeng/IDebugSymbolGroup2::GetNumberSymbols
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dbgeng.h
api_name:
 - IDebugSymbolGroup2::GetNumberSymbols
---

# IDebugSymbolGroup2::GetNumberSymbols


## -description

The <b>GetNumberSymbols</b> method returns the number of <a href="/windows-hardware/drivers/debugger/symbols4">symbols</a> that are contained in a symbol group.

## -parameters

### -param Number 

[out]
The number of symbols that are contained in this symbol group.

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
 

This method can also return error values.  For more information, see <a href="/windows-hardware/drivers/debugger/hresult-values">Return Values</a>.

## -remarks

Each symbol in a symbol group is identified by an <i>index</i>.  This index is a number between zero and the number that is returned to <i>Number</i> minus one.  Every time that a symbol is added or removed from the symbol group, the index of all of the symbols in the group might change.

For more information about symbol groups, see <a href="/windows-hardware/drivers/debugger/scopes-and-symbol-groups">Scopes and Symbol Groups</a>.

