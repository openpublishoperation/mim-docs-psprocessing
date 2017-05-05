---
external help file: Microsoft.IdentityManagement.RequestorPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: E6CEA6F8-5A7A-4C5F-9034-BA2E72952D95
updated_at: 4/24/2017 10:54 PM
ms.date: 4/24/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/MIMPAM/vlatest/Get-PAMRequestForReview.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/MIMPAM/vlatest/Get-PAMRequestForReview.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/3e9264276b5141f0a82bd9905d67bb4900c9c2b3/mim-cmdlets/MIMPAM/vlatest/Get-PAMRequestForReview.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Get-PAMRequestForReview

## SYNOPSIS
Gets PAM activation requests for this user from the MIM Service.

## SYNTAX

```
Get-PAMRequestForReview [-Active] [-Expired] [-Rejected] [-Pending] [-Closed] [-All] [[-Filter] <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-PAMRequestForReview** cmdlet gets Privileged Access Management (PAM) activation requests for this user from the Microsoft Identity Manager (MIM) Service.

## EXAMPLES

### Example 1: Get requests that are active
```
PS C:\> Get-PAMRequestForReview -Active
```

This command returns request the user made earlier that are still active.

## PARAMETERS

### -Active
Indicates that that this cmdlet returns activation requests that are currently active.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -All
Indicates that this cmdlet returns all requests.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Closed
Indicates that this cmdlet only return requests that were closed.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Expired
Indicates that this cmdlet returns PAM requests that have expired.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filter
Specifies a clause to use as a filter.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pending
Indicates that this cmdlet returns PAM requests that are pending.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Rejected
Indicates that this cmdlet only return requests that were pending and rejected.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMRequest

## NOTES

## RELATED LINKS

[Get-PAMRequestToApprove](xref:MIMPAM/vlatest/Get-PAMRequestToApprove.md)

[Microsoft Identity Manager (xref:MIMPAM/vlatest/MIMPAM.md)
