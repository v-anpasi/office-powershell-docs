---
external help file: sharepoint.xml
online version: 
schema: 2.0.0
---

# Get-SPDataConnectionFileDependent

## SYNOPSIS
Returns deployed forms on the server dependent on a universal data connection.

## SYNTAX

```
Get-SPDataConnectionFileDependent [-Identity] <SPDataConnectionFilePipeBind>
 [-AssignmentCollection <SPAssignmentCollection>]
```

## DESCRIPTION
The Get-SPDataConnectionFileDependent returns all administrator deployed forms that depend on a specified universal data connection (.udc) file located in the central data connection store.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### --------------EXAMPLE----------------- (SharePoint Server 2013)
```
C:\PS>Get-SPDataConnectionFileDependant -Identity "FileName.udcx

C:\PS>"FileName.udcx" | Get-SPDataConnectionFileDependant
```

This example displays a list of deployed forms with a specified name.

### --------------EXAMPLE----------------- (SharePoint Server 2016)
```
C:\PS>Get-SPDataConnectionFileDependant -Identity "FileName.udcx

C:\PS>"FileName.udcx" | Get-SPDataConnectionFileDependant
```

This example displays a list of deployed forms with a specified name.

## PARAMETERS

### -Identity
Specifies the data connection file to get.

The type must be a valid GUID, in form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a data connection file (for example, DataConnectionFileName1.udcx); or an instance of a valid SPDataConnectionFile object.

```yaml
Type: SPDataConnectionFilePipeBind
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AssignmentCollection
Manages objects for the purpose of proper disposal.
Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management.
Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory.
When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store.
If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

```yaml
Type: SPAssignmentCollection
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

