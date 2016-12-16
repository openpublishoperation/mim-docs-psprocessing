---
external help file: MIMPAM_Cmdlets.xml
online version: a328df0f-5d32-4a48-9e6b-b1c5f9899257
schema: 2.0.0
ms.assetid: BAE2036A-2BE3-4625-8F42-E4C0373E16CB
updated_at: 12/16/2016 10:24 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/Set-PAMRequestToApprove.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/Set-PAMRequestToApprove.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/d76fe71a336b890697ca5b79f29d35c57acf4cc6/mim-cmdlets/MicrosoftIdentityManager/vlatest/Set-PAMRequestToApprove.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# Set-PAMRequestToApprove

## SYNOPSIS
Updates a PAM activation request in the MIM Service from another user that is pending approval.

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Set-PAMRequestToApprove [-Request] <PAMRequestToApprove> [-Approve]
```

### UNNAMED_PARAMETER_SET_2
```
Set-PAMRequestToApprove [-Request] <PAMRequestToApprove> [-Reject]
```

## DESCRIPTION
The **Set-PAMRequestToApprove** cmdlet updates a Privileged Access Management (PAM) activation request in the Microsoft Identity Manager (MIM) Service from another user that is pending approval.
If an activation request is pending approval, at least one of the role owners must invoke Set-PAMRequestToApprove cmdlet for that request and specify to approve.
The value of the *Request* parameter is returned by an earlier call to Get-PAMRequestToApprove.
If you reject an activation request, it will prevent the MIM Service from adding the user into security groups.

## EXAMPLES

### Example 1: Reject requests that are pending approval
```
PS C:\>$RejectApproval = Get-PAMRequestToApprove ; foreach ($request in $RejectApproval) {Set-PAMRequestToApprove -Request $request -Reject}
```

This command rejects the requests other users made earlier that are pending this user's approval.

## PARAMETERS

### -Approve
Indicates that an activation request is allowed to proceed.

```yaml
Type: SwitchParameter
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Reject
Indicates that this cmdlet rejects a request, which prevents it from proceeding.

```yaml
Type: SwitchParameter
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Request
Specifies that the request object is returned by Get-PAMRequestToApprove.

```yaml
Type: PAMRequestToApprove
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True(ByValue)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-PAMRequestToApprove](xref:MicrosoftIdentityManager/vlatest/Get-PAMRequestToApprove.md)

[Microsoft Identity Manager (xref:MicrosoftIdentityManager/vlatest/MIMPAM.md)

