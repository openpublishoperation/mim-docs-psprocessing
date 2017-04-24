---
external help file: Microsoft.IdentityManagement.RequestorPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: D229B024-CB6B-4D9B-9BE8-8FD1C1E5FEBA
updated_at: 4/24/2017 10:54 PM
ms.date: 4/24/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/New-PAMRequest.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/New-PAMRequest.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/3e9264276b5141f0a82bd9905d67bb4900c9c2b3/mim-cmdlets/MIMPAM/vlatest/New-PAMRequest.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# New-PAMRequest

## SYNOPSIS
Creates a PAM activation request in the MIM Service.

## SYNTAX

### Role as PAMRole
```
New-PAMRequest [[-Role] <PAMRoleForRequest>] [[-Justification] <String>] [[-RequestedTTL] <TimeSpan>]
 [-RequestedTime <DateTime>] [<CommonParameters>]
```

### Role as Display Name
```
New-PAMRequest [[-RoleDisplayName] <String>] [[-Justification] <String>] [[-RequestedTTL] <TimeSpan>]
 [-RequestedTime <DateTime>] [<CommonParameters>]
```

## DESCRIPTION
The **New-PAMRequest** cmdlet creates a Privileged Access Management (PAM) activation request in the Microsoft Identity Manager (MIM) Service.
You must specify a role, using either the *Role* or *RoleDisplayName* parameters that indicates the security groups to which the user is requesting to be added.

## EXAMPLES

### Example 1: Create a new request for a PAM role
```
PS C:\> New-PAMRequest -role $Role
```

This command creates a new request for a PAM role. 
The variable Role is assumed to have been set by a previous use of the cmdlet [Get-PAMRoleForRequest](./Get-PAMRoleForRequest.md).

## PARAMETERS

### -Justification
Specifies an optional text parameter to be included in the activation request.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestedTime
Specifies an optional delayed start time for the activation.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestedTTL
Specifies an optional override of the time to live (TTL) for the activation request.
If you don't specify this parameter, then the role default TTL is used instead.

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Role
Specifies the PAM role in the MIM Service being requested, returned by [Get-PAMRoleForRequest](./Get-PAMRoleForRequest.md).

```yaml
Type: PAMRoleForRequest
Parameter Sets: Role as PAMRole
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RoleDisplayName
Specifies the display name of the PAM role in the MIM Service being requested.

```yaml
Type: String
Parameter Sets: Role as Display Name
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMRequest

## NOTES

## RELATED LINKS

[Close-PAMRequest](xref:MIMPAM/vlatest/Close-PAMRequest.md)

[Get-PAMRequest](xref:MIMPAM/vlatest/Get-PAMRequest.md)

[Get-PAMRoleForRequest](xref:MIMPAM/vlatest/Get-PAMRoleForRequest.md)

[Microsoft Identity Manager (xref:MIMPAM/vlatest/MIMPAM.md)
