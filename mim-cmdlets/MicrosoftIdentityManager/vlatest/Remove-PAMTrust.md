---
external help file: MIMPAM_Cmdlets.xml
online version: 54d81a07-17e4-4fb4-b936-7ea5e4ad7186
schema: 2.0.0
ms.assetid: F0AFA455-F856-4ECE-8C93-A91F69C28337
updated_at: 12/16/2016 10:24 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/Remove-PAMTrust.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/Remove-PAMTrust.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/d76fe71a336b890697ca5b79f29d35c57acf4cc6/mim-cmdlets/MicrosoftIdentityManager/vlatest/Remove-PAMTrust.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# Remove-PAMTrust

## SYNOPSIS
Removes a trust relationship of the PAM forest from an existing forest that was established by the New-PAMTrust cmdlet.

## SYNTAX

```
Remove-PAMTrust [-SourceForest] <String> [-Credentials] <PSCredential>
```

## DESCRIPTION
The **Remove-PAMTrust** cmdlet removes the trust relationship that a forest has to the Privileged Access Management (PAM) forest.
It is assumed that the trust was originally created by the New-PAMTrust cmdlet.
This cmdlet only removes the trust relationship and does not remove domain configuration data from the source domains.

## EXAMPLES

### Example 1: Remove the trust relationship with another forest
```
PS C:\>$SFC = Get-Credential ; Remove-PAMTrust -SourceForest "contoso.local" -Credentials $SFC
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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-PAMTrust](xref:MicrosoftIdentityManager/vlatest/New-PAMTrust.md)

[Test-PAMTrust](xref:MicrosoftIdentityManager/vlatest/Test-PAMTrust.md)

[Microsoft Identity Manager (xref:MicrosoftIdentityManager/vlatest/MIMPAM.md)

