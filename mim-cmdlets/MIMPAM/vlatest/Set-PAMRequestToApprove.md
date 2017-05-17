---
external help file: Microsoft.IdentityManagement.RequestorPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: BAE2036A-2BE3-4625-8F42-E4C0373E16CB
updated_at: 5/17/2017 7:27 PM
ms.date: 5/17/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/Set-PAMRequestToApprove.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/Set-PAMRequestToApprove.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/700d23db59d8a09b3e8f23225322beb52d5b1d73/mim-cmdlets/MIMPAM/vlatest/Set-PAMRequestToApprove.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Set-PAMRequestToApprove

## SYNOPSIS
Updates a PAM activation request in the MIM Service from another user that is pending approval.

## SYNTAX

### Approve Request
```
Set-PAMRequestToApprove [-Request] <PAMRequestToApprove> [-Approve] [<CommonParameters>]
```

### Reject Request
```
Set-PAMRequestToApprove [-Request] <PAMRequestToApprove> [-Reject] [<CommonParameters>]
```

## DESCRIPTION
The **Set-PAMRequestToApprove** cmdlet updates a Privileged Access Management (PAM) activation request in the Microsoft Identity Manager (MIM) Service from another user that is pending approval.
If an activation request is pending approval, at least one of the role owners must invoke **Set-PAMRequestToApprove** cmdlet for that request and specify to approve.
The value of the *Request* parameter is returned by an earlier call to [Get-PAMRequestToApprove](./Get-PAMRequestToApprove.md).
If you reject an activation request, it will prevent the MIM Service from adding the user into security groups.

## EXAMPLES

### Example 1: Reject requests that are pending approval
```
PS C:\> $RejectApproval = Get-PAMRequestToApprove ; foreach ($request in $RejectApproval) {Set-PAMRequestToApprove -Request $request -Reject}
```

This command rejects the requests other users made earlier that are pending this user's approval.

## PARAMETERS

### -Approve
Indicates that an activation request is allowed to proceed.

```yaml
Type: SwitchParameter
Parameter Sets: Approve Request
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
Parameter Sets: Reject Request
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Request
Specifies that the request object is returned by [Get-PAMRequestToApprove](./Get-PAMRequestToApprove.md).

```yaml
Type: PAMRequestToApprove
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-PAMRequestToApprove](xref:MIMPAM/vlatest/Get-PAMRequestToApprove.md)


