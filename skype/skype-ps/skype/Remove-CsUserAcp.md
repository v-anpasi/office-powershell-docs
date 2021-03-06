---
external help file: 
applicable: Lync Server 2010, Lync Server 2013, Skype for Business Online, Skype for Business Server 2015
schema: 2.0.0
---

# Remove-CsUserAcp

## SYNOPSIS
**Below Content Applies To:** Lync Server 2010

Removes one or more audio conferencing providers assigned to a user or group of users.

**Below Content Applies To:** Lync Server 2013, Skype for Business Server 2015

Removes one or more audio conferencing providers assigned to a user or group of users.
This cmdlet was introduced in Lync Server 2010.

**Below Content Applies To:** Skype for Business Online

Remove-CsUserAcp \[-Identity\] \<UserIdParameter\> \[-TollNumber \<string\>\] \[-ParticipantPasscode \<string\>\] \[-Name \<string\>\] \[-PassThru\] \[-WhatIf\] \[-Confirm\] \[\<CommonParameters\>\]



## SYNTAX

```
Remove-CsUserAcp [-Identity] <UserIdParameter> [-Name <String>] [-TollNumber <String>] [-PassThru] [-WhatIf]
 [-Confirm] [-ParticipantPasscode <String>] [-AsJob] [<CommonParameters>]
```

## DESCRIPTION
**Below Content Applies To:** Lync Server 2010

An audio conferencing provider is a third-party company that provides organizations with conferencing services.
Among other things, audio conferencing providers provide a way for users located off site, and not connected to the corporate network or the Internet, to participate in the audio portion of a conference or meeting.
Audio conferencing providers often provide high-end services such as live translation, transcription, and live per-conference operator assistance.

Microsoft Lync Server 2010 does not allow for complete integration with audio conferencing providers.
The CsUserAcp cmdlets do enable administrators to set a phone number and passcode, and to configure other information that can be used for audio conferencing provider integration any time a user schedules a meeting.
However, because these cmdlets were not designed for the on-premises version of Lync Server (instead, they are primarily intended for use with Microsoft Lync Online 2010) no additional audio conferencing provider integration is provided beyond assigning property values.

Any audio conferencing provider assigned to a user can later be removed by using the Remove-CsUserAcp cmdlet.
Calling Remove-CsUserAcp without any parameters (other than the Identity parameter, which indicates the user account to be modified) removes all the audio conferencing providers assigned to a user.
Alternatively, you can use the optional parameters included with Remove-CsUserAcp to remove selected providers from a user account.
For example, this command finds the Ken Myer user account and removes all the audio conferencing providers that have a Name equal to "Fabrikam ACP":

Remove-CsUserAcp -Identity "Ken Myer" -Name "Fabrikam ACP"

To provide finer-grained removal of audio conferencing providers, simply include additional parameters.
For example this command removes any audio conferencing providers that have the Name "Fabrikam ACP" and also have a TollNumber equal to "14255551298" as follows:

Remove-CsUserAcp -Identity "Ken Myer" -Name "Fabrikam ACP" -TollNumber "14255551298"

Who can run this cmdlet: By default, members of the following groups are authorized to run the Remove-CsUserAcp cmdlet locally: RTCUniversalUserAdmins.
To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself) run the following command from the Windows PowerShell prompt:

Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Remove-CsUserAcp"}

**Below Content Applies To:** Lync Server 2013

An audio conferencing provider is a third-party company that provides organizations with conferencing services.
Among other things, audio conferencing providers provide a way for users located off site, and not connected to the corporate network or the Internet, to participate in the audio portion of a conference or meeting.
Audio conferencing providers often provide high-end services such as live translation, transcription, and live per-conference operator assistance.

Lync Server does not allow for complete integration with audio conferencing providers.
The CsUserAcp cmdlets do enable administrators to set a phone number and passcode, and to configure other information that can be used for audio conferencing provider integration any time a user schedules a meeting.
However, because these cmdlets were not designed for the on-premises version of Lync Server (instead, they are primarily intended for use with Lync Online) no additional audio conferencing provider integration is provided beyond assigning property values.

Any audio conferencing provider assigned to a user can later be removed by using the Remove-CsUserAcp cmdlet.
Calling Remove-CsUserAcp without any parameters (other than the Identity parameter, which indicates the user account to be modified) removes all the audio conferencing providers assigned to a user.
Alternatively, you can use the optional parameters included with Remove-CsUserAcp to remove selected providers from a user account.
For example, this command finds the Ken Myer user account and removes all the audio conferencing providers that have a Name equal to "Fabrikam ACP":

Remove-CsUserAcp -Identity "Ken Myer" -Name "Fabrikam ACP"

To provide finer-grained removal of audio conferencing providers, simply include additional parameters.
For example this command removes any audio conferencing providers that have the Name "Fabrikam ACP" and also have a TollNumber equal to "14255551298" as follows:

Remove-CsUserAcp -Identity "Ken Myer" -Name "Fabrikam ACP" -TollNumber "14255551298"

Who can run this cmdlet: By default, members of the following groups are authorized to run the Remove-CsUserAcp cmdlet locally: RTCUniversalUserAdmins.
To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself) run the following command from the Windows PowerShell prompt:

Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Remove-CsUserAcp"}

**Below Content Applies To:** Skype for Business Online

{{Fill in the Description}}

**Below Content Applies To:** Skype for Business Server 2015

An audio conferencing provider is a third-party company that provides organizations with conferencing services.
Among other things, audio conferencing providers provide a way for users located off site, and not connected to the corporate network or the Internet, to participate in the audio portion of a conference or meeting.
Audio conferencing providers often provide high-end services such as live translation, transcription, and live per-conference operator assistance.

Skype for Business Server 2015 does not allow for complete integration with audio conferencing providers.
The CsUserAcp cmdlets do enable administrators to set a phone number and passcode, and to configure other information that can be used for audio conferencing provider integration any time a user schedules a meeting.
However, because these cmdlets were not designed for the on-premises version of Skype for Business Server 2015 (instead, they are primarily intended for use with Skype for Business Online) no additional audio conferencing provider integration is provided beyond assigning property values.

Any audio conferencing provider assigned to a user can later be removed by using the Remove-CsUserAcp cmdlet.
Calling the Remove-CsUserAcp cmdlet without any parameters (other than the Identity parameter, which indicates the user account to be modified) removes all the audio conferencing providers assigned to a user.
Alternatively, you can use the optional parameters included with the Remove-CsUserAcp cmdlet to remove selected providers from a user account.
For example, this command finds the Ken Myer user account and removes all the audio conferencing providers that have a Name equal to "Fabrikam ACP":

Remove-CsUserAcp -Identity "Ken Myer" -Name "Fabrikam ACP"

To provide finer-grained removal of audio conferencing providers, simply include additional parameters.
For example this command removes any audio conferencing providers that have the Name "Fabrikam ACP" and also have a TollNumber equal to "14255551298" as follows:

Remove-CsUserAcp -Identity "Ken Myer" -Name "Fabrikam ACP" -TollNumber "14255551298"



## EXAMPLES

### -------------------------- Example 1 ------------------------ (Lync Server 2010)
```
Remove-CsUserAcp -Identity "Ken Myer"
```

The command shown in Example 1 removes all the audio conferencing providers that have been assigned to the user Ken Myer.

### -------------------------- EXAMPLE 1 -------------------------- (Lync Server 2013)
```

```

The command shown in Example 1 removes all the audio conferencing providers that have been assigned to the user Ken Myer.

Remove-CsUserAcp -Identity "Ken Myer"

### Example 1 (Skype for Business Online)
```
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

### -------------------------- EXAMPLE 1 -------------------------- (Skype for Business Server 2015)
```

```

The command shown in Example 1 removes all the audio conferencing providers that have been assigned to the user Ken Myer.

Remove-CsUserAcp -Identity "Ken Myer"

### -------------------------- Example 2 ------------------------ (Lync Server 2010)
```
Get-CsUser | Remove-CsUserAcp
```

Example 2 shows how you can remove all of the audio conferencing providers that have been assigned to all the users enabled for Lync Server 2010.
To do this, the command first uses Get-CsUser to retrieve a collection of all the users who have been enabled for Lync Server.
That collection is then piped to the Remove-CsUserAcp cmdlet, which removes all the audio conferencing providers that have been assigned to each user in the collection.

### -------------------------- EXAMPLE 2 -------------------------- (Lync Server 2013)
```

```

Example 2 shows how you can remove all of the audio conferencing providers that have been assigned to all the users enabled for Lync Server.
To do this, the command first uses Get-CsUser to retrieve a collection of all the users who have been enabled for Lync Server.
That collection is then piped to the Remove-CsUserAcp cmdlet, which removes all the audio conferencing providers that have been assigned to each user in the collection.

Get-CsUser | Remove-CsUserAcp

### -------------------------- EXAMPLE 2 -------------------------- (Skype for Business Server 2015)
```

```

Example 2 shows how you can remove all of the audio conferencing providers that have been assigned to all the users enabled for Skype for Business Server 2015.
To do this, the command first uses the Get-CsUser cmdlet to retrieve a collection of all the users who have been enabled for Skype for Business Server 2015.
That collection is then piped to the Remove-CsUserAcp cmdlet, which removes all the audio conferencing providers that have been assigned to each user in the collection.

Get-CsUser | Remove-CsUserAcp

### -------------------------- Example 3 ------------------------ (Lync Server 2010)
```
Remove-CsUserAcp -Identity "Ken Myer" -Name "Fabrikam ACP"
```

In Example 3, all the audio conferencing providers that have the Name "Fabrikam ACP" are removed from Ken Myer's user account.

### -------------------------- EXAMPLE 3 -------------------------- (Lync Server 2013)
```

```

In Example 3, all the audio conferencing providers that have the Name "Fabrikam ACP" are removed from Ken Myer's user account.

Remove-CsUserAcp -Identity "Ken Myer" -Name "Fabrikam ACP"

### -------------------------- EXAMPLE 3 -------------------------- (Skype for Business Server 2015)
```

```

In Example 3, all the audio conferencing providers that have the Name "Fabrikam ACP" are removed from Ken Myer's user account.

Remove-CsUserAcp -Identity "Ken Myer" -Name "Fabrikam ACP"

### -------------------------- Example 4 ------------------------ (Lync Server 2010)
```
Get-CsUserAcp | Where-Object {$_.AcpInfo -match "14255551298"} | Remove-CsUserAcp
```

The preceding command removes the audio conferencing provider that has the toll number "14255551298" from all the user accounts that have been assigned an audio conferencing provider.
To carry out this task, the command first uses Get-CsUserAcp to return information about all the audio conferencing providers assigned to all your users.
This information is then piped to the Where-Object cmdlet, which selects only those accounts where the AcpInfo property includes (-match) the telephone number "14255551298".
This filtered collection is then piped to the Remove-CsUserAcp cmdlet, which removes the corresponding audio conferencing provider from each account in the filtered collection.

### -------------------------- EXAMPLE 4 -------------------------- (Lync Server 2013)
```

```

Example 4 removes the audio conferencing provider that has the toll number "14255551298" from all the user accounts that have been assigned an audio conferencing provider.
To carry out this task, the command first uses Get-CsUserAcp to return information about all the audio conferencing providers assigned to all your users.
This information is then piped to the Where-Object cmdlet, which selects only those accounts where the AcpInfo property includes (-match) the telephone number "14255551298".
This filtered collection is then piped to the Remove-CsUserAcp cmdlet, which removes the corresponding audio conferencing provider from each account in the filtered collection.

Get-CsUserAcp | Where-Object {$_.AcpInfo -match "14255551298"} | Remove-CsUserAcp

### -------------------------- EXAMPLE 4 -------------------------- (Skype for Business Server 2015)
```

```

Example 4 removes the audio conferencing provider that has the toll number "14255551298" from all the user accounts that have been assigned an audio conferencing provider.
To carry out this task, the command first uses the Get-CsUserAcp cmdlet to return information about all the audio conferencing providers assigned to all your users.
This information is then piped to the Where-Object cmdlet, which selects only those accounts where the AcpInfo property includes (-match) the telephone number "14255551298".
This filtered collection is then piped to the Remove-CsUserAcp cmdlet, which removes the corresponding audio conferencing provider from each account in the filtered collection.

Get-CsUserAcp | Where-Object {$_.AcpInfo -match "14255551298"} | Remove-CsUserAcp

## PARAMETERS

### -Identity
**Below Content Applies To:** Lync Server 2010

Indicates the Identity of the user account from which the audio conferencing provider is to be removed.
You can specify a user's identity using one of four formats: 1) the user's SIP address; 2) the user's user principal name (UPN); 3) the user's domain name and logon name, in the form domain\logon (for example, litwareinc\kenmyer); and, 4) the user's  Active Directory Domain Services (AD DS) display name (for example, Ken Myer).
User Identities can also be reference by using the user's Active Directory distinguished name.

You can use the asterisk (*) wildcard character when using the Display Name as the user Identity.
For example, the Identity "* Smith" returns all the users with a display name that ends with the string value " Smith".



**Below Content Applies To:** Lync Server 2013

Indicates the Identity of the user account from which the audio conferencing provider is to be removed.
You can specify a user's identity using one of four formats: 1) the user's SIP address; 2) the user's user principal name (UPN); 3) the user's domain name and logon name, in the form domain\logon (for example, litwareinc\kenmyer); and, 4) the user's Active Directory Domain Services (AD DS) display name (for example, Ken Myer).
User Identities can also be reference by using the user's Active Directory distinguished name.

You can use the asterisk (*) wildcard character when using the Display Name as the user Identity.
For example, the Identity "* Smith" returns all the users with a display name that ends with the string value " Smith".



**Below Content Applies To:** Skype for Business Online

{{Fill Identity Description}}



**Below Content Applies To:** Skype for Business Server 2015

Indicates the Identity of the user account from which the audio conferencing provider is to be removed.
You can specify a user's identity using one of four formats: 1) the user's SIP address; 2) the user's user principal name (UPN); 3) the user's domain name and logon name, in the form domain\logon (for example, litwareinc\kenmyer); and, 4) the user's Active Directory Domain Services display name (for example, Ken Myer).
User Identities can also be reference by using the user's Active Directory distinguished name.

You can use the asterisk (*) wildcard character when using the Display Name as the user Identity.
For example, the Identity "* Smith" returns all the users with a display name that ends with the string value " Smith".



```yaml
Type: UserIdParameter
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2010, Lync Server 2013, Skype for Business Online, Skype for Business Server 2015

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Name
**Below Content Applies To:** Lync Server 2010, Lync Server 2013

Name of the audio conferencing provider.
For example: -Name "Fabrikam Conference Services".



**Below Content Applies To:** Skype for Business Online

{{Fill Name Description}}



**Below Content Applies To:** Skype for Business Server 2015

Name of the audio conferencing provider.
For example:

-Name "Fabrikam Conference Services"



```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2010, Lync Server 2013, Skype for Business Online, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TollNumber
**Below Content Applies To:** Lync Server 2010, Lync Server 2013

Non-toll-free phone number used for audio conferences.
For example: -TollNumber "14255551298".



**Below Content Applies To:** Skype for Business Online

{{Fill TollNumber Description}}



**Below Content Applies To:** Skype for Business Server 2015

Non-toll-free phone number used for audio conferences.
For example:

-TollNumber "14255551298"



```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2010, Lync Server 2013, Skype for Business Online, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
**Below Content Applies To:** Lync Server 2010, Lync Server 2013, Skype for Business Server 2015

Enables you to pass a user object through the pipeline that represents the user who is having the audio conferencing provider removed.
By default, the Remove-CsUserAcp cmdlet does not pass objects through the pipeline.



**Below Content Applies To:** Skype for Business Online

{{Fill PassThru Description}}



```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2010, Lync Server 2013, Skype for Business Online, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
**Below Content Applies To:** Lync Server 2010, Lync Server 2013, Skype for Business Server 2015

Describes what would happen if you executed the command without actually executing the command.



**Below Content Applies To:** Skype for Business Online

Shows what would happen if the cmdlet runs.
The cmdlet is not run.



```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi
Applicable: Lync Server 2010, Lync Server 2013, Skype for Business Online, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
**Below Content Applies To:** Lync Server 2010, Lync Server 2013, Skype for Business Server 2015

Prompts you for confirmation before executing the command.



**Below Content Applies To:** Skype for Business Online

Prompts you for confirmation before running the cmdlet.



```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf
Applicable: Lync Server 2010, Lync Server 2013, Skype for Business Online, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParticipantPasscode
**Below Content Applies To:** Lync Server 2010, Lync Server 2013

Passcode required when connecting to a conference by using the audio conferencing provider.
For example: -PassCode "0712".



**Below Content Applies To:** Skype for Business Online

{{Fill ParticipantPasscode Description}}



**Below Content Applies To:** Skype for Business Server 2015

Passcode required when connecting to a conference by using the audio conferencing provider.
For example:

-PassCode "0712"



```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2010, Lync Server 2013, Skype for Business Online, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
{{Fill AsJob Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 
Applicable: Skype for Business Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

###  
String or Microsoft.Rtc.Management.ADConnect.Schema.ADUser object.
Remove-CsUserAcp accepts a pipelined string value representing the Identity of a user account that has been enabled for Microsoft Lync Server 2010.
The cmdlet also accepts pipelined instances of the Active Directory user object.

###  
String or Microsoft.Rtc.Management.ADConnect.Schema.ADUser object.
Remove-CsUserAcp accepts a pipelined string value representing the Identity of a user account that has been enabled for Lync Server.
The cmdlet also accepts pipelined instances of the Active Directory user object.

### Microsoft.Rtc.Management.AD.UserIdParameter

###  
String or Microsoft.Rtc.Management.ADConnect.Schema.ADUser object.
The Remove-CsUserAcp cmdlet accepts a pipelined string value representing the Identity of a user account that has been enabled for Skype for Business Server 2015.
The cmdlet also accepts pipelined instances of the Active Directory user object.

## OUTPUTS

###  
None.

### System.Object

## NOTES

## RELATED LINKS

[Online Version](http://technet.microsoft.com/EN-US/library/dec450bb-d523-468d-aee4-07fdc3d567c4(OCS.14).aspx)

[Get-CsUserAcp]()

[Set-CsUserAcp]()

[Online Version](http://technet.microsoft.com/EN-US/library/dec450bb-d523-468d-aee4-07fdc3d567c4(OCS.15).aspx)

[Online Version](http://technet.microsoft.com/EN-US/library/dec450bb-d523-468d-aee4-07fdc3d567c4(OCS.16).aspx)

