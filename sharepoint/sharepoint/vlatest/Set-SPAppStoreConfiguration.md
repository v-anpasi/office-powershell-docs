---
external help file: sharepoint.xml
online version: 
schema: 2.0.0
---

# Set-SPAppStoreConfiguration

## SYNOPSIS
Below Content Applies To: SharePoint Server 2013

## SYNTAX

```
Set-SPAppStoreConfiguration [-Url <String>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-WhatIf] -Enable <Boolean>
```

## DESCRIPTION
Below Content Applies To: SharePoint Server 2013

Use the Set-SPAppStoreConfiguration cmdlet to set SharePoint Store settings for a specified app.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).
Below Content Applies To: SharePoint Server 2016

{{Fill in the Description}}

## EXAMPLES

### -----------EXAMPLE 1-------- (SharePoint Server 2013)
```
C:\PS>Set-SPAppStoreConfiguration -Url https://officetestfive1.microsoft.com -Enable $true
```

This example sets the URL to the Office.com server.

### Example 1 (SharePoint Server 2016)
```
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

### -----------EXAMPLE 2-------- (SharePoint Server 2013)
```
C:\PS>Set-SPAppStoreConfiguration -Enable $false
```

This example turns off the SharePoint Store.

### -----------EXAMPLE 3-------- (SharePoint Server 2013)
```
C:\PS>Set-SPAppStoreConfiguration -Enable $true
```

This example turns on the SharePoint Store.

## PARAMETERS

### -Url
Below Content Applies To: SharePoint Server 2013

Specifies the URL of the app for which to set SharePoint Store settings.

The SharePoint store value should not be changed unless instructed by a Microsoft representative.
Below Content Applies To: SharePoint Server 2016

{{Fill Url Description}}

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

### -AssignmentCollection
Below Content Applies To: SharePoint Server 2013

Manages objects for the purpose of proper disposal.
Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management.
Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory.
When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store.
If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.
Below Content Applies To: SharePoint Server 2016

{{Fill AssignmentCollection Description}}

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

Prompts you for confirmation before executing the command.
For more information, type the following command: get-help about_commonparameters Below Content Applies To: SharePoint Server 2016

Prompts you for confirmation before running the cmdlet.

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
Below Content Applies To: SharePoint Server 2013

Displays a message that describes the effect of the command instead of executing the command.
For more information, type the following command: get-help about_commonparameters Below Content Applies To: SharePoint Server 2016

Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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

### -Enable
{{Fill Enable Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

### Microsoft.SharePoint.PowerShell.SPAssignmentCollection

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-SPAppStoreConfiguration]()

