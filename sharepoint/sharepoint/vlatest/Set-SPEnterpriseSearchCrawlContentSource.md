---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/7d803d1c-0b1d-4205-acdb-75d2878b6cfe(Office.15).aspx
schema: 2.0.0
---

# Set-SPEnterpriseSearchCrawlContentSource

## SYNOPSIS
Below Content Applies To: SharePoint Server 2013

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Set-SPEnterpriseSearchCrawlContentSource [-Identity] <ContentSourcePipeBind>
 [-AssignmentCollection <SPAssignmentCollection>]
 [-BDCApplicationProxyGroup <SPServiceApplicationProxyGroupPipeBind>] [-Confirm]
 [-CrawlPriority <CrawlPriority>] [-CrawlScheduleDaysOfMonth <Int32>]
 [-CrawlScheduleMonthsOfYear <MonthsOfYear>] [-CrawlScheduleRepeatDuration <Int32>]
 [-CrawlScheduleRepeatInterval <Int32>] [-CrawlScheduleStartDateTime <DateTime>] [-CustomProtocol <String>]
 [-EnableContinuousCrawls <Boolean>] [-LOBSystemSet <String[]>] [-MaxPageEnumerationDepth <Int32>]
 [-MaxSiteEnumerationDepth <Int32>] [-MonthlyCrawlSchedule] [-Name <String>]
 [-ScheduleType <ContentSourceCrawlScheduleType>] [-SearchApplication <SearchServiceApplicationPipeBind>]
 [-StartAddresses <String>] [-Tag <String>] [-WhatIf]
```

### UNNAMED_PARAMETER_SET_2
```
Set-SPEnterpriseSearchCrawlContentSource [-Identity] <ContentSourcePipeBind>
 [-AssignmentCollection <SPAssignmentCollection>]
 [-BDCApplicationProxyGroup <SPServiceApplicationProxyGroupPipeBind>] [-Confirm]
 [-CrawlPriority <CrawlPriority>] [-CrawlScheduleDaysOfWeek <DaysOfWeek>]
 [-CrawlScheduleRepeatDuration <Int32>] [-CrawlScheduleRepeatInterval <Int32>]
 [-CrawlScheduleRunEveryInterval <Int32>] [-CrawlScheduleStartDateTime <DateTime>] [-CustomProtocol <String>]
 [-EnableContinuousCrawls <Boolean>] [-LOBSystemSet <String[]>] [-MaxPageEnumerationDepth <Int32>]
 [-MaxSiteEnumerationDepth <Int32>] [-Name <String>] [-ScheduleType <ContentSourceCrawlScheduleType>]
 [-SearchApplication <SearchServiceApplicationPipeBind>] [-StartAddresses <String>] [-Tag <String>]
 [-WeeklyCrawlSchedule] [-WhatIf]
```

### UNNAMED_PARAMETER_SET_3
```
Set-SPEnterpriseSearchCrawlContentSource [-Identity] <ContentSourcePipeBind>
 [-AssignmentCollection <SPAssignmentCollection>]
 [-BDCApplicationProxyGroup <SPServiceApplicationProxyGroupPipeBind>] [-Confirm]
 [-CrawlPriority <CrawlPriority>] [-CrawlScheduleRepeatDuration <Int32>] [-CrawlScheduleRepeatInterval <Int32>]
 [-CrawlScheduleRunEveryInterval <Int32>] [-CrawlScheduleStartDateTime <DateTime>] [-CustomProtocol <String>]
 [-DailyCrawlSchedule] [-EnableContinuousCrawls <Boolean>] [-LOBSystemSet <String[]>]
 [-MaxPageEnumerationDepth <Int32>] [-MaxSiteEnumerationDepth <Int32>] [-Name <String>]
 -ScheduleType <ContentSourceCrawlScheduleType> [-SearchApplication <SearchServiceApplicationPipeBind>]
 [-StartAddresses <String>] [-Tag <String>] [-WhatIf]
```

### UNNAMED_PARAMETER_SET_4
```
Set-SPEnterpriseSearchCrawlContentSource [-Identity] <ContentSourcePipeBind>
 [-AssignmentCollection <SPAssignmentCollection>]
 [-BDCApplicationProxyGroup <SPServiceApplicationProxyGroupPipeBind>] [-Confirm]
 [-CrawlPriority <CrawlPriority>] [-CustomProtocol <String>] [-EnableContinuousCrawls <Boolean>]
 [-LOBSystemSet <String[]>] [-MaxPageEnumerationDepth <Int32>] [-MaxSiteEnumerationDepth <Int32>]
 [-Name <String>] [-RemoveCrawlSchedule] [-ScheduleType <ContentSourceCrawlScheduleType>]
 [-SearchApplication <SearchServiceApplicationPipeBind>] [-StartAddresses <String>] [-Tag <String>] [-WhatIf]
```

## DESCRIPTION
Below Content Applies To: SharePoint Server 2013

{{Fill in the Description}} Below Content Applies To: SharePoint Server 2016

This cmdlet contains more than one parameter set.
You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see Cmdlet Parameter Sets (http://go.microsoft.com/fwlink/?LinkID=187810).

The Set-SPEnterpriseSearchCrawlContentSource cmdlet updates the rules of a crawl content source when the search functionality is initially configured and after any new content source is added.
This cmdlet is called once to set the incremental crawl schedule for a content source, and it is called again to set a full crawl schedule.

The value of the optional EnableContinuousCrawls parameter can be True or False.
A value of True enables continuous crawls of items in this content source.
This causes the search system to automatically start incremental crawls to process the latest changes to items in the corresponding data repositories.
This helps to keep the index fresh for items in this content source.
Search service application administrators can still configure full crawls as needed.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### Example 1 (SharePoint Server 2013)
```
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

### ------------------EXAMPLE------------------ (SharePoint Server 2016)
```
C:\PS>$searchapp = Get-SPEnterpriseSearchServiceApplication "SearchApp1"
$cs = Get-SPEnterpriseSearchCrawlContentSource -SearchApplication $searchapp ""
$cs | Set-SPEnterpriseSearchCrawlContentSource -ScheduleType Full -DailyCrawlSchedule -CrawlScheduleRunEveryInterval 30
$cs | Set-SPEnterpriseSearchCrawlContentSource -ScheduleType Incremental -DailyCrawlSchedule -CrawlScheduleRepeatInterval 60 -CrawlScheduleRepeatDuration 1440
```

This example returns an existing content source ExampleContentSource1, and creates a schedule to run a full crawl every 30 days and an incremental crawl every hour every day.

## PARAMETERS

### -AssignmentCollection
Below Content Applies To: SharePoint Server 2013

{{Fill AssignmentCollection Description}} Below Content Applies To: SharePoint Server 2016

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

### -BDCApplicationProxyGroup
Below Content Applies To: SharePoint Server 2013

{{Fill BDCApplicationProxyGroup Description}} Below Content Applies To: SharePoint Server 2016

Specifies the proxy to use for a business type content source.
This proxy group must contain a default Business Data Connectivity Metadata Store proxy.

```yaml
Type: SPServiceApplicationProxyGroupPipeBind
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Below Content Applies To: SharePoint Server 2013

Prompts you for confirmation before running the cmdlet.
Below Content Applies To: SharePoint Server 2016

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

### -CrawlPriority
Below Content Applies To: SharePoint Server 2013

{{Fill CrawlPriority Description}} Below Content Applies To: SharePoint Server 2016

Specifies the priority of this content source.

The type must be one of the following integers: 1= Normal, 2=High.

```yaml
Type: CrawlPriority
Parameter Sets: (All)
Aliases: p
Accepted values: Normal, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CrawlScheduleDaysOfMonth
Below Content Applies To: SharePoint Server 2013

{{Fill CrawlScheduleDaysOfMonth Description}} Below Content Applies To: SharePoint Server 2016

Specifies the days on which to crawl when the MonthlyCrawlSchedule parameter is set.

```yaml
Type: Int32
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CrawlScheduleDaysOfWeek
Below Content Applies To: SharePoint Server 2013

{{Fill CrawlScheduleDaysOfWeek Description}} Below Content Applies To: SharePoint Server 2016

Specifies the days on which to crawl when the WeeklyCrawlSchedule parameter is set.

```yaml
Type: DaysOfWeek
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Weekdays, Saturday, Weekends, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CrawlScheduleMonthsOfYear
Below Content Applies To: SharePoint Server 2013

{{Fill CrawlScheduleMonthsOfYear Description}} Below Content Applies To: SharePoint Server 2016

Specifies the months on which to crawl when the MonthlyCrawlSchedule parameter is set.

```yaml
Type: MonthsOfYear
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: month
Accepted values: January, February, March, April, May, June, July, August, September, October, November, December, AllMonths

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CrawlScheduleRepeatDuration
Below Content Applies To: SharePoint Server 2013

{{Fill CrawlScheduleRepeatDuration Description}} Below Content Applies To: SharePoint Server 2016

Specifies the number of times to repeat the crawl schedule.

```yaml
Type: Int32
Parameter Sets: UNNAMED_PARAMETER_SET_1, UNNAMED_PARAMETER_SET_2, UNNAMED_PARAMETER_SET_3
Aliases: duration

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CrawlScheduleRepeatInterval
Below Content Applies To: SharePoint Server 2013

{{Fill CrawlScheduleRepeatInterval Description}} Below Content Applies To: SharePoint Server 2016

Specifies the number of minutes between each repeat interval for the crawl schedule

```yaml
Type: Int32
Parameter Sets: UNNAMED_PARAMETER_SET_1, UNNAMED_PARAMETER_SET_2, UNNAMED_PARAMETER_SET_3
Aliases: interval

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CrawlScheduleRunEveryInterval
Below Content Applies To: SharePoint Server 2013

{{Fill CrawlScheduleRunEveryInterval Description}} Below Content Applies To: SharePoint Server 2016

Specifies the interval between crawls.

When the DailyCrawlSchedule parameter is set, specifies the number of days between crawls.

When the WeeklyCrawlSchedule parameter is set, specifies the number of weeks between crawls.

```yaml
Type: Int32
Parameter Sets: UNNAMED_PARAMETER_SET_2, UNNAMED_PARAMETER_SET_3
Aliases: every

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CrawlScheduleStartDateTime
Below Content Applies To: SharePoint Server 2013

{{Fill CrawlScheduleStartDateTime Description}} Below Content Applies To: SharePoint Server 2016

Specifies the initial date of the crawl.
The default value is midnight on the current day.

```yaml
Type: DateTime
Parameter Sets: UNNAMED_PARAMETER_SET_1, UNNAMED_PARAMETER_SET_2, UNNAMED_PARAMETER_SET_3
Aliases: start

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomProtocol
Below Content Applies To: SharePoint Server 2013

{{Fill CustomProtocol Description}} Below Content Applies To: SharePoint Server 2016

Specifies the custom protocol, handled by the custom connector, to use for this content source.

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

### -DailyCrawlSchedule
Below Content Applies To: SharePoint Server 2013

{{Fill DailyCrawlSchedule Description}} Below Content Applies To: SharePoint Server 2016

Base schedule on days between crawls.

```yaml
Type: SwitchParameter
Parameter Sets: UNNAMED_PARAMETER_SET_3
Aliases: daily

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableContinuousCrawls
Below Content Applies To: SharePoint Server 2013

{{Fill EnableContinuousCrawls Description}} Below Content Applies To: SharePoint Server 2016

Specifies the value of the EnableContinuousCrawls parameter: True or False.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity
Below Content Applies To: SharePoint Server 2013

{{Fill Identity Description}} Below Content Applies To: SharePoint Server 2016

Specifies the crawl content source to update.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a ContentSource object (for example, ContentSource1); or an instance of a valid ContentSource object.

```yaml
Type: ContentSourcePipeBind
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LOBSystemSet
Below Content Applies To: SharePoint Server 2013

{{Fill LOBSystemSet Description}} Below Content Applies To: SharePoint Server 2016

Specifies a comma-separated list of Business Data Connectivity Metadata Store system names and system instance names for a business type content source.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPageEnumerationDepth
Below Content Applies To: SharePoint Server 2013

{{Fill MaxPageEnumerationDepth Description}} Below Content Applies To: SharePoint Server 2016

Specifies, for a web or custom type content source, the number of page hops that the crawler can make from the start address to a content item.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxSiteEnumerationDepth
Below Content Applies To: SharePoint Server 2013

{{Fill MaxSiteEnumerationDepth Description}} Below Content Applies To: SharePoint Server 2016

Specifies, for a web or custom type content source, the number of site hops that the crawler can take from the start address to a content item.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonthlyCrawlSchedule
Below Content Applies To: SharePoint Server 2013

{{Fill MonthlyCrawlSchedule Description}} Below Content Applies To: SharePoint Server 2016

Base the schedule on months between crawls.

```yaml
Type: SwitchParameter
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: monthly

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Below Content Applies To: SharePoint Server 2013

{{Fill Name Description}} Below Content Applies To: SharePoint Server 2016

Specifies the new display name for the content source.

The type must be a valid name of a content source; for example, ContentSource1.

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveCrawlSchedule
Below Content Applies To: SharePoint Server 2013

{{Fill RemoveCrawlSchedule Description}} Below Content Applies To: SharePoint Server 2016

Deletes the specified crawl.

```yaml
Type: SwitchParameter
Parameter Sets: UNNAMED_PARAMETER_SET_4
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScheduleType
Below Content Applies To: SharePoint Server 2013

{{Fill ScheduleType Description}} Below Content Applies To: SharePoint Server 2016

Specifies the type of crawl schedule.

The type must be one of the following values: Full or Incremental.

```yaml
Type: ContentSourceCrawlScheduleType
Parameter Sets: UNNAMED_PARAMETER_SET_1, UNNAMED_PARAMETER_SET_2, UNNAMED_PARAMETER_SET_4
Aliases: 
Accepted values: Full, Incremental, Full, Incremental, Full, Incremental, Full, Incremental

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ContentSourceCrawlScheduleType
Parameter Sets: UNNAMED_PARAMETER_SET_3
Aliases: 
Accepted values: Full, Incremental, Full, Incremental, Full, Incremental, Full, Incremental

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchApplication
Below Content Applies To: SharePoint Server 2013

{{Fill SearchApplication Description}} Below Content Applies To: SharePoint Server 2016

Specifies the search application that contains the content source.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid SearchServiceApplication object.

```yaml
Type: SearchServiceApplicationPipeBind
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartAddresses
Below Content Applies To: SharePoint Server 2013

{{Fill StartAddresses Description}} Below Content Applies To: SharePoint Server 2016

Specifies the comma-separated list of URLs at which to start a crawl for this content source.

The type must be a valid URL, in the form http://server_name.

```yaml
Type: String
Parameter Sets: (All)
Aliases: s

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Below Content Applies To: SharePoint Server 2013

{{Fill Tag Description}} Below Content Applies To: SharePoint Server 2016

Specifies the URL for the page to modify the settings for a custom content source.
The string that specifies the URL can contain a maximum of 1,024 characters.

The type must be a valid URL, in the form http://server_name.

```yaml
Type: String
Parameter Sets: (All)
Aliases: t

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WeeklyCrawlSchedule
Below Content Applies To: SharePoint Server 2013

{{Fill WeeklyCrawlSchedule Description}} Below Content Applies To: SharePoint Server 2016

Base the schedule on weeks between crawls.

```yaml
Type: SwitchParameter
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: weekly

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Below Content Applies To: SharePoint Server 2013

Shows what would happen if the cmdlet runs.
The cmdlet is not run.
Below Content Applies To: SharePoint Server 2016

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

### Microsoft.Office.Server.Search.Cmdlet.ContentSourcePipeBind
Microsoft.SharePoint.PowerShell.SPAssignmentCollection

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

