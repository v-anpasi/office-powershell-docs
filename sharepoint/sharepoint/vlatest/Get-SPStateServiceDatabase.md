---
external help file: sharepoint.xml
online version: 
schema: 2.0.0
---

# Get-SPStateServiceDatabase

## SYNOPSIS
Returns a state service database.

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Get-SPStateServiceDatabase [[-Identity] <SPStateDatabasePipeBind>]
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf]
```

### UNNAMED_PARAMETER_SET_2
```
Get-SPStateServiceDatabase [[-ServiceApplication] <SPStateServiceApplicationPipeBind>]
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf]
```

## DESCRIPTION
This cmdlet contains more than one parameter set.
You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see Cmdlet Parameter Sets (http://go.microsoft.com/fwlink/?LinkID=187810).

The Get-SPStateServiceDatabase cmdlet returns a state service database on the farm.
If the Identity parameter is not specified, this cmdlet returns the collection of all state service databases on the farm.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### --------------EXAMPLE 1---------------- (SharePoint Server 2013)
```
C:\PS>Get-SPStateServiceDatabase
```

This example displays all of the state service databases on the farm.

### --------------EXAMPLE 1---------------- (SharePoint Server 2016)
```
C:\PS>Get-SPStateServiceDatabase
```

This example displays all of the state service databases on the farm.

### --------------EXAMPLE 2-------------- (SharePoint Server 2013)
```
C:\PS>Get-SPStateServiceDatabase -Identity 9703f7e2-9521-47c3-bd92-80e3eeba391b
```

This example displays a specific state service database in the farm.

### --------------EXAMPLE 2-------------- (SharePoint Server 2016)
```
C:\PS>Get-SPStateServiceDatabase -Identity 9703f7e2-9521-47c3-bd92-80e3eeba391b
```

This example displays a specific state service database in the farm.

### --------------EXAMPLE 3-------------- (SharePoint Server 2013)
```
C:\PS>Get-SPStateServiceDatabase -ServiceApplication "StateServiceApp1"
```

This example displays all state service databases associated with a specific service.

### --------------EXAMPLE 3-------------- (SharePoint Server 2016)
```
C:\PS>Get-SPStateServiceDatabase -ServiceApplication "StateServiceApp1"
```

This example displays all state service databases associated with a specific service.

## PARAMETERS

### -Identity
Specifies the state service database to get.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh or an instance of a valid SPStateServiceDatabase object (for example, StateSvcDB1).

```yaml
Type: SPStateDatabasePipeBind
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ServiceApplication
Filters to return only the state service database associated with the specified state service application.

The type must be a valid name of a state service application (for example, StateServiceApp1); a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or an instance of a valid SPStateServiceApplication object.

```yaml
Type: SPStateServiceApplicationPipeBind
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: Application

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### -Confirm
Prompts you for confirmation before executing the command.
For more information, type the following command: get-help about_commonparameters

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Displays a message that describes the effect of the command instead of executing the command.
For more information, type the following command: get-help about_commonparameters

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

