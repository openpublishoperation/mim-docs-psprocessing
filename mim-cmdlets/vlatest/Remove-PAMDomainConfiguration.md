---
external help file: MIMPAM_Cmdlets.xml
online version: 6012424e-297f-40df-bfd0-7c815217d560
schema: 2.0.0
ms.assetid: 709BC14A-0C25-4F11-9816-8DF2F220C8EE
updated_at: 12/16/2016 10:21 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/MicrosoftIdentityManager/vlatest/Remove-PAMDomainConfiguration.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/MicrosoftIdentityManager/vlatest/Remove-PAMDomainConfiguration.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/5d96fa08a7ab9495ea82f55bde05b621f03e62cc/MicrosoftIdentityManager/vlatest/Remove-PAMDomainConfiguration.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# Remove-PAMDomainConfiguration

## SYNOPSIS
Updates a domain in an existing forest to remove configuration data required by PAM.

## SYNTAX

```
Remove-PAMDomainConfiguration [-SourceDomain] <String> [-Credentials] <PSCredential>
```

## DESCRIPTION
The **Remove-PAMDomainConfiguration** cmdlet updates a domain in an existing forest to remove configuration data required by Privileged Access Management (PAM).
The configuration data would have been created by an earlier call to New-PAMDomainConfiguration.

## EXAMPLES

### Example 1: Remove the domain configuration objects from a domain in another forest
```
PS C:\>$SFC = Get-Credential ; Remove-PAMDomainConfiguration -SourceDomain "contoso" -Credentials $SFC
```

This cmdlet removes the domain configuration objects from the source domain in another forest. 
Note that it requires authentication credentials for an administrator user in that forest.

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
Specifies the NetBIOS name of the domain that contains the existing users or groups.

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

[New-PAMDomainConfiguration](xref:vlatest/New-PAMDomainConfiguration.md)

[Test-PAMDomainConfiguration](xref:vlatest/Test-PAMDomainConfiguration.md)

[Microsoft Identity Manager (xref:vlatest/MIMPAM.md)

