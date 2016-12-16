---
external help file: MIMPAM_Cmdlets.xml
online version: 54d81a07-17e4-4fb4-b936-7ea5e4ad7186
schema: 2.0.0
ms.assetid: 8113A53B-C081-44AE-877B-42A23B90E5AA
updated_at: 12/16/2016 10:24 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/Test-PAMTrust.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/Test-PAMTrust.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/d76fe71a336b890697ca5b79f29d35c57acf4cc6/mim-cmdlets/MicrosoftIdentityManager/vlatest/Test-PAMTrust.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# Test-PAMTrust

## SYNOPSIS
Verifies whether a trust relationship exists from the source forest in the PAM domain.

## SYNTAX

```
Test-PAMTrust [-SourceForest] <String> [-Credentials] <PSCredential>
```

## DESCRIPTION
The **Test-PAMTrust** cmdlet verifies whether a trust relationship exists from source forest in the Privileged Access Management (PAM) domain.
The trust relationship needed to be established by an earlier call to New-PAMTrust.

## EXAMPLES

### Example 1: Validate the trust relationship with another forest
```
PS C:\>$SFC = Get-Credential ; $Result = Test-PAMTrust -SourceForest "contoso.local" -Credentials $SFC
```

This command returns whether the trust relationship has been established with the source forest. 
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
Specifies the NetBIOS domain name of the root domain of the forest.

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

### bool

## NOTES

## RELATED LINKS

[New-PAMTrust](xref:MicrosoftIdentityManager/vlatest/New-PAMTrust.md)

[Remove-PAMTrust](xref:MicrosoftIdentityManager/vlatest/Remove-PAMTrust.md)

[Microsoft Identity Manager (xref:MicrosoftIdentityManager/vlatest/MIMPAM.md)

