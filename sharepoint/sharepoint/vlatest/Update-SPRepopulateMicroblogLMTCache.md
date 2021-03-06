---
external help file: sharepoint.xml
online version: 
schema: 2.0.0
---

# Update-SPRepopulateMicroblogLMTCache

## SYNOPSIS
Refreshes the cache.

## SYNTAX

```
Update-SPRepopulateMicroblogLMTCache -ProfileServiceApplicationProxy <SPServiceApplicationProxyPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>]
```

## DESCRIPTION
Use the Update-SPRepopulateMicroblogLMTCache cmdlet to refresh when the Feed Cache Repopulation Job timer job fails to work.
The Update-SPRepopulateMicroblogLMTCache cmdlet forcefully refreshes the last modified times of all the known persisted entities to FeedCache.

When you refresh the cache, the Update-SPRepopulateMicroblogLMTCache cmdlet should be run first, and then the Update-SPRepopulateMicroblogFeedCache cmdlet second.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ------------EXAMPLE----------- (SharePoint Server 2013)
```
C:\PS>Update-SPRepopulateMicroblogLMTCache -ProfileServiceApplicationProxy a4f93369-0795-4aee-8a21-46f5ade29606
```

This example refreshes the cache for the specified proxy.

### ------------EXAMPLE----------- (SharePoint Server 2016)
```
C:\PS>Update-SPRepopulateMicroblogLMTCache -ProfileServiceApplicationProxy a4f93369-0795-4aee-8a21-46f5ade29606
```

This example refreshes the cache for the specified proxy.

## PARAMETERS

### -ProfileServiceApplicationProxy
Specifies the User Profile Service application proxy to update.

The type must be in one of the following forms:

--A valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh
--A valid name of a service application proxy (for example, UserProfileSvcProxy1)
--An instance of a valid SPServiceApplicationProxy object

```yaml
Type: SPServiceApplicationProxyPipeBind
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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Update-SPRepopulateMicroblogFeedCache]()

