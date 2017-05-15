---
external help file: Microsoft.IdentityManagement.AdminPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 8113A53B-C081-44AE-877B-42A23B90E5AA
updated_at: 5/15/2017 3:45 PM
ms.date: 5/15/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/MIMPAM/vlatest/Test-PAMTrust.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/MIMPAM/vlatest/Test-PAMTrust.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/9b28322895cedef17814e137aefa9d68fe2293a6/mim-cmdlets/MIMPAM/vlatest/Test-PAMTrust.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Test-PAMTrust

## SYNOPSIS
Verifies whether a trust relationship exists from the source forest in the PAM domain.

## SYNTAX

```
Test-PAMTrust [-SourceForest] <String> [-CorpCredentials] <PSCredential> [[-PrivCredentials] <PSCredential>]
 [-Bidirectional] [<CommonParameters>]
```

## DESCRIPTION
The **Test-PAMTrust** cmdlet verifies whether a trust relationship exists from source forest in the Privileged Access Management (PAM) domain.
The trust relationship needed to be established by an earlier call to [New-PAMTrust](./New-PAMTrust.md).

## EXAMPLES

### Example 1: Validate the trust relationship with another forest
```
PS C:\> $SFC = Get-Credential ; $Result = Test-PAMTrust -SourceForest "contoso.local" -Credentials $SFC
```

This command returns whether the trust relationship has been established with the source forest. 
Note that it requires authentication credentials for an administrator user in that forest.

## PARAMETERS

### -Bidirectional
Switch Parameter to establish bidirectional trust between PAM domain from a domain and an existing forest.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CorpCredentials
Credentials to authenticate as an administrator to the existing forest.

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

### -PrivCredentials
Credentials to authenticate as an administrator to the PAM domain.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### bool

## NOTES

## RELATED LINKS

[New-PAMTrust](xref:MIMPAM/vlatest/New-PAMTrust.md)

[Remove-PAMTrust](xref:MIMPAM/vlatest/Remove-PAMTrust.md)

[Microsoft Identity Manager (xref:MIMPAM/vlatest/MIMPAM.md)
