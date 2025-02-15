---
UID: NF:dbgeng.IDebugSymbols.GetFieldOffset
title: IDebugSymbols::GetFieldOffset (dbgeng.h)
description: The GetFieldOffset method returns the offset of a field from the base address of an instance of a type. This method belongs to the IDebugSymbols interface.
old-location: debugger\getfieldoffset2.htm
tech.root: debugger
ms.date: 05/03/2018
keywords: ["IDebugSymbols::GetFieldOffset"]
ms.keywords: GetFieldOffset, GetFieldOffset method [Windows Debugging], GetFieldOffset method [Windows Debugging],IDebugSymbols interface, GetFieldOffset method [Windows Debugging],IDebugSymbols2 interface, GetFieldOffset method [Windows Debugging],IDebugSymbols3 interface, IDebugSymbols interface [Windows Debugging],GetFieldOffset method, IDebugSymbols.GetFieldOffset, IDebugSymbols2 interface [Windows Debugging],GetFieldOffset method, IDebugSymbols2::GetFieldOffset, IDebugSymbols3 interface [Windows Debugging],GetFieldOffset method, IDebugSymbols3::GetFieldOffset, IDebugSymbols::GetFieldOffset, IDebugSymbols_3e5be57a-3af9-4fe3-a7cc-4f31fb9b54f0.xml, dbgeng/IDebugSymbols2::GetFieldOffset, dbgeng/IDebugSymbols3::GetFieldOffset, dbgeng/IDebugSymbols::GetFieldOffset, debugger.getfieldoffset2
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
 - IDebugSymbols::GetFieldOffset
 - dbgeng/IDebugSymbols::GetFieldOffset
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dbgeng.h
api_name:
 - IDebugSymbols::GetFieldOffset
---

# IDebugSymbols::GetFieldOffset


## -description

The <b>GetFieldOffset</b>  method returns the offset of a field from the base address of an instance of a type.

## -parameters

### -param Module 

[in]
Specifies the module containing the types of both the container and the field.

### -param TypeId 

[in]
Specifies the type ID of the type containing the field.

### -param Field 

[in]
Specifies the name of the field whose offset is requested.  Subfields may be specified by using a dot-separated path.

### -param Offset 

[out]
Receives the offset of the specified field from the base memory location of an instance of the type.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The field <i>Field</i> could not be found in the type specified by <i>TypeId</i>.

</td>
</tr>
</table>

## -remarks

An example of a dot-separated path for the <i>Field</i> parameter is as follows.  Suppose the MyStruct structure contains a field <b>MyField</b> of type MySubStruct, and the MySubStruct structure contains the field <b>MySubField</b>.  Then the location of this field relative to the location of MyStruct structure can be found by setting the <i>Field</i> parameter to "MyField.MySubField".

For more information about types, see <a href="/windows-hardware/drivers/debugger/types">Types</a>.

