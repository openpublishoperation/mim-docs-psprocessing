---
external help file: MIMPAM_Cmdlets.xml
online version: 0baae78c-6bb9-41c5-b0cc-76a85aa90a8a
schema: 2.0.0
ms.assetid: E97C36FB-D472-47EF-83F3-6916EB14EA4A
updated_at: 12/16/2016 10:33 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/Remove-PAMRole.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/Remove-PAMRole.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/d2936ea0bd6215b3aed43b77e4d364e636108a4d/mim-cmdlets/MicrosoftIdentityManager/vlatest/Remove-PAMRole.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# Remove-PAMRole

## SYNOPSIS
Removes a PAM role from the MIM Service.

## SYNTAX

```
Remove-PAMRole [-Role] <PAMRole> [[-Session] <PAMSession>] [-Force] [-Confirm] [-WhatIf]
```

## DESCRIPTION
The **Remove-PAMRole** cmdlet removes a Privileged Access Management (PAM) role from the Microsoft Identity Manager (MIM) Service.

## EXAMPLES

### Example 1: Remove a role
```
PS C:\>Remove-PAMRole -Role (Get-PAMRole -DisplayName "IT")
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
You can get the role by calling the Get-PAMRole cmdlet.

```yaml
Type: PAMRole
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True(ByValue)
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
Aliases: 

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
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-PAMRole](xref:MicrosoftIdentityManager/vlatest/Get-PAMRole.md)

[New-PAMRole](xref:MicrosoftIdentityManager/vlatest/New-PAMRole.md)

[Set-PAMRole](xref:MicrosoftIdentityManager/vlatest/Set-PAMRole.md)

[Microsoft Identity Manager Privileged Access Management Administrator](xref:MicrosoftIdentityManager/vlatest/MIMPAM.md)

