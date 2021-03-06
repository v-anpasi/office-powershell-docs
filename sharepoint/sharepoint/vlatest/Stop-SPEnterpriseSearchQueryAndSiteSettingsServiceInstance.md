---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/ca0e1528-4e67-4e34-87db-e34e373df740(Office.15).aspx
schema: 2.0.0
---

# Stop-SPEnterpriseSearchQueryAndSiteSettingsServiceInstance

## SYNOPSIS
Stops an instance of a search manager service.

## SYNTAX

```
Stop-SPEnterpriseSearchQueryAndSiteSettingsServiceInstance
 [-Identity] <SearchQueryAndSiteSettingsServiceInstancePipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf]
```

## DESCRIPTION
The Stop-SPEnterpriseSearchQueryAndSiteSettingsServiceInstance cmdlet stops an instance of a search manager service.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ------------------EXAMPLE------------------ (SharePoint Server 2013)
```
$qssInstance = Get-SPEnterpriseSearchQueryAndSiteSettingsServiceInstance -LocalStop-SPEnterpriseSearchQueryAndSiteSettingsServiceInstance -Identity $qssInstance
```

This example stops the local query and site settings service instance.

### ------------------EXAMPLE------------------ (SharePoint Server 2016)
```
C:\PS>$qssInstance = Get-SPEnterpriseSearchQueryAndSiteSettingsServiceInstance -Local
Stop-SPEnterpriseSearchQueryAndSiteSettingsServiceInstance -Identity $qssInstance
```

This example stops the local query and site settings service instance.

## PARAMETERS

### -Identity
Specifies the search manager service instance to stop.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid SPServer name, or the name of a search manager service instance (for example, SearchManagerServiceInstance1); or an instance of a valid SearchManagerServiceInstance object.

```yaml
Type: SearchQueryAndSiteSettingsServiceInstancePipeBind
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

[Online Version](http://technet.microsoft.com/EN-US/library/ca0e1528-4e67-4e34-87db-e34e373df740(Office.15).aspx)

