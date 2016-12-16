---
external help file: MIMPAM_Cmdlets.xml
online version: f0afa455-f856-4ece-8c93-a91f69c28337
schema: 2.0.0
ms.assetid: 54D81A07-17E4-4FB4-B936-7EA5E4AD7186
updated_at: 12/16/2016 10:33 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/New-PAMTrust.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/New-PAMTrust.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/d2936ea0bd6215b3aed43b77e4d364e636108a4d/mim-cmdlets/MicrosoftIdentityManager/vlatest/New-PAMTrust.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# New-PAMTrust

## SYNOPSIS
Creates a trust relationship of the PAM domain from a domain in an existing forest.

## SYNTAX

```
New-PAMTrust [-SourceForest] <String> [-Credentials] <PSCredential>
```

## DESCRIPTION
The **New-PAMTrust** cmdlet establishes a trust relationship from a domain in an existing forest to the PAM domain.

## EXAMPLES

### Example 1: Establish a trust relationship of the PAM domain from a domain in an existing forest
```
PS C:\>New-PAMTrust -SourceForest "Contoso" -Credentials (Get-Credential)
```

This command establishes trust from an existing forest with a root domain with NetBIOS name Contoso to the PAM domain.
The cmdlet prompts the user to provide administrator credentials to manage in that forest.

## PARAMETERS

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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Remove-PAMTrust](xref:MicrosoftIdentityManager/vlatest/Remove-PAMTrust.md)

[Test-PAMTrust](xref:MicrosoftIdentityManager/vlatest/Test-PAMTrust.md)

[Microsoft Identity Manager Privileged Access Management Administrator](xref:MicrosoftIdentityManager/vlatest/MIMPAM.md)

