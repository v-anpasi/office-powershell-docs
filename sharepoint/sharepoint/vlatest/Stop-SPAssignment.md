---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/55060c1d-4024-438e-b31d-6854df8b00d5(Office.15).aspx
schema: 2.0.0
---

# Stop-SPAssignment

## SYNOPSIS
Below Content Applies To: SharePoint Server 2013

## SYNTAX

```
Stop-SPAssignment [[-SemiGlobal] <SPAssignmentCollection>] [-AssignmentCollection <SPAssignmentCollection>]
 [-Global]
```

## DESCRIPTION
The Stop-SPAssignment cmdlet disposes of objects in the provided assignment collection.
Use the Global parameter to dispose of all objects in the global assignment collector and to stop the global store from collecting additional objects.
Provide a SemiGlobal assignment collector to dispose of all contained objects.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ------------------EXAMPLE------------------ (SharePoint Server 2013)
```
C:\PS>Start-SPAssignment -global

C:\PS>$w=Get-SPWeb http://MyWeb

C:\PS>$w | Set-SPWeb -title "Accounting"

C:\PS>Stop-SPAssignment -global
```

This example uses simple assignment.
While easier to use simple assignment, running commands that iterate through multiple SPSite or SPWeb objects while simple assignment is enabled is not recommended.
Ensure that Stop-SPAssignment is run before attempting any iterations of multiple objects.

### ------------------EXAMPLE------------------ (SharePoint Server 2016)
```
C:\PS>Start-SPAssignment -global

C:\PS>$w = Get-SPWeb http://MyWeb

C:\PS>$w | Set-SPWeb -title "Accounting"

C:\PS>Stop-SPAssignment -global
```

This example uses simple assignment.
While easier to use simple assignment, running commands that iterate through multiple SPSite or SPWeb objects while simple assignment is enabled is not recommended.
Ensure that Stop-SPAssignment is run before attempting any iterations of multiple objects.

## PARAMETERS

### -SemiGlobal
Provides the assignment collector from which to dispose of objects.

```yaml
Type: SPAssignmentCollection
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

### -Global
Stops the global assignment collector from storing objects, and disposes of any objects contained by the global assignment collector.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
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

