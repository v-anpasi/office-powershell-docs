---
external help file: sharepoint.xml
online version: 
schema: 2.0.0
---

# Clear-SPMetadataWebServicePartitionData

## SYNOPSIS
Removes all data for a site subscription on a metadata Web service application.

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Clear-SPMetadataWebServicePartitionData [-Identity] <SPSiteSubscriptionPipeBind>
 [-ServiceProxy] <SPMetadataServiceProxyCmdletPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
 [-FromContentDatabase <SPContentDatabasePipeBind>] [-FromServiceDatabase]
```

### UNNAMED_PARAMETER_SET_2
```
Clear-SPMetadataWebServicePartitionData [-ServiceProxy] <SPMetadataServiceProxyCmdletPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] -ServiceContext <SPServiceContextPipeBind>
 [-FromContentDatabase <SPContentDatabasePipeBind>] [-FromServiceDatabase]
```

## DESCRIPTION
Use the Clear-SPMetadataWebServicePartitionData cmdlet to clear all data for a site subscription on a metadata Web service application.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ----------------EXAMPLE--------------- (SharePoint Server 2013)
```
C:\PS>Clear-SPMetadataWebServicePartitionData -Identity $siteSubscriptionPipeBind1 -ServiceProxy "MetadataServiceProxy2"
```

This example removes data for a site subscription on a Metadata Service application.

### ----------------EXAMPLE--------------- (SharePoint Server 2016)
```
C:\PS>Clear-SPMetadataWebServicePartitionData -Identity $siteSubscriptionPipeBind1 -ServiceProxy "MetadataServiceProxy2"
```

This example removes data for a site subscription on a Metadata Service application.

## PARAMETERS

### -Identity
Specifies the site subscription configuration to remove.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a site subscription (for example, SiteSubscriptionConfig1); or an instance of a valid SiteSubscription object.

```yaml
Type: SPSiteSubscriptionPipeBind
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ServiceProxy
Specifies the service proxy for the service application that contains the site subscription.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of the service application proxy (for example, ServiceAppProxy1); or an instance of a valid SPMetadataServiceProxy object.

```yaml
Type: SPMetadataServiceProxyCmdletPipeBind
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

### -ServiceContext
{{Fill ServiceContext Description}}

```yaml
Type: SPServiceContextPipeBind
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -FromContentDatabase
{{Fill FromContentDatabase Description}}

```yaml
Type: SPContentDatabasePipeBind
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FromServiceDatabase
{{Fill FromServiceDatabase Description}}

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

