---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/eb1fdf2f-324d-4023-b534-93664b45d17d(Office.15).aspx
schema: 2.0.0
---

# Import-SPEnterpriseSearchThesaurus

## SYNOPSIS
Deploys the dictionary to the thesaurus component in the query processing flow.

## SYNTAX

```
Import-SPEnterpriseSearchThesaurus -FileName <String> -SearchApplication <SearchServiceApplicationPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf]
```

## DESCRIPTION
This cmdlet imports a thesaurus dictionary using a .cvs file, and deploys it to the query processing flow.
A previously deployed thesaurus is overwritten by an import of a new .cvs file.

NOTE: If an empty .cvs file is imported, an empty thesaurus will be deployed.
No synonyms will then be added to the queries.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ------------------EXAMPLE----------------- (SharePoint Server 2013)
```
$searchApp = Get-SPEnterpriseSearchServiceApplication


Import-SPEnterpriseSearchThesaurus -SearchApplication $searchApp -Filename \\host\share\thesaurus.csv
```

This example imports a thesaurus dictionary .cvs file named thesaurus.csv that is located at \\\\host\share to the default search service application.

### ------------------EXAMPLE----------------- (SharePoint Server 2016)
```
C:\PS>$searchApp = Get-SPEnterpriseSearchServiceApplication 
Import-SPEnterpriseSearchThesaurus -SearchApplication $searchApp -Filename 
\\host\share\thesaurus.csv
```

This example imports a thesaurus dictionary .cvs file named thesaurus.csv that is located at \\\\host\share  to the default search service application.

## PARAMETERS

### -FileName
Specifies the full UNC (Universal Naming Convention) path of the .cvs file to be imported.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchApplication
Specifies the search application to which the thesaurus dictionary should be imported

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

[Online Version](http://technet.microsoft.com/EN-US/library/eb1fdf2f-324d-4023-b534-93664b45d17d(Office.15).aspx)

