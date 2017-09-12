---
external help file: sharepoint.xml
online version: 
schema: 2.0.0
---

# Test-SPProjectServiceApplication

## SYNOPSIS
{{Fill in the Synopsis}}

## SYNTAX

```
Test-SPProjectServiceApplication [-Identity] <PsiServiceApplicationPipeBind>
 [[-Rule] <ProjectServiceApplicationHealthRuleName>] [-AssignmentCollection <SPAssignmentCollection>]
```

## DESCRIPTION
{{Fill in the Description}}

## EXAMPLES

### Example 1 (SharePoint Server 2016)
```
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -AssignmentCollection
{{Fill AssignmentCollection Description}}

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

### -Identity
{{Fill Identity Description}}

```yaml
Type: PsiServiceApplicationPipeBind
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Rule
{{Fill Rule Description}}

```yaml
Type: ProjectServiceApplicationHealthRuleName
Parameter Sets: (All)
Aliases: 
Accepted values: All, QueueServiceInternalState, QueueInFlightJobs, CalcServiceWorkerState, DatabasePermissions

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

## INPUTS

### Microsoft.Office.Project.Server.Cmdlet.PsiServiceApplicationPipeBind
Microsoft.Office.Project.Server.HealthRules.ProjectServiceApplicationHealthRuleName Microsoft.SharePoint.PowerShell.SPAssignmentCollection

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

