---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/26d6e44c-a606-47a1-a3e0-c4919670f684(Office.15).aspx
schema: 2.0.0
---

# Get-SPFeature

## SYNOPSIS
Below Content Applies To: SharePoint Server 2013

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Get-SPFeature [[-Identity] <SPFeatureDefinitionPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
 [-Farm] [-Limit <String>]
```

### UNNAMED_PARAMETER_SET_2
```
Get-SPFeature [[-Identity] <SPFeatureDefinitionPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
 [-Limit <String>] [-Site <SPSitePipeBind>] [-Sandboxed]
```

### UNNAMED_PARAMETER_SET_3
```
Get-SPFeature [[-Identity] <SPFeatureDefinitionPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
 [-Limit <String>] [-Web <SPWebPipeBind>]
```

### UNNAMED_PARAMETER_SET_4
```
Get-SPFeature [[-Identity] <SPFeatureDefinitionPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
 [-Limit <String>] [-WebApplication <SPWebApplicationPipeBind>]
```

### UNNAMED_PARAMETER_SET_5
```
Get-SPFeature [[-Identity] <SPFeatureDefinitionPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
 [-Limit <String>] [-CompatibilityLevel <Int32>]
```

## DESCRIPTION
This cmdlet contains more than one parameter set.
You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see Cmdlet Parameter Sets (http://go.microsoft.com/fwlink/?LinkID=187810).

All parameter sets take the Identity parameter, which can be either the relative path of the SharePoint Feature (considered the feature name) or the GUID of a Feature definition.
If the Identity parameter is provided, the cmdlets attempt to find the given Feature definition or instance for the given scope.
If no parameters are specified, all installed features are returned.

The Get-SPFeature cmdlet behaves differently at each scope, returning the enabled Features at each level.
If no scope is provided, all installed Features are returned.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### --------------EXAMPLE 1----------------- (SharePoint Server 2013)
```
C:\PS>Get-SPFeature -Limit ALL | Where-Object {$_.Scope -eq "SITE"}
```

This example returns a list of all installed SITE scoped Features.

### --------------EXAMPLE 1----------------- (SharePoint Server 2016)
```
C:\PS>Get-SPFeature -Limit ALL | Where-Object {$_.Scope -eq "SITE"}
```

This example returns a list of all installed SITE scoped Features.

### --------------EXAMPLE 2----------------- (SharePoint Server 2013)
```
C:\PS>Get-SPSite http://somesite | Get-SPWeb -Limit ALL |%{ Get-SPFeature -Web $_ } | Select DisplayName,ID -Unique
```

This example returns the name and identifier (ID) of each uniquely enabled Feature on every SPWeb object in the site collection at http://somesite.

### --------------EXAMPLE 2----------------- (SharePoint Server 2016)
```
C:\PS>Get-SPSite http://somesite | Get-SPWeb -Limit ALL |%{ Get-SPFeature -Web $_ } | Select DisplayName,ID -Unique
```

This example returns the name and identifier (ID) of each uniquely enabled Feature on every SPWeb object in the site collection at http://somesite.

## PARAMETERS

### -Identity
Specifies the name of the Feature to retrieve.

The type must be the full or partial name, in the form  Feature1, or a GUID, in the form  1234-4567-9879, of the Feature to get .

```yaml
Type: SPFeatureDefinitionPipeBind
Parameter Sets: (All)
Aliases: 

Required: False
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

### -Farm
Specifies that if this parameter is used, only enabled farm Features are displayed.

```yaml
Type: SwitchParameter
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Limit
Limits the display results.
If "All" is specified, all Features are displayed.

The type must be a valid number greater than 0.
The default value is 200.

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

### -Site
Specifies the name of the site collection from which to get enabled Features.

The type must be a valid URL for a site collection, in the form http://server_name .

```yaml
Type: SPSitePipeBind
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Web
Specifies the URL or GUID of the Web.

The type must be a valid URL, in the form  http://server_name , or a GUID, in the form 1234-5678-9876-0987.

```yaml
Type: SPWebPipeBind
Parameter Sets: UNNAMED_PARAMETER_SET_3
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApplication
Specifies the name of the Web application from which to get enabled Features.

The type must be a valid URL to the Web application in the form http://server_name .

```yaml
Type: SPWebApplicationPipeBind
Parameter Sets: UNNAMED_PARAMETER_SET_4
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CompatibilityLevel
{{Fill CompatibilityLevel Description}}

```yaml
Type: Int32
Parameter Sets: UNNAMED_PARAMETER_SET_5
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sandboxed
{{Fill Sandboxed Description}}

```yaml
Type: SwitchParameter
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 

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

