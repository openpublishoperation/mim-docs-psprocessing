---
external help file: MIMPAM_Cmdlets.xml
online version: 4066d446-6ee0-4d1c-b4ee-5069e32d9567
schema: 2.0.0
ms.assetid: CCB40ADA-BCF8-4706-8267-94BCA06C710F
updated_at: 12/16/2016 10:24 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/Remove-PAMUser.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/Remove-PAMUser.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/d76fe71a336b890697ca5b79f29d35c57acf4cc6/mim-cmdlets/MicrosoftIdentityManager/vlatest/Remove-PAMUser.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# Remove-PAMUser

## SYNOPSIS
Removes a user from the MIM Service and the PAM domain.

## SYNTAX

```
Remove-PAMUser [-User] <PAMUser> [[-Session] <PAMSession>] [-Force] [-Confirm] [-WhatIf]
```

## DESCRIPTION
The **Remove-PAMUser** cmdlet removes a user from the Microsoft Identity Manager (MIM) Service and the Privileged Access Management (PAM) domain.
The user to be deleted is indicated by an object returned by a call to Get-PAMUser.

## EXAMPLES

### Example 1: Remove a user
```
PS C:\>Remove-PAMUser -User (Get-PAMUser -PrivDisplayName "contoso.jen")
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
You can use the Get-PAMUser cmdlet to get the user that needs to be deleted.

```yaml
Type: PAMUser
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True(ByValue)
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

[Get-PAMUser](xref:MicrosoftIdentityManager/vlatest/Get-PAMUser.md)

[New-PAMUser](xref:MicrosoftIdentityManager/vlatest/New-PAMUser.md)

[Set-PAMUser](xref:MicrosoftIdentityManager/vlatest/Set-PAMUser.md)

[Microsoft Identity Manager (xref:MicrosoftIdentityManager/vlatest/MIMPAM.md)

