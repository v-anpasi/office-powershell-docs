---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/5bff925f-3845-434e-be9f-3ba50673be28(Office.15).aspx
schema: 2.0.0
---

# Move-SPEnterpriseSearchLinksDatabases

## SYNOPSIS
Moves data across links databases.

## SYNTAX

```
Move-SPEnterpriseSearchLinksDatabases [-SearchApplication] <SearchServiceApplicationPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-RepartitioningId <Guid>]
 [-SourceStores <LinksStore[]>] [-TargetStores <LinksStore[]>] [-WhatIf]
```

## DESCRIPTION
The Move-SPEnterpriseSearchLinksDatabases cmdlet moves data across a given list of links databases during farm configuration and scale out, to improve the performance and resource load of the farm.
Once the move has started, the cmdlet will return a unique identifier, the RepartitioningId.
Use this identifier to retrigger if the current run fails.
After the move has finished, the old databases can be removed.

A links database stores query logging and analytics information.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### --------EXAMPLE-------- (SharePoint Server 2013)
```
$ssa=Get-SPEnterpriseSearchServiceapplication
$ssa | New-SPEnterpriseSearchLinksDatabase -DatabaseName "links1"
$ssa | New-SPEnterpriseSearchLinksDatabase -DatabaseName "links2"
$ssa | New-SPEnterpriseSearchLinksDatabase -DatabaseName "links3"
$dbs = $ssa | Get-SPEnterpriseSearchLinksDatabase
$ssa | Repartition-SPEnterpriseSearchLinksDatabases -TargetStores $dbs
```

This example adds 3 new links databases and uses Move-SPEnterpriseSearchLinksDatabases to move data from the current links databases into new databases.

### --------EXAMPLE-------- (SharePoint Server 2016)
```
C:\PS>$ssa=Get-SPEnterpriseSearchServiceapplication
$ssa | New-SPEnterpriseSearchLinksDatabase -DatabaseName "links1"
$ssa | New-SPEnterpriseSearchLinksDatabase -DatabaseName "links2"
$ssa | New-SPEnterpriseSearchLinksDatabase -DatabaseName "links3"
$dbs = $ssa | Get-SPEnterpriseSearchLinksDatabase
$ssa | Repartition-SPEnterpriseSearchLinksDatabases -TargetStores $dbs
```

This example adds 3 new links databases and uses Move-SPEnterpriseSearchLinksDatabases to move data from the current links databases into new databases.

## PARAMETERS

### -SearchApplication
Below Content Applies To: SharePoint Server 2013

Specifies the search application that contains the links database.
The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid SearchServiceApplication object.
Below Content Applies To: SharePoint Server 2016

Specifies the search application that contains the links database.
The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid SearchServiceApplication object.

Specifies the search application that contains the links database.
The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid SearchServiceApplication object.

```yaml
Type: SearchServiceApplicationPipeBind
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AssignmentCollection
Below Content Applies To: SharePoint Server 2013

{{Fill AssignmentCollection Description}} Below Content Applies To: SharePoint Server 2016

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
Below Content Applies To: SharePoint Server 2013

Prompts you for confirmation before running the cmdlet.
Below Content Applies To: SharePoint Server 2016

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

### -RepartitioningId
Below Content Applies To: SharePoint Server 2013

{{Fill RepartitioningId Description}} Below Content Applies To: SharePoint Server 2016

Resumes the move with this identifier.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceStores
Below Content Applies To: SharePoint Server 2013

{{Fill SourceStores Description}} Below Content Applies To: SharePoint Server 2016

Specifies a source list of databases.
If this parameter is not specified then all currently existing links databases will be used as a source list.

```yaml
Type: LinksStore[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetStores
Below Content Applies To: SharePoint Server 2013

{{Fill TargetStores Description}} Below Content Applies To: SharePoint Server 2016

Specifies a target list of databases.
If this parameter is not specified then all currently existing links databases will be used as a target list.

```yaml
Type: LinksStore[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Below Content Applies To: SharePoint Server 2013

Shows what would happen if the cmdlet runs.
The cmdlet is not run.
Below Content Applies To: SharePoint Server 2016

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

[Online Version](http://technet.microsoft.com/EN-US/library/5bff925f-3845-434e-be9f-3ba50673be28(Office.15).aspx)

[New-SPEnterpriseSearchLinksDatabase]()

[Set-SPEnterpriseSearchLinksDatabase]()

[Get-SPEnterpriseSearchLinksDatabase]()

[Remove-SPEnterpriseSearchLinksDatabase]()

