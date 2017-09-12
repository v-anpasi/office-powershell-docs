---
external help file: sharepoint.xml
online version: 
schema: 2.0.0
---

# Set-SPTopologyServiceApplicationProxy

## SYNOPSIS
Below Content Applies To: SharePoint Server 2013

## SYNTAX

```
Set-SPTopologyServiceApplicationProxy [-Identity] <SPTopologyWebServiceProxyPipeBind> -BadListPeriod <String>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf]
```

## DESCRIPTION
The Set-SPTopologyServiceApplicationProxy cmdlet sets the properties of the local topology service application proxy and the default load balancer.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ------------------EXAMPLE----------------------- (SharePoint Server 2013)
```
C:\PS>Set-SPTopologyServiceApplicationProxy 67877d63-bff4-4521-867a-ef4979ba07ce -BadListPeriod 1234
```

This example sets the bad list period for the given topology service application proxy.

The topology service application GUID is unique to every farm.
You can run the Get-SPTopologyServiceApplication cmdlet to retrieve the GUID.

### ------------------EXAMPLE----------------------- (SharePoint Server 2016)
```
C:\PS>Set-SPTopologyServiceApplicationProxy 67877d63-bff4-4521-867a-ef4979ba07ce -BadListPeriod 1234
```

This example sets the bad list period for the given topology service application proxy.

The topology service application GUID is unique to every farm.
You can run the Get-SPTopologyServiceApplication cmdlet to retrieve the GUID.

## PARAMETERS

### -Identity
Specifies the GUID of the application proxy.

The type must be a valid GUID, in the form 1234-4567-098jhj.

```yaml
Type: SPTopologyWebServiceProxyPipeBind
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BadListPeriod
Specifies the time period that a node is kept in a bad list.

The type must be a valid value between 1 and 480 (in minutes).

The default value is 10.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

