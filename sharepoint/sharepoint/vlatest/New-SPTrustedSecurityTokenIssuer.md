---
external help file: sharepoint.xml
online version: 
schema: 2.0.0
---

# New-SPTrustedSecurityTokenIssuer

## SYNOPSIS
Below Content Applies To: SharePoint Server 2013

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
New-SPTrustedSecurityTokenIssuer [-Name] <String> -Certificate <X509Certificate2>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-Description <String>] [-IsTrustBroker]
 [-RegisteredIssuerName <String>] [-WhatIf]
```

### UNNAMED_PARAMETER_SET_2
```
New-SPTrustedSecurityTokenIssuer [-Name] <String> -MetadataEndPoint <Uri>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-Description <String>] [-IsTrustBroker]
 [-RegisteredIssuerName <String>] [-WhatIf]
```

## DESCRIPTION
This cmdlet contains more than one parameter set.
You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see Cmdlet Parameter Sets (http://go.microsoft.com/fwlink/?LinkID=187810).

Use the New-SPTrustedSecurityTokenIssuer cmdlet to establish a trust between a server to server principal.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### -----------EXAMPLE----------- (SharePoint Server 2013)
```
C:\PS>New-SPTrustedSecurityTokenIssuer -Name "SPFarmA" -MetadataEndPoint https://mysite/my/_layouts/metadata/test/1/ -isSelfIssuer "false"
```

This example creates a new trusted security token named SPFarmA.

### -----------EXAMPLE----------- (SharePoint Server 2016)
```
C:\PS>New-SPTrustedSecurityTokenIssuer -Name "SPFarmA" -MetadataEndPoint https://mysite/my/_layouts/metadata/test/1/ -isSelfIssuer "false"
```

This example creates a new trusted security token named SPFarmA.

## PARAMETERS

### -Name
Specifies the name of the issuer.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Certificate
Specifies the X509Certificate object that represents the public key of the signing certificate of the security token issuer.

```yaml
Type: X509Certificate2
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MetadataEndPoint
Specifies the URI for the metadata endpoint of the issuer.

```yaml
Type: Uri
Parameter Sets: UNNAMED_PARAMETER_SET_2
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

### -Description
Specifies the description of the issuer.

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

### -IsTrustBroker
Specifies whether the trust is established with a self-issuer partner app (that is, Exchange Server 2010 or Exchange Server 2007 or Lync).

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

### -RegisteredIssuerName
@{Text=}

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

[Get-SPTrustedSecurityTokenIssuer]()

[Remove-SPTrustedSecurityTokenIssuer]()

[Set-SPTrustedSecurityTokenIssuer]()

