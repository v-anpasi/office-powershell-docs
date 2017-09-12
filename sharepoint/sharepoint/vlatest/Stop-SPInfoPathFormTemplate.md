---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/985591b0-951f-4274-aead-a184398bba41(Office.15).aspx
schema: 2.0.0
---

# Stop-SPInfoPathFormTemplate

## SYNOPSIS
Disables a InfoPath 2013 form template on a farm before an upgrade.

## SYNTAX

```
Stop-SPInfoPathFormTemplate [-Identity] <SPFormTemplatePipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-TimeLeft <Int32>] [-WhatIf]
```

## DESCRIPTION
The Stop-SPInfoPathFormTemplate cmdlet quiesces, or disables, an InfoPath 2013 form template before it upgrades the form.
Before a form is updated it is quiesced, which disables access to the form.
Use Start-SPIPFormTemplate to unquiesce, or activate, a form template after the form is upgraded.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ---------------EXAMPLE-------------- (SharePoint Server 2013)
```
C:\PS>Stop-SPInfoPathFormTemplate -Identity formName.xsn
```

This example disables a form template for a specified name.

### ---------------EXAMPLE-------------- (SharePoint Server 2016)
```
C:\PS>Stop-SPInfoPathFormTemplate -Identity formName.xsn
```

This example disables a form template for a specified name.

## PARAMETERS

### -Identity
Specifies the InfoPath 2013 form template to start.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a form template (for example, InfoPathFormTemplate1); a valid name of a form template files (for example, FormTemplateFile1.xsn); or an instance of a valid SPFormTemplate object.

```yaml
Type: SPFormTemplatePipeBind
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

### -TimeLeft
Specifies the time duration, in minutes, before the form template will be quiesced.
The default value is 0.

An integer value in the range from 0 to 1440.

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

