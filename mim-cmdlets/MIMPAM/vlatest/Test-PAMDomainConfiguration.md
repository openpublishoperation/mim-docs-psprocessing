---
external help file: Microsoft.IdentityManagement.AdminPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 4AE2B6EF-9538-4AFC-BC61-924EA4C37FA8
updated_at: 5/17/2017 7:27 PM
ms.date: 5/17/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/Test-PAMDomainConfiguration.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/Test-PAMDomainConfiguration.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/700d23db59d8a09b3e8f23225322beb52d5b1d73/mim-cmdlets/MIMPAM/vlatest/Test-PAMDomainConfiguration.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Test-PAMDomainConfiguration

## SYNOPSIS
Verifies a domain has been prepared for its user and group resources to be managed by PAM.

## SYNTAX

```
Test-PAMDomainConfiguration [-SourceDomain] <String> [-Credentials] <PSCredential> [<CommonParameters>]
```

## DESCRIPTION
The **Test-PAMDomainConfiguration** cmdlet verifies a domain has been prepared for its user and group resources to be managed by Privileged Access Management (PAM).
This cmdlet assumes an earlier call to [New-PAMDomainConfiguration](./New-PAMDomainConfiguration.md) has been made.

## EXAMPLES

### Example 1: Validate the domain configuration objects exist in a source domain in another forest
```
PS C:\> $SFC = Get-Credential ; Test-PAMDomainConfiguration -SourceDomain "contoso" -Credentials $SFC
```

This command indicates whether the trust relationship has been established with the source domain in another forest. 
Note that it requires authentication credentials for an administrator user in that forest.

## PARAMETERS

### -Credentials
Specifies the credentials to authenticate as an administrator to the domain where the source users and groups are located.

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

### -SourceDomain
Specifies the NetBIOS name of the domain in which the existing users and groups are located.

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

### String

## NOTES

## RELATED LINKS

[New-PAMDomainConfiguration](xref:MIMPAM/vlatest/New-PAMDomainConfiguration.md)

[Remove-PAMDomainConfiguration](xref:MIMPAM/vlatest/Remove-PAMDomainConfiguration.md)


