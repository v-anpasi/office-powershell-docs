---
external help file: sharepoint.xml
online version: 
schema: 2.0.0
---

# Register-SPAppPrincipal

## SYNOPSIS
Below Content Applies To: SharePoint Server 2013

## SYNTAX

```
Register-SPAppPrincipal -DisplayName <String> -NameIdentifier <String> -Site <SPWebPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>]
```

## DESCRIPTION
Use the Register-SPAppPrincipal cmdlet to let an on-premise farm or SharePoint Online administrator to register an app principal management service.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ------------EXAMPLE-------- (SharePoint Server 2013)
```
C:\PS>$site = Get-SPSite "https://<urlofsite>"

C:\PS>Register-SPAppPrincipal -site $site.root -NameIdentifier "00000003-0000-0ff1-ce00-000000000000@f686d426-8d16-42db-81b7-cb578e110ccd" -DisplayName "Contoso SharePoint Online"
```

This example registers the app principal named Contoso SharePoint Online.

### ------------EXAMPLE-------- (SharePoint Server 2016)
```
C:\PS>$site = Get-SPSite "https://<urlofsite>"

C:\PS>Register-SPAppPrincipal -site $site.root -NameIdentifier "00000003-0000-0ff1-ce00-000000000000@f686d426-8d16-42db-81b7-cb578e110ccd" -DisplayName "Contoso SharePoint Online"
```

This example registers the app principal named Contoso SharePoint Online.

## PARAMETERS

### -DisplayName
Specifies the friendly name to use for the app principal that is being registered.

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

### -NameIdentifier
Specifies the app principal's name identifier that needs to be added to the app management service.

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

### -Site
@{Text=}

```yaml
Type: SPWebPipeBind
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

[Get-SPAppPrincipal]()

