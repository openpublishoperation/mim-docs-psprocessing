---
external help file: MIMPAM_Cmdlets.xml
online version: 811219bb-df83-431f-ae84-812b137bac7a
schema: 2.0.0
ms.assetid: 19EB62F6-443A-4D61-9AB3-CFF2D3249BD1
updated_at: 12/16/2016 10:21 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/MicrosoftIdentityManager/vlatest/Remove-PAMGroup.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/MicrosoftIdentityManager/vlatest/Remove-PAMGroup.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/5d96fa08a7ab9495ea82f55bde05b621f03e62cc/MicrosoftIdentityManager/vlatest/Remove-PAMGroup.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# Remove-PAMGroup

## SYNOPSIS
Removes a PAM group from the MIM Service.

## SYNTAX

```
Remove-PAMGroup [-Group] <PAMGroup> [[-Session] <PAMSession>] [-Force] [-Confirm] [-WhatIf]
```

## DESCRIPTION
The **Remove-PAMGroup** cmdlet can be used to remove a Privileged Access Management (PAM) group from the Microsoft Identity Manager (MIM) Service and PAM domain.

## EXAMPLES

### Example 1: Remove a group
```
PS C:\>Remove-PAMGroup -Group (Get-PAMGroup -PrivDisplayName "contoso.corpadmins")
```

This command removes a single group with a specified display name from the MIM Service and the PAM domain.

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

### -Group
Specifies the group to be deleted.
You can get the group by calling the Get-PAMGroup cmdlet.

```yaml
Type: PAMGroup
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

[Get-PAMGroup](xref:vlatest/Get-PAMGroup.md)

[New-PAMGroup](xref:vlatest/New-PAMGroup.md)

[Set-PAMGroup](xref:vlatest/Set-PAMGroup.md)

[Microsoft Identity Manager (xref:vlatest/MIMPAM.md)

