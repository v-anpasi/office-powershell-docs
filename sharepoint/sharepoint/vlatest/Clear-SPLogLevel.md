---
external help file: sharepoint.xml
online version: 
schema: 2.0.0
---

# Clear-SPLogLevel

## SYNOPSIS
Below Content Applies To: SharePoint Server 2013

## SYNTAX

```
Clear-SPLogLevel [-AssignmentCollection <SPAssignmentCollection>] [-Identity <String[]>]
 [-InputObject <PSObject>]
```

## DESCRIPTION
The Clear-SPLogLevel cmdlet resets the Windows event logging and trace logging levels for the specified categories to the default values.
If the Identity parameter is not provided, all categories are affected.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### --------------EXAMPLE 1----------------- (SharePoint Server 2013)
```
C:\PS>Clear-SPLogLevel -Identity Cat1
```

This example resets the log levels for a single category.

### --------------EXAMPLE 1----------------- (SharePoint Server 2016)
```
C:\PS>Clear-SPLogLevel -Identity Cat1
```

This example resets the log levels for a single category.

### --------------EXAMPLE 2----------------- (SharePoint Server 2013)
```
C:\PS>"Cat1", "Cat2", "Cat3" | Clear-SPLogLevel
```

This example resets the log levels for multiple categories.

### --------------EXAMPLE 2----------------- (SharePoint Server 2016)
```
C:\PS>"Cat1", "Cat2", "Cat3" | Clear-SPLogLevel
```

This example resets the log levels for multiple categories.

### --------------EXAMPLE 3----------------- (SharePoint Server 2013)
```
C:\PS>Get-SPLogLevel | Clear-SPLogLevel
```

This example resets the log levels for all categories.

### --------------EXAMPLE 3----------------- (SharePoint Server 2016)
```
C:\PS>Get-SPLogLevel | Clear-SPLogLevel
```

This example resets the log levels for all categories.

## PARAMETERS

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

### -Identity
Specifies the name(s) of the category or set of categories to set the throttle for; for example, "Unified Logging  Service".
If the Identity parameter is not specified, the event throttling setting is applied to all categories in the farm.

Providing an invalid category is a non-terminating error and will be ignored.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies the result of the InputObject parameter to be piped.
The value can be a string in a format identical to the Identity parameter, or can be an SPDiagnosticsCategory object.
The user can retrieve one or more categories from the Get-SPLogLevel cmdlet, modify their values, and then pipe the results to the Set-SPLogLevel cmdlet.

```yaml
Type: PSObject
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

