---
external help file: sharepoint.xml
online version: 
schema: 2.0.0
---

# Get-SPServiceInstance

## SYNOPSIS
Below Content Applies To: SharePoint Server 2013

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Get-SPServiceInstance [[-Identity] <SPServiceInstancePipeBind>]
 [-AssignmentCollection <SPAssignmentCollection>] [-All]
```

### UNNAMED_PARAMETER_SET_2
```
Get-SPServiceInstance -Server <SPServerPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-All]
```

## DESCRIPTION
This cmdlet contains more than one parameter set.
You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see Cmdlet Parameter Sets (http://go.microsoft.com/fwlink/?LinkID=187810).

The Get-SPServiceInstance cmdlet returns the services instance specified by the Identity parameter for a specific server.
If the Server parameter is not specified, the Get-SPServiceInstance cmdlet returns results for the entire farm.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### --------------EXAMPLE----------------- (SharePoint Server 2013)
```
C:\PS>Get-SPServiceInstance -Server ServerA
```

This example displays the service instances from a given server.

### --------------EXAMPLE----------------- (SharePoint Server 2016)
```
C:\PS>Get-SPServiceInstance -Server ServerA
```

This example displays the service instances from a given server.

## PARAMETERS

### -Identity
Specifies the GUID of the service instance.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh.

```yaml
Type: SPServiceInstancePipeBind
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Server
Specifies the server from which to return the service instance.

```yaml
Type: SPServerPipeBind
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 

Required: True
Position: Named
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

### -All
{{Fill All Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

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

