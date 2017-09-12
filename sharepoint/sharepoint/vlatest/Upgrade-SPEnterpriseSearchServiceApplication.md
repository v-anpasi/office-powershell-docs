---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/d864545d-2b27-4cc0-9c56-e421fb8d0641(Office.15).aspx
schema: 2.0.0
---

# Upgrade-SPEnterpriseSearchServiceApplication

## SYNOPSIS
Upgrades a search service application.

## SYNTAX

```
Upgrade-SPEnterpriseSearchServiceApplication [-Identity] <SearchServiceApplicationPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf]
```

## DESCRIPTION
This cmdlet starts an upgrade process on a search service application.
This cmdlet runs the associated upgrade actions for the search service application.
Also, you can upgrade multiple search service applications in parallel by starting several instances of this cmdlet.
It is not necessary to run this cmdlet if you already have run the SharePoint Products Configuration Wizard.

For the upgrade process to run successful, all of the computers in the farm must have the same version of binaries installed.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ----------------EXAMPLE 1----------------- (SharePoint Server 2013)
```
Get-SPEnterpriseSearchServiceApplication | Upgrade-SPEnterpriseSearchServiceApplication
```

This example upgrades a search service application.

### ----------------EXAMPLE 1----------------- (SharePoint Server 2016)
```
C:\PS>Get-SPEnterpriseSearchServiceApplication | Upgrade-SPEnterpriseSearchServiceApplication
```

This example upgrades a search service application.

### ----------------EXAMPLE 2----------------- (SharePoint Server 2013)
```
Upgrade-SPEnterpriseSearchServiceApplication -Identity 846ceb0b-31d6-4c79-82c1-3a9deafe0b45
```

This example upgrades a search service application.

### ----------------EXAMPLE 2----------------- (SharePoint Server 2016)
```
C:\PS>Upgrade-SPEnterpriseSearchServiceApplication -Identity 846ceb0b-31d6-4c79-82c1-3a9deafe0b45
```

This example upgrades a search service application.

### ----------------EXAMPLE 3----------------- (SharePoint Server 2013)
```
Upgrade-SPEnterpriseSearchServiceApplication "DefaultSearchApplication"
```

This example upgrades a search service application.

### ----------------EXAMPLE 3----------------- (SharePoint Server 2016)
```
C:\PS>Upgrade-SPEnterpriseSearchServiceApplication "DefaultSearchApplication"
```

This example upgrades a search service application.

## PARAMETERS

### -Identity
Specifies the search service application to upgrade.

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

[Online Version](http://technet.microsoft.com/EN-US/library/d864545d-2b27-4cc0-9c56-e421fb8d0641(Office.15).aspx)

