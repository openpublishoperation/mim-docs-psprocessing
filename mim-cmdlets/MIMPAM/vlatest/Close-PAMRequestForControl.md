---
external help file: Microsoft.IdentityManagement.AdminPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: D68A83DC-0EA8-4405-AD1F-C55E3ADE5AE0
updated_at: 4/24/2017 10:54 PM
ms.date: 4/24/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/MIMPAM/vlatest/Close-PAMRequestForControl.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/MIMPAM/vlatest/Close-PAMRequestForControl.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/3e9264276b5141f0a82bd9905d67bb4900c9c2b3/mim-cmdlets/MIMPAM/vlatest/Close-PAMRequestForControl.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Close-PAMRequestForControl

## SYNOPSIS
Cancels current PAM activation requests from other users.

## SYNTAX

### Role
```
Close-PAMRequestForControl [-Role] <PAMRole> [-Force] [<CommonParameters>]
```

### User
```
Close-PAMRequestForControl [-User] <PAMUser> [-Force] [<CommonParameters>]
```

### Request
```
Close-PAMRequestForControl [-Request] <PAMRequest> [-Force] [<CommonParameters>]
```

### All
```
Close-PAMRequestForControl [-All] [-Force] [<CommonParameters>]
```

## DESCRIPTION
The **Close-PAMRequestForControl** cmdlet cancels current Privileged Access Management (PAM) activation requests.
One of the *All*, *Request*, *Role*, or *User* parameters can be specified.

## EXAMPLES

### Example 1: Close requests from a specific user
```
PS C:\> Close-PAMRequestForControl -User (Get-PAMUser -PrivDisplayName "contoso.PattiFul")
```

This command closes all requests a specified user made.

## PARAMETERS

### -All
Indicates that all active requests are closed if the *Request*, *Role*, or *User* parameters are not specified.

```yaml
Type: SwitchParameter
Parameter Sets: All
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
Forces the command to run without asking for user confirmation.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Request
Specifies an object returned by an earlier call to [Get-PAMRequest](./Get-PAMRequest.md).

```yaml
Type: PAMRequest
Parameter Sets: Request
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Role
Specifies an object returned by an earlier call to [Get-PAMRole](./Get-PAMRole.md).

```yaml
Type: PAMRole
Parameter Sets: Role
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -User
Specifies an object returned by an earlier call to [Get-PAMUser](./Get-PAMUser.md).

```yaml
Type: PAMUser
Parameter Sets: User
Aliases: 

Required: True
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

[Get-PAMRequest](xref:MIMPAM/vlatest/Get-PAMRequest.md)

[Get-PAMRole](xref:MIMPAM/vlatest/Get-PAMRole.md)

[Get-PAMUser](xref:MIMPAM/vlatest/Get-PAMUser.md)

[Microsoft Identity Manager (xref:MIMPAM/vlatest/MIMPAM.md)
