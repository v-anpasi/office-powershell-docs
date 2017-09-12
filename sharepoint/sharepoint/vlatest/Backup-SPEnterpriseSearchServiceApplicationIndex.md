---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/625bd9f3-d7f5-4d8a-9edf-6cb270ce27b3(Office.15).aspx
schema: 2.0.0
---

# Backup-SPEnterpriseSearchServiceApplicationIndex

## SYNOPSIS
Takes a backup of the search index to a specified backup location.

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Backup-SPEnterpriseSearchServiceApplicationIndex [-Phase] <Int32>
 [-SearchApplication] <SearchServiceApplication> [-BackupFolder] <String> [-BackupHandleFile] <String>
 [[-Retries] <Int32>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf] [-PeerToPeer]
 [-SpecifiedBackupHandle <String>]
```

### UNNAMED_PARAMETER_SET_2
```
Backup-SPEnterpriseSearchServiceApplicationIndex [-SearchApplication] <SearchServiceApplication>
 [-BackupHandleFile] <String> [[-Retries] <Int32>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-WhatIf] [-Abort] [-PeerToPeer] [-SpecifiedBackupHandle <String>]
```

## DESCRIPTION
Below Content Applies To: SharePoint Server 2013

This cmdlet will take a backup of the search index to a specified backup location.
The cmdlet has to be run in two phases.
Phase one will take a backup of what is present in the index at the time that the backup cmdlet is run.
Phase two will take a differential backup of what was added to the index after you started the first phase index backup.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).
Below Content Applies To: SharePoint Server 2016

This cmdlet will take a backup of the search index to a specified backup location. 
The cmdlet has to be run in two phases. 
Phase one will take a backup of what is present in the index at the time that the backup cmdlet is run. 
Phase two will take a differential backup of what was added to the index after you started the first phase index backup.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ------------------EXAMPLE 1------------------ (SharePoint Server 2013)
```
$ssa = Get-SPEnterpriseSearchServiceApplicationBackup-SPEnterpriseSearchServiceApplicationIndex -Phase 1 -SearchApplication $ssa -BackupFolder "\\backuphost\backupfolder" -BackupHandleFile "\\backuphost\backupfolder\backuphandle.txt" -Retries 3
```

This example starts a Phase 1 backup of the search index for the default search application, and stores the backup at the location \\\\backuphost\backupfolder.
The cmdlet stores a handle file backuphandle.txt that is used by the second phase cmdlet.

### ------------------EXAMPLE 1------------------ (SharePoint Server 2016)
```
C:\PS>$ssa = Get-SPEnterpriseSearchServiceApplication
Backup-SPEnterpriseSearchServiceApplicationIndex -Phase 1 -SearchApplication $ssa -BackupFolder "\\backuphost\backupfolder" -BackupHandleFile "\\backuphost\backupfolder\backuphandle.txt" -Retries 3
```

This example starts a Phase 1 backup of the search index for the default search application, and stores the backup at the location \\\\backuphost\backupfolder. 
The cmdlet stores a handle file backuphandle.txt that is used by the second phase cmdlet.

### ------------------EXAMPLE 2------------------ (SharePoint Server 2013)
```
$ssa = Get-SPEnterpriseSearchServiceApplicationBackup-SPEnterpriseSearchServiceApplicationIndex -Phase 1 $ssa -BackupFolder "\\backuphost\backupfolder" -BackupHandleFile "\\backuphost\backupfolder\backuphandle.txt" -Retries 3
```

This example checks the backup status and progress by re-running the cmdlet for Phase 1.

### ------------------EXAMPLE 2------------------ (SharePoint Server 2016)
```
C:\PS>$ssa = Get-SPEnterpriseSearchServiceApplication
Backup-SPEnterpriseSearchServiceApplicationIndex -Phase 1 $ssa -BackupFolder "\\backuphost\backupfolder" -BackupHandleFile "\\backuphost\backupfolder\backuphandle.txt" -Retries 3
```

This example checks the backup status and progress by re-running the cmdlet for Phase 1.

### ------------------EXAMPLE 3------------------ (SharePoint Server 2013)
```
$ssa = Get-SPEnterpriseSearchServiceApplicationBackup-SPEnterpriseSearchServiceApplicationIndex -Phase 2 -SearchApplication $ssa -BackupFolder "\\backuphost\backupfolder" -BackupHandleFile "\\backuphost\backupfolder\backuphandle.txt" -Retries 3
```

This example starts the Phase 2 of the search index backup by using the same backup location and backup handle file as used for Phase 1.
The Search Service Application must be paused before the second phase can be started.

### ------------------EXAMPLE 3------------------ (SharePoint Server 2016)
```
C:\PS>$ssa = Get-SPEnterpriseSearchServiceApplication
Backup-SPEnterpriseSearchServiceApplicationIndex -Phase 2 -SearchApplication $ssa -BackupFolder "\\backuphost\backupfolder" -BackupHandleFile "\\backuphost\backupfolder\backuphandle.txt" -Retries 3
```

This example starts the Phase 2 of the search index backup by using the same backup location and backup handle file as used for Phase 1. 
The Search Service Application must be paused before the second phase can be started.

## PARAMETERS

### -Phase
Specifies the phase of the backup job.

```yaml
Type: Int32
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchApplication
Name of the search service application to be backed up

```yaml
Type: SearchServiceApplication
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BackupFolder
Full UNC path of the backup files should be written.

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackupHandleFile
Specifies a file handle for an ongoing backup job.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Retries
Number of times to retry if temporary failure occurs.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
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

### -Abort
{{Fill Abort Description}}

```yaml
Type: SwitchParameter
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -PeerToPeer
{{Fill PeerToPeer Description}}

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

### -SpecifiedBackupHandle
{{Fill SpecifiedBackupHandle Description}}

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

[Online Version](http://technet.microsoft.com/EN-US/library/625bd9f3-d7f5-4d8a-9edf-6cb270ce27b3(Office.15).aspx)

