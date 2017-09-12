---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/0aff3f02-ef56-4ac3-8a32-254f3d6365e3(Office.15).aspx
schema: 2.0.0
---

# Get-SPEnterpriseSearchMetadataCrawledProperty

## SYNOPSIS
Returns a crawled property.

## SYNTAX

```
Get-SPEnterpriseSearchMetadataCrawledProperty [-AssignmentCollection <SPAssignmentCollection>]
 [-Category <CategoryPipeBind>] [-Limit <String>] [-Name <String>] [-PropSet <Guid>]
 -SearchApplication <SearchServiceApplicationPipeBind> [-SiteCollection <Guid>] [-Tenant <Guid>]
 [-VariantType <Int32>]
```

## DESCRIPTION
This cmdlet reads a CrawledProperty object for a crawled property that was created or updated.
You should run this cmdlet when the search functionality is configured for the first time, and after new crawled properties are discovered during a crawl.
If the Name parameter is not specified, this cmdlet returns all crawled properties for the specified category for the specified search application.
If neither the Name nor the Category parameter is specified, this cmdlet returns all crawled properties for the specified search application.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### ------------------EXAMPLE------------------ (SharePoint Server 2013)
```
$searchapp = Get-SPEnterpriseSearchServiceApplication

$cat = Get-SPEnterpriseSearchMetadataCategory -SearchApplication $searchapp -Identity People


Get-SPEnterpriseSearchMetadataCrawledProperty -SearchApplication $searchapp -Category $cat -Limit 1
```

This example returns the first crawled property in the PeopleSearch_Scope metadata category for the default search service application.

### ------------------EXAMPLE------------------ (SharePoint Server 2016)
```
C:\PS>$searchapp = Get-SPEnterpriseSearchServiceApplication
$cat = Get-SPEnterpriseSearchMetadataCategory -SearchApplication $searchapp -Identity People
Get-SPEnterpriseSearchMetadataCrawledProperty -SearchApplication $searchapp -Category $cat -Limit 1
```

This example returns the first crawled property in the PeopleSearch_Scope metadata category for the default search service application.

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

### -Category
Below Content Applies To: SharePoint Server 2013

{{Fill Category Description}} Below Content Applies To: SharePoint Server 2016

Specifies the metadata category of the crawled property to return.

The type must be a valid GUID in the form 12345678-90ab-cdef-1234-567890bcdefgh, a valid name of a metadata category, for example, MetadataCategory1, or an instance of a valid Category object.

```yaml
Type: CategoryPipeBind
Parameter Sets: (All)
Aliases: c

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Limit
Below Content Applies To: SharePoint Server 2013

{{Fill Limit Description}} Below Content Applies To: SharePoint Server 2016

Specifies the maximum number of items to return.
Specify ALL to return all possible results.

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

### -Name
Below Content Applies To: SharePoint Server 2013

{{Fill Name Description}} Below Content Applies To: SharePoint Server 2016

Specifies the crawled property to retrieve.

The type must be a valid crawled property name, for example "urn:schemas-microsoft-com:sharepoint:portal:profile:UserName"

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

### -PropSet
Below Content Applies To: SharePoint Server 2013

{{Fill PropSet Description}} Below Content Applies To: SharePoint Server 2016

Specifies to return crawled properties that use the specified property set.
A property set belongs to one crawled property category.

The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: p

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchApplication
Below Content Applies To: SharePoint Server 2013

{{Fill SearchApplication Description}} Below Content Applies To: SharePoint Server 2016

Specifies the search application that contains the crawled property.

The type must be a valid search application name, for example, SearchApp1, or an instance of a valid SearchServiceApplication object.

```yaml
Type: SearchServiceApplicationPipeBind
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCollection
Below Content Applies To: SharePoint Server 2013

{{Fill SiteCollection Description}} Below Content Applies To: SharePoint Server 2016

Specifies that the crawled properties returned are to be within the scope of a site collection (SPSite).

The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tenant
Below Content Applies To: SharePoint Server 2013

{{Fill Tenant Description}} Below Content Applies To: SharePoint Server 2016

Specifies that the crawled properties returned are to be within the scope of a tenant.

The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VariantType
Below Content Applies To: SharePoint Server 2013

{{Fill VariantType Description}} Below Content Applies To: SharePoint Server 2016

Specifies to return crawled properties that use the specified variant type.

The type must be an integer that specifies the variant data type of the property set.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: vt

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

[Online Version](http://technet.microsoft.com/EN-US/library/0aff3f02-ef56-4ac3-8a32-254f3d6365e3(Office.15).aspx)

