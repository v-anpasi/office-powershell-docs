---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/5551df7f-5f62-4c67-ae59-96b89e95a60a(Office.15).aspx
schema: 2.0.0
---

# Remove-SPEnterpriseSearchSiteHitRule

## SYNOPSIS
Deletes a site hit rule.

## SYNTAX

```
Remove-SPEnterpriseSearchSiteHitRule [-Identity] <SiteHitRulePipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-SearchService <SearchServicePipeBind>] [-WhatIf]
```

## DESCRIPTION
The Remove-SPEnterpriseSearchSiteHitRule cmdlet deletes the site hit rule that controls the number of threads used to crawl a given site.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ------------------EXAMPLE------------------- (SharePoint Server 2013)
```
Remove-SPEnterpriseSearchSiteHitRule -Identity myHost
```

This example removes a site hit rule for the myHost host.

### ------------------EXAMPLE------------------- (SharePoint Server 2016)
```
C:\PS>
Remove-SPEnterpriseSearchSiteHitRule -Identity myHost
```

This example removes a site hit rule for the myHost host.

## PARAMETERS

### -Identity
The rule that is used for the specified site.

The type must be a valid site hit rule host or an instance of a valid SiteHitRule object.

```yaml
Type: SiteHitRulePipeBind
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

### -SearchService
Specifies the search service in the farm that hosts the crawl.

The type must be an instance of a valid SearchService object; otherwise, the local service on the server that hosts the Windows PowerShell cmdlet is used.

```yaml
Type: SearchServicePipeBind
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

[Online Version](http://technet.microsoft.com/EN-US/library/5551df7f-5f62-4c67-ae59-96b89e95a60a(Office.15).aspx)

