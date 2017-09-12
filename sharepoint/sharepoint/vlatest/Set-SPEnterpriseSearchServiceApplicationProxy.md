---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/460f7977-117b-4c9b-8085-d97ad30214dd(Office.15).aspx
schema: 2.0.0
---

# Set-SPEnterpriseSearchServiceApplicationProxy

## SYNOPSIS
Sets properties of a search service application proxy.

## SYNTAX

```
Set-SPEnterpriseSearchServiceApplicationProxy [-Identity] <SearchServiceApplicationProxyPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-Name <String>] [-WhatIf]
```

## DESCRIPTION
This cmdlet updates properties of a site administration service application proxy for a search application.
SPEnterpriseSearchServiceApplicationProxy represents the proxy for search site administration functionality.
One search service application proxy exists for each search application on a farm.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ------------------EXAMPLE------------------ (SharePoint Server 2013)
```
Get-SPEnterpriseSearchServiceApplicationProxy -Identity SsaProxy | Set- SPEnterpriseSearchServiceApplicationProxy -Name ContosoSearchProxy
```

This example sets the display name of a search service application proxy.

### ------------------EXAMPLE------------------ (SharePoint Server 2016)
```
C:\PS>Get-SPEnterpriseSearchServiceApplicationProxy -Identity SsaProxy | Set- SPEnterpriseSearchServiceApplicationProxy -Name ContosoSearchProxy
```

This example sets the display name of a search service application proxy.

## PARAMETERS

### -Identity
Specified the search service application proxy to update.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a search service application proxy (for example, SearchServiceAppProxy1); or an instance of a valid SearchServiceApplicationProxy object.

```yaml
Type: SearchServiceApplicationProxyPipeBind
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

### -Name
Specifies the display name of the search application proxy to retrieve.

The type must be a valid string, for example, SearchAppProxy1.

```yaml
Type: String
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

[Online Version](http://technet.microsoft.com/EN-US/library/460f7977-117b-4c9b-8085-d97ad30214dd(Office.15).aspx)

