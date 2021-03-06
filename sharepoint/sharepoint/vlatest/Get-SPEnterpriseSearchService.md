---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/fcf865a8-b46b-44fb-89ba-f52e20876f6c(Office.15).aspx
schema: 2.0.0
---

# Get-SPEnterpriseSearchService

## SYNOPSIS
Returns the search service for the farm.

## SYNTAX

```
Get-SPEnterpriseSearchService [-AssignmentCollection <SPAssignmentCollection>]
```

## DESCRIPTION
This cmdlet returns the SearchService object when the search service is updated or deleted.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ------------------EXAMPLE------------------ (SharePoint Server 2013)
```
$searchService = Get-SPEnterpriseSearchService
```

This example obtains a reference to the search service of the current farm.

### ------------------EXAMPLE------------------ (SharePoint Server 2016)
```
C:\PS>$searchService = Get-SPEnterpriseSearchService
```

This example obtains a reference to the search service of the current farm.

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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Online Version](http://technet.microsoft.com/EN-US/library/fcf865a8-b46b-44fb-89ba-f52e20876f6c(Office.15).aspx)

