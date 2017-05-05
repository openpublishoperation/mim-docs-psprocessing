---
external help file: Microsoft.IdentityManagement.RequestorPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: C4E502EA-ABF6-4CF5-AFE8-85D544BDA79D
updated_at: 4/24/2017 10:54 PM
ms.date: 4/24/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/MIMPAM/vlatest/Close-PAMRequest.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/MIMPAM/vlatest/Close-PAMRequest.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/3e9264276b5141f0a82bd9905d67bb4900c9c2b3/mim-cmdlets/MIMPAM/vlatest/Close-PAMRequest.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Close-PAMRequest

## SYNOPSIS
Closes the specified user's PAM activation request.

## SYNTAX

### Role as PAMRole
```
Close-PAMRequest [[-Role] <PAMRoleForRequest>] [<CommonParameters>]
```

### Role as Display Name
```
Close-PAMRequest [[-RoleDisplayName] <String>] [<CommonParameters>]
```

### Request as PAMRequest
```
Close-PAMRequest [[-Request] <PAMRequest>] [<CommonParameters>]
```

## DESCRIPTION
The **Close-PAMRequest** cmdlet deactivates one or more of the user's Privileged Access Management (PAM) activation requests.
The *Request*, *Role*, or *RoleDisplayName* parameters must be specified.

## EXAMPLES

### Example 1: Close requests for a specific role
```
PS C:\> Close-PAMRequest -RoleDisplayName "IT"
```

This command closes request the user made earlier for a specific role.

## PARAMETERS

### -Request
Specifies the request to be deactivated.

```yaml
Type: PAMRequest
Parameter Sets: Request as PAMRequest
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Role
Specifies a role that was returned by [Get-PAMRoleForRequest](./Get-PAMRoleForRequest.md) and provided to an earlier call to [New-PAMRequest](./New-PAMRequest.md).

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
Specifies the display name of the role that was earlier requested for activation.

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

## NOTES

## RELATED LINKS

[Get-PAMRoleForRequest](xref:MIMPAM/vlatest/Get-PAMRoleForRequest.md)

[New-PAMRequest](xref:MIMPAM/vlatest/New-PAMRequest.md)

[Microsoft Identity Manager (xref:MIMPAM/vlatest/MIMPAM.md)
