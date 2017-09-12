---
external help file: sharepoint.xml
online version: 
schema: 2.0.0
---

# Get-SPODataConnectionSetting

## SYNOPSIS
Below Content Applies To: SharePoint Server 2013

## SYNTAX

```
Get-SPODataConnectionSetting -ServiceContext <SPServiceContextPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Name <String>]
```

## DESCRIPTION
Use the Get-SPODataConnectionSetting cmdlet to display Business Connectivity Services OData connection properties for a specified Business Connectivity Services connection.

If the name of the connection is not specified by using the Name parameter, this cmdlet will return the list of the connections for the specified BDC service context.

This cmdlet applies to an on-premises environment only.
You cannot use this command in the SharePoint Online Management Shell.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ----------------EXAMPLE 1------------ (SharePoint Server 2013)
```
C:\PS>Get-SPODataConnectionSetting -ServiceContext  "http://contoso" -Name "ContosoServiceApp"
```

This example returns properties of the BCS connection named ContosoServiceApp

### ----------------EXAMPLE 1------------ (SharePoint Server 2016)
```
C:\PS>Get-SPODataConnectionSetting -ServiceContext  "http://contoso" -Name "ContosoServiceApp"
```

This example returns properties of the BCS connection named ContosoServiceApp

### ----------------EXAMPLE 2------------ (SharePoint Server 2013)
```
C:\PS>Get-SPODataConnectionSetting -ServiceContext "http://contoso"
```

This example returns a list of BCS connections for the service context named http://contoso

### ----------------EXAMPLE 2------------ (SharePoint Server 2016)
```
C:\PS>Get-SPODataConnectionSetting -ServiceContext "http://contoso"
```

This example returns a list of BCS connections for the service context named http://contoso

## PARAMETERS

### -ServiceContext
Specifies the service context which is in the form of an instance of an SPServiceContext object, an SPSiteAdministration object identifier, or a SPSite object.
An example of a service context value is an identifier from the ID field, a string identifier, a URI, or a string representation of a GUID.

```yaml
Type: SPServiceContextPipeBind
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

### -Name
Specifies the name of the Business Connectivity Services connection object.

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

[New-SPODataConnectionSetting]()

[Remove-SPODataConnectionSetting]()

[Set-SPODataConnectionSetting]()

