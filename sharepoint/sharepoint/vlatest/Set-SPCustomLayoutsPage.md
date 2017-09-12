---
external help file: sharepoint.xml
online version: 
schema: 2.0.0
---

# Set-SPCustomLayoutsPage

## SYNOPSIS
Below Content Applies To: SharePoint Server 2013

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Set-SPCustomLayoutsPage -Identity <SPCustomPage> -RelativePath <String>
 -WebApplication <SPWebApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-WhatIf] [-CompatibilityLevel <Int32>]
```

### UNNAMED_PARAMETER_SET_2
```
Set-SPCustomLayoutsPage -Identity <SPCustomPage> [-Reset] -WebApplication <SPWebApplicationPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf] [-CompatibilityLevel <Int32>]
```

## DESCRIPTION
This cmdlet contains more than one parameter set.
You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see Cmdlet Parameter Sets (http://go.microsoft.com/fwlink/?LinkID=187810).

The Set-SPCustomLayoutsPage cmdlet maps a new path for a custom layouts page in a Web application.
To remove the mapping for a custom layouts page, use the Reset parameter instead of the RelativePath parameter.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ------------------EXAMPLE----------------------- (SharePoint Server 2013)
```
C:\PS>Set-SPCustomLayoutsPage -Identity "_layouts/accessdenied.aspx" -RelativePath "/_layouts/custompages/myaccessdenied.aspx" -WebApplication "http://server_name/mywebapp"
```

This example maps the specified path for the AccessDenied layout page in the Web application "http://server_name/mywebapp".

### ------------------EXAMPLE----------------------- (SharePoint Server 2016)
```
C:\PS>Set-SPCustomLayoutsPage -Identity "_layouts/accessdenied.aspx" -RelativePath "/_layouts/custompages/myaccessdenied.aspx" -WebApplication "http://server_name/mywebapp"
```

This example maps the specified path for the AccessDenied layout page in the Web application "http://server_name/mywebapp".

## PARAMETERS

### -Identity
Specifies the custom layout page to set.

The type must be one of the following: None, AccessDenied, Confirmation, Error, Login, RequestAccess, Signout, or WebDeleted.

```yaml
Type: SPCustomPage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RelativePath
Specifies the path of the custom layout page.

The type must be a valid path of a layout page, in the form _layouts/custompages/myaccessdenied.aspx.

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Reset
Resets the mapping of a custom layouts page.

```yaml
Type: SwitchParameter
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApplication
Specifies the SharePoint Web application that contains the custom layout page.

The type must be a valid URL, in the form http://server_name; a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of SharePoint Web application (for example, MyOfficeApp1); or an instance of a valid SPWebApplication object.

```yaml
Type: SPWebApplicationPipeBind
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
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

### -CompatibilityLevel
{{Fill CompatibilityLevel Description}}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

