---
external help file: MIMPAM_Cmdlets.xml
online version: 0baae78c-6bb9-41c5-b0cc-76a85aa90a8a
schema: 2.0.0
ms.assetid: 0332854C-EB3A-4EA8-BFEC-A72618778663
updated_at: 12/16/2016 10:24 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/New-PAMRole.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/New-PAMRole.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/d76fe71a336b890697ca5b79f29d35c57acf4cc6/mim-cmdlets/MicrosoftIdentityManager/vlatest/New-PAMRole.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# New-PAMRole

## SYNOPSIS
Creates a PAM role in the MIM Service.

## SYNTAX

```
New-PAMRole [-DisplayName] <String> [-AvailabilityWindowEnabled] [[-Description] <String>]
 [[-Session] <PAMSession>] [[-Privileges] <PAMGroup[]>] [[-Approvers] <PAMUser[]>] [[-Candidates] <PAMUser[]>]
 [[-TTL] <TimeSpan]>] [[-AvailableFrom] <Nullable [System.DateTime]>]
 [[-AvailableTo] <Nullable [System.DateTime]>] [-MFAEnabled] [-ApprovalEnabled]
```

## DESCRIPTION
The **New-PAMRole** cmdlet creates a Privileged Access Management (PAM) role in the Microsoft Identity Manager (MIM) Service.
This cmdlet assigns one or more candidate users with one or more security groups (privileges), to permit a candidate user assigned to the role to subsequently request to activate. 
The *ApprovalEnabled* and *MFAEnabled* parameters control the authorization gates for an activation request. 
The *Owners* parameter specifies users which can approve activation requests. 
The *TTL* (time to live) parameter specifies the default time to live for memberships in the groups for activation requests through this role.

## EXAMPLES

### Example 1: Create a new PAM role in the MIM Service with a specified time to live
```
PS C:\>New-PAMRole -DisplayName "CorpAdmins" -TTL 600 -Privileges $PG -Candidates $SJ
```

This command creates a new PAM Role in the MIM Service, with a Time to Live of 600 seconds. 
The variable $PG is a list of groups from an earlier call to New-PAMGroup or Get-PAMGroup, and the variable $SJ is a list of PAM Users from an earlier call to New-PAMUser or Get-PAMUser.

## PARAMETERS

### -ApprovalEnabled
Indicates that activation requests to this role will require approval by a role owner.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Approvers


```yaml
Type: PAMUser[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AvailabilityWindowEnabled
Indicates the role can only be activated during a specified time interval

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AvailableFrom
Indicates the earliest time of day that a request will be activated. 
Only the time portion of the parameter is used.

```yaml
Type: Nullable [System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AvailableTo
Indicates the latest time of day that a request will be activated. 
Only the time portion of the parameter is used.

```yaml
Type: Nullable [System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Candidates
Specifies the collection of candidate users which are to be associated with and can activate into the PAM role.

```yaml
Type: PAMUser[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
Specifies the description of the new PAM role in the MIM Service.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Specifies the name of the new PAM role in the MIM Service.

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

### -MFAEnabled
Indicates that activation requests to this role will require an MFA challenge.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Privileges
Specifies the collection of groups which are to be associated with the PAM role.

```yaml
Type: PAMGroup[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Session
Specifies the session with the PAM domain and MIM Service.

```yaml
Type: PAMSession
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TTL
Specifies the default time to live in seconds of group memberships assigned to users through this role.
The minimum recommended time is 5 minutes.

```yaml
Type: TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMRole

## NOTES

## RELATED LINKS

[Get-PAMRole](xref:MicrosoftIdentityManager/vlatest/Get-PAMRole.md)

[Remove-PAMRole](xref:MicrosoftIdentityManager/vlatest/Remove-PAMRole.md)

[Set-PAMRole](xref:MicrosoftIdentityManager/vlatest/Set-PAMRole.md)

[Get-PAMGroup](xref:MicrosoftIdentityManager/vlatest/Get-PAMGroup.md)

[New-PAMGroup](xref:MicrosoftIdentityManager/vlatest/New-PAMGroup.md)

[Get-PAMUser](xref:MicrosoftIdentityManager/vlatest/Get-PAMUser.md)

[New-PAMUser](xref:MicrosoftIdentityManager/vlatest/New-PAMUser.md)

[Microsoft Identity Manager (xref:MicrosoftIdentityManager/vlatest/MIMPAM.md)

