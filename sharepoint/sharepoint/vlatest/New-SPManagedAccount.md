---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/60a5a81a-4c8a-47d6-8226-81b1e9d2fab9(Office.15).aspx
schema: 2.0.0
---

# New-SPManagedAccount

## SYNOPSIS
Below Content Applies To: SharePoint Server 2013

## SYNTAX

```
New-SPManagedAccount [-Credential] <PSCredential> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-WhatIf]
```

## DESCRIPTION
The New-SPManagedAccount cmdlet registers a new managed account for the specified Credential or Username, and Password.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ------------------EXAMPLE----------------------- (SharePoint Server 2013)
```
C:\PS>$cred = Get-Credential

C:\PS>New-SPManagedAccount -Credential $cred
```

This example adds a new managed account to the farm by using credentials that are prompted.

### ------------------EXAMPLE----------------------- (SharePoint Server 2016)
```
C:\PS>$cred = Get-Credential

C:\PS>New-SPManagedAccount -Credential $cred
```

This example adds a new managed account to the farm by using credentials that are prompted.

## PARAMETERS

### -Credential
Indicates the Credential object that specifies the credentials of the new managed account.
If you use Credential, you cannot specify Username and Password.

```yaml
Type: PSCredential
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

### -Confirm
Prompts you for confirmation before running the cmdlet.

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
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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

