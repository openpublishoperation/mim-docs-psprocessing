---
external help file: MIMPAM_Cmdlets.xml
online version: 709bc14a-0c25-4f11-9816-8df2f220c8ee
schema: 2.0.0
ms.assetid: 6012424E-297F-40DF-BFD0-7C815217D560
updated_at: 12/16/2016 10:39 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/New-PAMDomainConfiguration.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/New-PAMDomainConfiguration.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/91e8680653c5bbea5afddb262c8a143482b14fd5/mim-cmdlets/MicrosoftIdentityManager/vlatest/New-PAMDomainConfiguration.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# New-PAMDomainConfiguration

## SYNOPSIS
Updates a domain in an existing forest to add configuration data required by PAM.

## SYNTAX

```
New-PAMDomainConfiguration [-SourceDomain] <String> [-Credentials] <PSCredential>
```

## DESCRIPTION
The **New-PAMDomainConfiguration** cmdlet updates a domain in an existing forest to add configuration data required by Privileged Access Management (PAM). 
You should invoke this cmdlet subsequently to the New-PAMTrust cmdlet.

## EXAMPLES

### Example 1: Update a domain
```
PS C:\>New-PAMDomainConfiguration -SourceDomain "Contoso" -Credentials (Get-Credential)
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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Remove-PAMDomainConfiguration](xref:MicrosoftIdentityManager/vlatest/Remove-PAMDomainConfiguration.md)

[Test-PAMDomainConfiguration](xref:MicrosoftIdentityManager/vlatest/Test-PAMDomainConfiguration.md)



