---
external help file: Microsoft.IdentityManagement.AdminPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: CCB40ADA-BCF8-4706-8267-94BCA06C710F
updated_at: 4/24/2017 10:54 PM
ms.date: 4/24/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/Remove-PAMUser.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/Remove-PAMUser.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/3e9264276b5141f0a82bd9905d67bb4900c9c2b3/mim-cmdlets/MIMPAM/vlatest/Remove-PAMUser.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Remove-PAMUser

## SYNOPSIS
Removes a user from the MIM Service and the PAM domain.

## SYNTAX

```
Remove-PAMUser [-User] <PAMUser> [-Force] [[-Session] <PAMSession>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-PAMUser** cmdlet removes a user from the Microsoft Identity Manager (MIM) Service and the Privileged Access Management (PAM) domain.
The user to be deleted is indicated by an object returned by a call to [Get-PAMUser](./Get-PAMUser.md).

## EXAMPLES

### Example 1: Remove a user
```
PS C:\> Remove-PAMUser -User (Get-PAMUser -PrivDisplayName "contoso.jen")
```

This command removes a single user with a specified display name from the MIM Service and the PAM domain.

## PARAMETERS

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

### -Session
Specifies the session with the PAM domain and MIM Service.

```yaml
Type: PAMSession
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -User
Specifies the user to be deleted.
You can use the **Get-PAMUser** cmdlet to get the user that needs to be deleted.

```yaml
Type: PAMUser
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-PAMUser](xref:MIMPAM/vlatest/Get-PAMUser.md)

[New-PAMUser](xref:MIMPAM/vlatest/New-PAMUser.md)

[Set-PAMUser](xref:MIMPAM/vlatest/Set-PAMUser.md)

[Microsoft Identity Manager (xref:MIMPAM/vlatest/MIMPAM.md)
