---
external help file: Microsoft.IdentityManagement.RequestorPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: A328DF0F-5D32-4A48-9E6B-B1C5F9899257
updated_at: 4/24/2017 10:54 PM
ms.date: 4/24/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/MIMPAM/vlatest/Get-PAMRequestToApprove.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/MIMPAM/vlatest/Get-PAMRequestToApprove.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/3e9264276b5141f0a82bd9905d67bb4900c9c2b3/mim-cmdlets/MIMPAM/vlatest/Get-PAMRequestToApprove.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Get-PAMRequestToApprove

## SYNOPSIS
Gets PAM activation requests from another user that are pending approval.

## SYNTAX

```
Get-PAMRequestToApprove [<CommonParameters>]
```

## DESCRIPTION
The **Get-PAMRequestToApprove** cmdlet gets Privileged Access Management (PAM) activation requests from another user that are pending approval.
If the user is a role owner, then this cmdlet returns requests from other users that are currently pending approval for activation into that role. 
The objects returned from this cmdlet are provided to [Set-PAMRequestToApprove](./Set-PAMRequestToApprove.md) to approve or reject the request.

## EXAMPLES

### Example 1: Get requests that are pending approval
```
PS C:\> $Requests = Get-PAMRequestToApprove
```

This command returns requests other users made earlier that are pending approval.

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMRequestToApprove

## NOTES

## RELATED LINKS

[Set-PAMRequestToApprove](xref:MIMPAM/vlatest/Set-PAMRequestToApprove.md)

[Microsoft Identity Manager (xref:MIMPAM/vlatest/MIMPAM.md)
