---
external help file: sharepoint.xml
online version: 
schema: 2.0.0
---

# Upgrade-SPOSite

## SYNOPSIS
Starts the upgrade process on a site collection.

## SYNTAX

```
Upgrade-SPOSite [-Confirm] -Identity <SpoSitePipeBind> [-NoEmail] [-QueueOnly] [-VersionUpgrade] [-WhatIf]
```

## DESCRIPTION
The Upgrade-SPOSite cmdlet activates the upgrade process for the specified SharePoint Online site collection.
This cmdlet can also be used to resume failed upgrades.

When upgrade is initiated, it can either be a build-to-build or version-to-version upgrade.
The default is build-to-build upgrade.
When in version-to-version upgrade, site collection health checks are first run in repair mode to ensure that the site collection can be upgraded successfully.

You must be a SharePoint Online global administrator and a site collection administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251832 (http://go.microsoft.com/fwlink/p/?LinkId=251832).

## EXAMPLES

### (SharePoint Online)
```

```

### (SharePoint Online)
```

```

## PARAMETERS

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

### -Identity
{{Fill Identity Description}}

```yaml
Type: SpoSitePipeBind
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NoEmail
{{Fill NoEmail Description}}

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

### -QueueOnly
{{Fill QueueOnly Description}}

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

### -VersionUpgrade
{{Fill VersionUpgrade Description}}

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

[Introduction to the SharePoint Online management shell]()

[Set up the SharePoint Online Management Shell Windows PowerShell environment]()

[Request-SPOUpgradeEvaluationSite]()

[New-SPOSite]()

[Online Version](http://technet.microsoft.com/EN-US/library/e45078d4-2933-4001-a27b-aff9e6b1eb9d(Office.15).aspx)

