---
external help file: Microsoft.IdentityManagement.AdminPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 6012424E-297F-40DF-BFD0-7C815217D560
updated_at: 5/17/2017 7:27 PM
ms.date: 5/17/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/New-PAMDomainConfiguration.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/New-PAMDomainConfiguration.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/700d23db59d8a09b3e8f23225322beb52d5b1d73/mim-cmdlets/MIMPAM/vlatest/New-PAMDomainConfiguration.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# New-PAMDomainConfiguration

## SYNOPSIS
Updates a domain in an existing forest to add configuration data required by PAM.

## SYNTAX

```
New-PAMDomainConfiguration [-SourceDomain] <String> [-Credentials] <PSCredential> [<CommonParameters>]
```

## DESCRIPTION
The **New-PAMDomainConfiguration** cmdlet updates a domain in an existing forest to add configuration data required by Privileged Access Management (PAM). 
You should invoke this cmdlet subsequently to the [New-PAMTrust](./New-PAMTrust.md) cmdlet.

## EXAMPLES

### Example 1: Update a domain
```
PS C:\> New-PAMDomainConfiguration -SourceDomain "Contoso" -Credentials (Get-Credential)
```

This command updates a domain with NetBIOS name Contoso to set the configuration data required to be managed from the PAM domain.
You are then prompted to provide administrator credentials to manage in that forest.

## PARAMETERS

### -Credentials
Specifies credentials to authenticate as an administrator to the domain where the source groups are located.

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
Specifies the NetBIOS name of the domain in which the existing groups are located.

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

[Remove-PAMDomainConfiguration](xref:MIMPAM/vlatest/Remove-PAMDomainConfiguration.md)

[Test-PAMDomainConfiguration](xref:MIMPAM/vlatest/Test-PAMDomainConfiguration.md)


