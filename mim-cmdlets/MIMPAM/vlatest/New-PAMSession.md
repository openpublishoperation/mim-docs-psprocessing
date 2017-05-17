---
external help file: Microsoft.IdentityManagement.AdminPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 70B15B31-A525-4AE2-AC57-D74F97159E66
updated_at: 5/17/2017 7:27 PM
ms.date: 5/17/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/New-PAMSession.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/New-PAMSession.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/700d23db59d8a09b3e8f23225322beb52d5b1d73/mim-cmdlets/MIMPAM/vlatest/New-PAMSession.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# New-PAMSession

## SYNOPSIS
Creates a session for PAM administration with a different server.

## SYNTAX

```
New-PAMSession [[-Domain] <String>] [[-Credentials] <PSCredential>] [<CommonParameters>]
```

## DESCRIPTION
The **New-PAMSession** cmdlet creates a session for Privileged Access Management (PAM) administration interaction with Active Directory and the Microsoft Identity Manager (MIM) Service.

## EXAMPLES

### Example 1: Create a session with a local Active Directory server using the identity of the currently logged in user
```
PS C:\> $Session = New-PAMSession
```

This command prepares a session with a local Active Directory server using the identity of the currently logged in user.

## PARAMETERS

### -Credentials
Specifies credentials of a PAM domain administrator.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Domain
Specifies the domain name of the PAM domain.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMSession

## NOTES

## RELATED LINKS



