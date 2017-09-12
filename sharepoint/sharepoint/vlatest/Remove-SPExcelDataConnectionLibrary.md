---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/15289d89-02bb-4d34-abf8-6fb217ffe341(Office.15).aspx
schema: 2.0.0
---

# Remove-SPExcelDataConnectionLibrary

## SYNOPSIS
Removes a data connection library from Excel Services Application.

## SYNTAX

```
Remove-SPExcelDataConnectionLibrary [-Identity] <SPExcelDCLPipeBind>
 -ExcelServiceApplication <SPExcelServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
 [-Confirm] [-WhatIf]
```

## DESCRIPTION
The Remove-SPExcelDataConnectionLibrary cmdlet removes a library from the Excel Services Application trusted data connection libraries list. 
Excel Services Application loads data connection files only if they are stored in a data connection library that is on the trusted data connection libraries list.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### --------------EXAMPLE 1-------------- (SharePoint Server 2013)
```
C:\PS>Get-SPExcelServiceApplication -Identity "MyExcelService" | Remove- SPExcelDataConnectionLibrary -Identity "http://portal/site/salesDCL"
```

This example removes the http://portal/site/salesDCL library from the list of trusted data connection libraries, which is on the Excel Services Application Web service application named MyExcelService.

Connection files are no longer loaded from this library.
Workbooks that depend on this connection file might not refresh data.

### --------------EXAMPLE 2-------------- (SharePoint Server 2013)
```
C:\PS>Get-SPExcelServiceApplication | Get-SPExcelDataConnectionLibrary | Remove-SPExcelDataConnectionLibrary
```

This example removes all data connection libraries from all Excel Services Application running in the farm.

Connection files are no longer loaded from any libraries.
Workbooks that depend on any connection files might not refresh data.

## PARAMETERS

### -Identity
Specifies the data connection library to remove.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a data connection library (for example, DataConnectionLib1); a valid URL, in the form http://server_name; or an instance of a valid SPExcelDCL object.

```yaml
Type: SPExcelDCLPipeBind
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ExcelServiceApplication
Specifies the Excel Services Application Web service application that contains the SPExcelDataConnectionLibrary list object.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of an Excel Services Application Web service application in the farm (for example, MyExcelService1); or an instance of a valid SPExcelServiceApplication object.

```yaml
Type: SPExcelServiceApplicationPipeBind
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

