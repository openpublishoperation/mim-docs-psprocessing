---
external help file: Microsoft.IdentityManagement.AdminPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: F0AFA455-F856-4ECE-8C93-A91F69C28337
updated_at: 5/17/2017 7:27 PM
ms.date: 5/17/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/Remove-PAMTrust.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/Remove-PAMTrust.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/700d23db59d8a09b3e8f23225322beb52d5b1d73/mim-cmdlets/MIMPAM/vlatest/Remove-PAMTrust.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Remove-PAMTrust

## SYNOPSIS
Removes a trust relationship of the PAM forest from an existing forest that was established by the New-PAMTrust cmdlet.

## SYNTAX

```
Remove-PAMTrust [-SourceForest] <String> [-Credentials] <PSCredential> [<CommonParameters>]
```

## DESCRIPTION
The **Remove-PAMTrust** cmdlet removes the trust relationship that a forest has to the Privileged Access Management (PAM) forest.
It is assumed that the trust was originally created by the [New-PAMTrust](./New-PAMTrust.md) cmdlet.
This cmdlet only removes the trust relationship and does not remove domain configuration data from the source domains.

## EXAMPLES

### Example 1: Remove the trust relationship with another forest
```
PS C:\> $SFC = Get-Credential ; Remove-PAMTrust -SourceForest "contoso.local" -Credentials $SFC
```

This cmdlet removes the trust relationship which had been established with the source domain in another forest. 
Note that it requires authentication credentials for an administrator user in that forest.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-PAMTrust](xref:MIMPAM/vlatest/New-PAMTrust.md)

[Test-PAMTrust](xref:MIMPAM/vlatest/Test-PAMTrust.md)


