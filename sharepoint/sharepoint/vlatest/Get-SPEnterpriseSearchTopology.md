---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/43e2c839-54b8-4f78-b883-abc1dbea617c(Office.15).aspx
schema: 2.0.0
---

# Get-SPEnterpriseSearchTopology

## SYNOPSIS
Retrieves one or all search topologies that belong to a given search service application.

## SYNTAX

```
Get-SPEnterpriseSearchTopology [[-Identity] <SearchTopologyPipeBind>]
 -SearchApplication <SearchServiceApplicationPipeBind> [-Active]
 [-AssignmentCollection <SPAssignmentCollection>]
```

## DESCRIPTION
This cmdlet retrieves a given search topology, the active search topology, or all search topologies that belong to a given search service application.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ------------------EXAMPLE 1------------------ (SharePoint Server 2013)
```
$ssa = Get-SPEnterpriseSearchServiceApplication

Get-SPEnterpriseSearchTopology -SearchApplication $ssa
```

This example retrieves all search topologies of the search service application referenced by $ssa.

### ------------------EXAMPLE 1------------------ (SharePoint Server 2016)
```
C:\PS>$ssa = Get-SPEnterpriseSearchServiceApplication
Get-SPEnterpriseSearchTopology -SearchApplication $ssa
```

This example retrieves all search topologies of the search service application referenced by $ssa.

### ------------------EXAMPLE 2------------------ (SharePoint Server 2013)
```
$ssa = Get-SPEnterpriseSearchServiceApplication

Get-SPEnterpriseSearchTopology -SearchApplication $ssa -Active
```

This example retrieves the active search topology of the search service application referenced by $ssa.

### ------------------EXAMPLE 2------------------ (SharePoint Server 2016)
```
C:\PS>$ssa = Get-SPEnterpriseSearchServiceApplication
Get-SPEnterpriseSearchTopology -SearchApplication $ssa -Active
```

This example retrieves the active search topology of the search service application referenced by $ssa.

### ------------------EXAMPLE 3------------------ (SharePoint Server 2013)
```
$ssa = Get-SPEnterpriseSearchServiceApplication


Get-SPEnterpriseSearchTopology -SearchApplication $ssa -Identity 10fa59cb-4b32-4fe6-8f8d-065388df201e
```

This example retrieves search topology with the identity 10fa59cb-4b32-4fe6-8f8d-065388df201e of the search service application referenced by $ssa.

### ------------------EXAMPLE 3------------------ (SharePoint Server 2016)
```
C:\PS>$ssa = Get-SPEnterpriseSearchServiceApplication
Get-SPEnterpriseSearchTopology -SearchApplication $ssa -Identity 10fa59cb-4b32-4fe6-8f8d-065388df201e
```

This example retrieves search topology with the identity 10fa59cb-4b32-4fe6-8f8d-065388df201e of the search service application referenced by $ssa.

## PARAMETERS

### -Identity
Specifies the search topology to retrieve.

```yaml
Type: SearchTopologyPipeBind
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
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

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Active
Specifies that the active search topology should be returned.

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

[Online Version](http://technet.microsoft.com/EN-US/library/43e2c839-54b8-4f78-b883-abc1dbea617c(Office.15).aspx)

[New-SPEnterpriseSearchTopology]()

[Set-SPEnterpriseSearchTopology]()

[Remove-SPEnterpriseSearchTopology]()

