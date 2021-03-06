---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/15289d89-02bb-4d34-abf8-6fb217ffe341(Office.15).aspx
schema: 2.0.0
---

# Remove-SPEnterpriseSearchTopology

## SYNOPSIS
Removes an inactive search topology from a search service application.

## SYNTAX

```
Remove-SPEnterpriseSearchTopology [-Identity] <SearchTopologyPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-SearchApplication <SearchServiceApplicationPipeBind>] [-WhatIf]
```

## DESCRIPTION
This cmdlet removes the given inactive search topology from the search service application to which it belongs.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ------------------EXAMPLE 1------------------ (SharePoint Server 2013)
```
$ssa = Get-SPEnterpriseSearchServiceApplication

$topology = Get-SPEnterpriseSearchTopology -SearchApplication $ssa -Identity 4b32-4fe6-8f8d-065388df201e

Remove-SPEnterpriseSearchTopology -Identity $topology
```

This example removes a search topology with the identity 4b32-4fe6-8f8d-065388df201e.

### ------------------EXAMPLE 1------------------ (SharePoint Server 2016)
```
C:\PS>$ssa = Get-SPEnterpriseSearchServiceApplication
$topology = Get-SPEnterpriseSearchTopology -SearchApplication $ssa -Identity 4b32-4fe6-8f8d-065388df201e
Remove-SPEnterpriseSearchTopology -Identity $topology
```

This example removes a search topology with the identity 4b32-4fe6-8f8d-065388df201e.

### ------------------EXAMPLE 2------------------ (SharePoint Server 2013)
```
$ssa = Get-SPEnterpriseSearchServiceApplication


Remove-SPEnterpriseSearchTopology -Identity $topo -SearchApplication $ssa
```

This example removes the search topology referenced by $topo in the search service application referenced by $ssa.

### ------------------EXAMPLE 2------------------ (SharePoint Server 2016)
```
C:\PS>$ssa = Get-SPEnterpriseSearchServiceApplication
Remove-SPEnterpriseSearchTopology -Identity $topo -SearchApplication $ssa
```

This example removes the search topology referenced by $topo in the search service application referenced by $ssa.

## PARAMETERS

### -Identity
Specifies the search topology to retrieve.

```yaml
Type: SearchTopologyPipeBind
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

### -SearchApplication
Specifies the search application to which the search topology belongs.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid SearchServiceApplication object.

```yaml
Type: SearchServiceApplicationPipeBind
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
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

[Online Version](http://technet.microsoft.com/EN-US/library/15289d89-02bb-4d34-abf8-6fb217ffe341(Office.15).aspx)

[Get-SPEnterpriseSearchTopology]()

[New-SPEnterpriseSearchTopology]()

[Set-SPEnterpriseSearchTopology]()

