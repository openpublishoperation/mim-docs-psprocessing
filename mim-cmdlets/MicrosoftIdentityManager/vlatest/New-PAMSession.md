---
external help file: MIMPAM_Cmdlets.xml
online version: a821a0a5-e511-4606-a532-cc8d813b1758
schema: 2.0.0
ms.assetid: 70B15B31-A525-4AE2-AC57-D74F97159E66
updated_at: 12/16/2016 10:33 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/New-PAMSession.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/New-PAMSession.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/d2936ea0bd6215b3aed43b77e4d364e636108a4d/mim-cmdlets/MicrosoftIdentityManager/vlatest/New-PAMSession.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# New-PAMSession

## SYNOPSIS
Creates a session for PAM administration with a different server.

## SYNTAX

```
New-PAMSession [[-Domain] <String>] [[-Credentials] <PSCredential>]
```

## DESCRIPTION
The **New-PAMSession** cmdlet creates a session for Privileged Access Management (PAM) administration interaction with Active Directory and the Microsoft Identity Manager (MIM) Service.

## EXAMPLES

### Example 1: Create a session with a local Active Directory server using the identity of the currently logged in user
```
PS C:\>$Session = New-PAMSession
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

## INPUTS

## OUTPUTS

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMSession

## NOTES

## RELATED LINKS

[Microsoft Identity Manager Privileged Access Management Administrator](xref:MicrosoftIdentityManager/vlatest/MIMPAM.md)

