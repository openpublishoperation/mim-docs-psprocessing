---
external help file: Microsoft.IdentityManagement.AdminPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 709BC14A-0C25-4F11-9816-8DF2F220C8EE
updated_at: 5/17/2017 7:27 PM
ms.date: 5/17/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/Remove-PAMDomainConfiguration.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/Remove-PAMDomainConfiguration.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/700d23db59d8a09b3e8f23225322beb52d5b1d73/mim-cmdlets/MIMPAM/vlatest/Remove-PAMDomainConfiguration.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Remove-PAMDomainConfiguration

## SYNOPSIS
Updates a domain in an existing forest to remove configuration data required by PAM.

## SYNTAX

```
Remove-PAMDomainConfiguration [-SourceDomain] <String> [-Credentials] <PSCredential> [<CommonParameters>]
```

## DESCRIPTION
The **Remove-PAMDomainConfiguration** cmdlet updates a domain in an existing forest to remove configuration data required by Privileged Access Management (PAM).
The configuration data would have been created by an earlier call to [New-PAMDomainConfiguration](./New-PAMDomainConfiguration.md).

## EXAMPLES

### Example 1: Remove the domain configuration objects from a domain in another forest
```
PS C:\> $SFC = Get-Credential ; Remove-PAMDomainConfiguration -SourceDomain "contoso" -Credentials $SFC
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-PAMDomainConfiguration](xref:MIMPAM/vlatest/New-PAMDomainConfiguration.md)

[Test-PAMDomainConfiguration](xref:MIMPAM/vlatest/Test-PAMDomainConfiguration.md)


