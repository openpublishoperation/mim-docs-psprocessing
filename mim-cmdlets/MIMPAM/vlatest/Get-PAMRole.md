---
external help file: Microsoft.IdentityManagement.AdminPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 0BAAE78C-6BB9-41C5-B0CC-76A85AA90A8A
updated_at: 5/17/2017 7:27 PM
ms.date: 5/17/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/Get-PAMRole.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/Get-PAMRole.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/700d23db59d8a09b3e8f23225322beb52d5b1d73/mim-cmdlets/MIMPAM/vlatest/Get-PAMRole.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Get-PAMRole

## SYNOPSIS
Gets PAM roles from the MIM Service.

## SYNTAX

```
Get-PAMRole [[-DisplayName] <String>] [[-Session] <PAMSession>] [-Active] [[-Filter] <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-PAMRole** cmdlet gets Privileged Access Management (PAM) roles from the Microsoft Identity Manager (MIM) Service.

## EXAMPLES

### Example 1: Retrieve a single PAM role
```
PS C:\> $Role = Get-PAMRole -DisplayName "IT"
```

This command gets a single PAM role with a specified display name from the MIM Service.

## PARAMETERS

### -Active
Indicates that this cmdlet gets roles with activation requests that are currently active.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Specifies a matching value for the DisplayName attribute of a PAM role resource in the MIM Service.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filter
Specifies a clause to use as a filter.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Session
Specifies a session with the PAM domain and the MIM Service.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMRole

## NOTES

## RELATED LINKS

[New-PAMRole](xref:MIMPAM/vlatest/New-PAMRole.md)

[Remove-PAMRole](xref:MIMPAM/vlatest/Remove-PAMRole.md)

[Set-PAMRole](xref:MIMPAM/vlatest/Set-PAMRole.md)


