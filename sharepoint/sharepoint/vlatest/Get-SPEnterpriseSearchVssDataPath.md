---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/26d6e44c-a606-47a1-a3e0-c4919670f684(Office.15).aspx
schema: 2.0.0
---

# Get-SPEnterpriseSearchVssDataPath

## SYNOPSIS
Retrieves the index paths for all active search index components on the current server.

## SYNTAX

```
Get-SPEnterpriseSearchVssDataPath [-AssignmentCollection <SPAssignmentCollection>]
```

## DESCRIPTION
Below Content Applies To: SharePoint Server 2013

This cmdlet retrieves the index paths for all active index components on the current server.
This list is required as input by the Search VSS Writer in order to perform VSS backup of the current server.
This cmdlet will typically be called from a VSS script, and rarely used directly.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).
Below Content Applies To: SharePoint Server 2016

This cmdlet retrieves the index paths for all active index components on the current server. 
This list is required as input by the Search VSS Writer in order to perform VSS backup of the current server. 
This cmdlet will typically be called from a VSS script, and rarely used directly.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ------------------EXAMPLE----------------- (SharePoint Server 2013)
```
Get-SPEnterpriseSearchVssDataPath
```

This example gets the index paths for all active index components on the current server.

### ------------------EXAMPLE----------------- (SharePoint Server 2016)
```
C:\PS>Get-SPEnterpriseSearchVssDataPath
```

This example gets the index paths for all active index components on the current server.

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

[Online Version](http://technet.microsoft.com/EN-US/library/26d6e44c-a606-47a1-a3e0-c4919670f684(Office.15).aspx)

