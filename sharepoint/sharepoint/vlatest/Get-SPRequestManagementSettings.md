---
external help file: sharepoint.xml
online version: 
schema: 2.0.0
---

# Get-SPRequestManagementSettings

## SYNOPSIS
Below Content Applies To: SharePoint Server 2013

## SYNTAX

```
Get-SPRequestManagementSettings [-Identity] <SPRequestManagementSettingsPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>]
```

## DESCRIPTION
The Get-SPRequestManagementSettings cmdlet returns a Request Manager object which is base for performing any request manager management operation.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### -----------EXAMPLE------- (SharePoint Server 2013)
```
C:\PS>Get-SPRequestManagementSettings -Identity <GUID>
```

This example returns a request manager object for a specified identity.

### -----------EXAMPLE------- (SharePoint Server 2016)
```
C:\PS>Get-SPRequestManagementSettings -Identity <GUID>
```

This example returns a request manager object for a specified identity.

## PARAMETERS

### -Identity
Specifies the web-application for which a user wants to enable routing or throttling.

```yaml
Type: SPRequestManagementSettingsPipeBind
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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-SPRequestManagementSettings]()

[New-SPRequestManagementRuleCriteria]()

