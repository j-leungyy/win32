---
Description: Determines whether components marked in the options are installed on the system.
ms.assetid: 5fda917a-9c4b-42a3-8f79-9c609f56eb9f
title: IcfgNeedInetComponents function
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# IcfgNeedInetComponents function

Determines whether components marked in the options are installed on the system.

## Syntax


```C++
HRESULT IcfgNeedInetComponents(
   DWORD  dwfOptions,
   LPBOOL lpfNeedComponents
);
```



## Parameters

<dl> <dt>

*dwfOptions* 
</dt> <dd>

A combination of the following flags that specify which components to detect from the following list.



| Value                                                                                                                                                                                                                                  | Meaning                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <dt>**ICFG\_INSTALLMAIL**</dt> <dt>0x00000004</dt> </dl> | Is Exchange or Internet mail needed?<br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <dt>**ICFG\_INSTALLRAS**</dt> <dt>0x00000002</dt> </dl>    | Is RAS needed?<br/>                       |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <dt>**ICFG\_INSTALLTCP**</dt> <dt>0x00000001</dt> </dl>    | Is TCP/IP needed?<br/>                    |



 

</dd> <dt>

*lpfNeedComponents* 
</dt> <dd>

If this value is non-**NULL**, it is **TRUE** on return if one or more components are not installed on the system.

</dd> </dl>

## Return value

Returns an **HRESULT** value. If no errors occur, it returns the **ERROR\_SUCCESS** code.

## Remarks

This function has no associated import library or header file; you must call it using the [**LoadLibrary**](https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65) and [**GetProcAddress**](https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597) functions.

## Requirements



|                |                                                                                        |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Icfgnt5.dll</dt> </dl> |



 

 



