---
external help file: sharepoint.xml
online version: 
schema: 2.0.0
---

# Get-SPAppInstance

## SYNOPSIS
Below Content Applies To: SharePoint Server 2013

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Get-SPAppInstance -Identity <SPAppInstance> [-AssignmentCollection <SPAssignmentCollection>]
```

### UNNAMED_PARAMETER_SET_2
```
Get-SPAppInstance -Site <SPSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>] -AppInstanceId <Guid>
```

### UNNAMED_PARAMETER_SET_3
```
Get-SPAppInstance [-App <SPApp>] [-AssignmentCollection <SPAssignmentCollection>] -Web <SPWebPipeBind>
```

## DESCRIPTION
This cmdlet contains more than one parameter set.
You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see Cmdlet Parameter Sets (http://go.microsoft.com/fwlink/?LinkID=187810).

Use the Get-AppInstance cmdlet to get a collection of app instances that are installed on an SPWeb object.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### -----------EXAMPLE 1----------- (SharePoint Server 2013)
```
C:\PS>$instances = Get-SPAppInstance -Web http://localhost
```

This example returns a collection if more than one app is installed on http://localhost.
If only one app is installed, a single object is returned.

### -----------EXAMPLE 1----------- (SharePoint Server 2016)
```
C:\PS>$instances = Get-SPAppInstance -Web http://localhost
```

This example returns a collection if more than one app is installed on http://localhost.
If only one app is installed, a single object is returned.

### -----------EXAMPLE 2----------- (SharePoint Server 2013)
```
C:\PS>$instance = Get-SPAppInstance -AppInstanceId $instance.Id
```

This example returns the ID of an instance of an app.

### -----------EXAMPLE 2----------- (SharePoint Server 2016)
```
C:\PS>$instance = Get-SPAppInstance -AppInstanceId $instance.Id
```

This example returns the ID of an instance of an app.

## PARAMETERS

### -Identity
Specifies the App instance for which to find metadata.

```yaml
Type: SPAppInstance
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Site
Sets the query scope to a site.

Subsites are not included.

```yaml
Type: SPSitePipeBind
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -App
Specifies the App.
This parameter returns metadata for all instances of an app.

```yaml
Type: SPApp
Parameter Sets: UNNAMED_PARAMETER_SET_3
Aliases: 

Required: False
Position: Named
Default value: None
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

### -AppInstanceId
{{Fill AppInstanceId Description}}

```yaml
Type: Guid
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Web
{{Fill Web Description}}

```yaml
Type: SPWebPipeBind
Parameter Sets: UNNAMED_PARAMETER_SET_3
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Restart-SPAppInstanceJobs]()

[Uninstall-SPAppInstance]()

[Update-SPAppInstance]()

