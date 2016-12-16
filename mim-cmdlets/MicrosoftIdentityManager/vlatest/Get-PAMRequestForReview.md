---
external help file: MIMPAM_Cmdlets.xml
online version: a328df0f-5d32-4a48-9e6b-b1c5f9899257
schema: 2.0.0
ms.assetid: E6CEA6F8-5A7A-4C5F-9034-BA2E72952D95
updated_at: 12/16/2016 10:39 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/Get-PAMRequestForReview.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/Get-PAMRequestForReview.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/91e8680653c5bbea5afddb262c8a143482b14fd5/mim-cmdlets/MicrosoftIdentityManager/vlatest/Get-PAMRequestForReview.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# Get-PAMRequestForReview

## SYNOPSIS
Gets PAM activation requests for this user from the MIM Service.

## SYNTAX

```
Get-PAMRequestForReview [-Active] [-Expired] [-Rejected] [-Pending] [-Closed] [-All] [[-Filter] <String>]
```

## DESCRIPTION
The **Get-PAMRequestForReview** cmdlet gets Privileged Access Management (PAM) activation requests for this user from the Microsoft Identity Manager (MIM) Service.

## EXAMPLES

### Example 1: Retrieves requests that are active
```
PS C:\>Get-PAMRequestForReview -Active
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
Position: 7
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
Position: 6
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
Position: 8
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

## INPUTS

## OUTPUTS

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMRequest

## NOTES

## RELATED LINKS

[Get-PAMRequestToApprove](xref:MicrosoftIdentityManager/vlatest/Get-PAMRequestToApprove.md)



