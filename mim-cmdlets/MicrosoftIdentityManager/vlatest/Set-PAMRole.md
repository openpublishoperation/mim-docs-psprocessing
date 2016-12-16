---
external help file: MIMPAM_Cmdlets.xml
online version: 0baae78c-6bb9-41c5-b0cc-76a85aa90a8a
schema: 2.0.0
ms.assetid: CDAC3378-51F6-468E-8755-3F872C859D9F
updated_at: 12/16/2016 10:24 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/Set-PAMRole.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/Set-PAMRole.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/d76fe71a336b890697ca5b79f29d35c57acf4cc6/mim-cmdlets/MicrosoftIdentityManager/vlatest/Set-PAMRole.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# Set-PAMRole

## SYNOPSIS
Updates a PAM role in the MIM Service.

## SYNTAX

```
Set-PAMRole [-Role] <PAMRole> [[-Candidates] <PAMUser[]>] [[-Privileges] <PAMGroup[]>]
 [[-Approvers] <PAMUser[]>] [[-Session] <PAMSession>] [[-TTL] <TimeSpan]>]
 [[-AvailableFrom] <Nullable [System.DateTime]>] [[-AvailableTo] <Nullable [System.DateTime]>]
 [[-MFAEnabled] <Boolean]>] [[-ApprovalEnabled] <Boolean]>]
 [[-AvailabilityWindowEnabled] <Nullable [System.Boolean]>] [[-DisplayName] <String>] [[-Description] <String>]
```

## DESCRIPTION
The **Set-PAMRole** cmdlet updates a Privileged Access Management (PAM) role in the Microsoft Identity Manager (MIM) Service.

## EXAMPLES

### Example 1: Change an attribute of the role
```
PS C:\>Set-PAMRole -Role (Get-PAMRole -DisplayName "IT") -Description "For IT Use Only"
```

This command changes an attribute of the PAM role in the MIM Service.

### Example 2: Adding a candidate user to a role
```
PS C:\>$Role = Get-PAMRole -DisplayName "IT" ; $NC = $Role.Candidates + (Get-PAMUser -PrivDisplayName "contoso.jen") ; $Role = Set-PAMRole -Role $Role -Candidates $NC
```

This command adds a candidate user to a PAM role in the MIM Service.

## PARAMETERS

### -ApprovalEnabled
Specifies, if true, activation requests to this role will require approval by a role owner.

```yaml
Type: Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
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
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AvailabilityWindowEnabled
Indicates whether the role can only be activated during a specified time interval.

```yaml
Type: Nullable [System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
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
Position: 3
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
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Candidates
Specifies the collection of candidate users which are to be associated with the PAM Role.

```yaml
Type: PAMUser[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
Specifies the description of the PAM role in the MIM Service.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Specifies the value for the DisplayName attribute of the PAM role in the MIM Service.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MFAEnabled
Specifies, if true, that activation requests to this role will require an MFA challenge.

```yaml
Type: Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Privileges
Specifies the collection of groups which are associated with the PAM role.

```yaml
Type: PAMGroup[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Role
Specifies the role to be updated, returned by Get-PAMRole.

```yaml
Type: PAMRole
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Session
Specifies the session with the PAM domain and MIM Service.

```yaml
Type: PAMSession
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TTL
Specifies the default time to live (TTL) in seconds of group memberships assigned to users through this role.

```yaml
Type: TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
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

[New-PAMRole](xref:MicrosoftIdentityManager/vlatest/New-PAMRole.md)

[Remove-PAMRole](xref:MicrosoftIdentityManager/vlatest/Remove-PAMRole.md)

[Microsoft Identity Manager (xref:MicrosoftIdentityManager/vlatest/MIMPAM.md)

