---
external help file: MIMPAM_Cmdlets.xml
online version: 6012424e-297f-40df-bfd0-7c815217d560
schema: 2.0.0
ms.assetid: 4AE2B6EF-9538-4AFC-BC61-924EA4C37FA8
updated_at: 12/16/2016 10:21 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/MicrosoftIdentityManager/vlatest/Test-PAMDomainConfiguration.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/MicrosoftIdentityManager/vlatest/Test-PAMDomainConfiguration.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/5d96fa08a7ab9495ea82f55bde05b621f03e62cc/MicrosoftIdentityManager/vlatest/Test-PAMDomainConfiguration.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# Test-PAMDomainConfiguration

## SYNOPSIS
Verifies a domain has been prepared for its user and group resources to be managed by PAM.

## SYNTAX

```
Test-PAMDomainConfiguration [-SourceDomain] <String> [-Credentials] <PSCredential>
```

## DESCRIPTION
The **Test-PAMDomainConfiguration** cmdlet verifies a domain has been prepared for its user and group resources to be managed by Privileged Access Management (PAM).
This cmdlet assumes an earlier call to New-PAMDomainConfiguration has been made.

## EXAMPLES

### Example 1: Validate the domain configuration objects exist in a source domain in another forest
```
PS C:\>$SFC = Get-Credential ; Test-PAMDomainConfiguration -SourceDomain "contoso" -Credentials $SFC
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

## INPUTS

## OUTPUTS

### String

## NOTES

## RELATED LINKS

[New-PAMDomainConfiguration](xref:vlatest/New-PAMDomainConfiguration.md)

[Remove-PAMDomainConfiguration](xref:vlatest/Remove-PAMDomainConfiguration.md)

[Microsoft Identity Manager (xref:vlatest/MIMPAM.md)

