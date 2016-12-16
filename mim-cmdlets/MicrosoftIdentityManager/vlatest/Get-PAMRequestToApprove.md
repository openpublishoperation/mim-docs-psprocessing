---
external help file: MIMPAM_Cmdlets.xml
online version: bae2036a-2be3-4625-8f42-e4c0373e16cb
schema: 2.0.0
ms.assetid: A328DF0F-5D32-4A48-9E6B-B1C5F9899257
updated_at: 12/16/2016 10:24 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/Get-PAMRequestToApprove.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/Get-PAMRequestToApprove.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/d76fe71a336b890697ca5b79f29d35c57acf4cc6/mim-cmdlets/MicrosoftIdentityManager/vlatest/Get-PAMRequestToApprove.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# Get-PAMRequestToApprove

## SYNOPSIS
Gets PAM activation requests from another user that are pending approval.

## SYNTAX

```
Get-PAMRequestToApprove
```

## DESCRIPTION
The **Get-PAMRequestToApprove** cmdlet gets Privileged Access Management (PAM) activation requests from another user that are pending approval.
If the user is a role owner, then this cmdlet returns requests from other users that are currently pending approval for activation into that role. 
The objects returned from this cmdlet are provided to Set-PAMRequestToApprove to approve or reject the request.

## EXAMPLES

### Example 1: Retrieve requests that are pending approval
```
PS C:\>$Requests = Get-PAMRequestToApprove
```

This command returns requests other users made earlier that are pending approval.

## PARAMETERS

## INPUTS

## OUTPUTS

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMRequestToApprove

## NOTES

## RELATED LINKS

[Set-PAMRequestToApprove](xref:MicrosoftIdentityManager/vlatest/Set-PAMRequestToApprove.md)

[Microsoft Identity Manager (xref:MicrosoftIdentityManager/vlatest/MIMPAM.md)

