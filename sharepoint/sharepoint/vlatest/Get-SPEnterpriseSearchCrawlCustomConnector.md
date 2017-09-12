---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/bd3948e9-e1b5-453e-bd2d-85be7c859339(Office.15).aspx
schema: 2.0.0
---

# Get-SPEnterpriseSearchCrawlCustomConnector

## SYNOPSIS
Returns a CustomConnector object type.

## SYNTAX

```
Get-SPEnterpriseSearchCrawlCustomConnector -SearchApplication <SearchServiceApplicationPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Protocol <String>]
```

## DESCRIPTION
The Identity parameter displays a custom connector for a specified Web application.
If no parameters are specified, all the objects of the CustomConnector object type are returned.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### --------------------EXAMPLE---------------------- (SharePoint Server 2013)
```
$searchApp = Get-SPEnterpriseSearchServiceApplication MySearchServiceApp$crawlConn = Get-SPEnterpriseSearchCrawlCustomConnector -SearchApplication$searchApp -Protocol "http://"
```

This example obtains a reference to all custom crawl connectors for the http:// protocol for a search service application named MySearchServiceApp.

### --------------------EXAMPLE---------------------- (SharePoint Server 2016)
```
C:\PS>$searchApp = Get-SPEnterpriseSearchServiceApplication MySearchServiceApp
$crawlConn = Get-SPEnterpriseSearchCrawlCustomConnector -SearchApplication
$searchApp -Protocol "http://"
```

This example obtains a reference to all custom crawl connectors for the http:// protocol for a search service application named MySearchServiceApp.

## PARAMETERS

### -SearchApplication
Specifies the Search application with which the CustomConnector objects are associated.

```yaml
Type: SearchServiceApplicationPipeBind
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

### -Protocol
Specifies the string version of the protocol for which to return the CustomConnector object.
For example, "dctm://"

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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Online Version](http://technet.microsoft.com/EN-US/library/bd3948e9-e1b5-453e-bd2d-85be7c859339(Office.15).aspx)

