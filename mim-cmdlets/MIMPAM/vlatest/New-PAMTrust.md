---
external help file: Microsoft.IdentityManagement.AdminPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 54D81A07-17E4-4FB4-B936-7EA5E4AD7186
updated_at: 5/17/2017 7:27 PM
ms.date: 5/17/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/New-PAMTrust.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/New-PAMTrust.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/700d23db59d8a09b3e8f23225322beb52d5b1d73/mim-cmdlets/MIMPAM/vlatest/New-PAMTrust.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# New-PAMTrust

## SYNOPSIS
Creates a trust relationship of the PAM domain from a domain in an existing forest.

## SYNTAX

```
New-PAMTrust [-SourceForest] <String> [-Credentials] <PSCredential> [-Bidirectional] [<CommonParameters>]
```

## DESCRIPTION
The **New-PAMTrust** cmdlet establishes a trust relationship from a domain in an existing forest to the Privileged Access Management (PAM) domain.

## EXAMPLES

### Example 1: Establish a trust relationship of the PAM domain from a domain in an existing forest
```
PS C:\> New-PAMTrust -SourceForest "Contoso" -Credentials (Get-Credential)
```

This command establishes trust from an existing forest with a root domain with NetBIOS name Contoso to the PAM domain.
The cmdlet prompts the user to provide administrator credentials to manage in that forest.

## PARAMETERS

### -Bidirectional
Switch Parameter to establish bidirectional trust between PAM domain from a domain and an existing forest.

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

### -Credentials
Specifies credentials to authenticate as an administrator to the existing forest.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceForest
Specifies the domain name of the existing forest.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Remove-PAMTrust](xref:MIMPAM/vlatest/Remove-PAMTrust.md)

[Test-PAMTrust](xref:MIMPAM/vlatest/Test-PAMTrust.md)


