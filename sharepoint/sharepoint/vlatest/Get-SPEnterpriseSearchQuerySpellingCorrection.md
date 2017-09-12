---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/4a00b085-917b-48c2-a2cc-8252410b2a24(Office.15).aspx
schema: 2.0.0
---

# Get-SPEnterpriseSearchQuerySpellingCorrection

## SYNOPSIS
Returns the object that exposes the Query Spelling Correction (QSC) configuration.

## SYNTAX

```
Get-SPEnterpriseSearchQuerySpellingCorrection [[-Identity] <QuerySpellingCorrectionPipeBind>]
 -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## DESCRIPTION
This cmdlet returns the object that exposes the QSC configuration parameters.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ------------------EXAMPLE------------------ (SharePoint Server 2013)
```
$searchApp = Get-SPEnterpriseSearchServiceApplication

Get-SPEnterpriseSearchQuerySpellingCorrection -SearchApplication $searchApp
```

Returns the current configuration for the Query Spelling Correction component for the default Search service application.

### ------------------EXAMPLE------------------ (SharePoint Server 2016)
```
C:\PS>$searchApp = Get-SPEnterpriseSearchServiceApplication
Get-SPEnterpriseSearchQuerySpellingCorrection -SearchApplication $searchApp
```

Returns the current configuration for the Query Spelling Correction component for the default search service application.

## PARAMETERS

### -Identity
Specifies an object that represents the current status for the query spelling correction.

```yaml
Type: QuerySpellingCorrectionPipeBind
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchApplication
Below Content Applies To: SharePoint Server 2013

Specifies the Search service application that contains the query spelling correction parameters.
Below Content Applies To: SharePoint Server 2016

Specifies the search service application that contains the query spelling correction parameters.

```yaml
Type: SearchServiceApplicationPipeBind
Parameter Sets: (All)
Aliases: 

Required: True
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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Online Version](http://technet.microsoft.com/EN-US/library/4a00b085-917b-48c2-a2cc-8252410b2a24(Office.15).aspx)

