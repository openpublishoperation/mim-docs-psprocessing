---
external help file: Microsoft.IdentityManagement.AdminPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: E97C36FB-D472-47EF-83F3-6916EB14EA4A
updated_at: 4/24/2017 10:54 PM
ms.date: 4/24/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/MIMPAM/vlatest/Remove-PAMRole.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/MIMPAM/vlatest/Remove-PAMRole.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/3e9264276b5141f0a82bd9905d67bb4900c9c2b3/mim-cmdlets/MIMPAM/vlatest/Remove-PAMRole.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Remove-PAMRole

## SYNOPSIS
Removes a PAM role from the MIM Service.

## SYNTAX

```
Remove-PAMRole [-Role] <PAMRole> [-Force] [[-Session] <PAMSession>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-PAMRole** cmdlet removes a Privileged Access Management (PAM) role from the Microsoft Identity Manager (MIM) Service.

## EXAMPLES

### Example 1: Remove a role
```
PS C:\> Remove-PAMRole -Role (Get-PAMRole -DisplayName "IT")
```

This command removes a single role with a specified display name from the MIM Service.

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

### -Role
Specifies the role to be deleted.
You can get the role by calling the [Get-PAMRole](./Get-PAMRole.md) cmdlet.

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
Position: 2
Default value: None
Accept pipeline input: False
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

[Get-PAMRole](xref:MIMPAM/vlatest/Get-PAMRole.md)

[New-PAMRole](xref:MIMPAM/vlatest/New-PAMRole.md)

[Set-PAMRole](xref:MIMPAM/vlatest/Set-PAMRole.md)

[Microsoft Identity Manager (xref:MIMPAM/vlatest/MIMPAM.md)
