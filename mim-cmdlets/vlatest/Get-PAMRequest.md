---
external help file: MIMPAM_Cmdlets.xml
online version: c4e502ea-abf6-4cf5-afe8-85d544bda79d
schema: 2.0.0
ms.assetid: D41947C3-21DE-4585-824D-B164891FC6D7
updated_at: 12/16/2016 10:21 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/MicrosoftIdentityManager/vlatest/Get-PAMRequest.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/MicrosoftIdentityManager/vlatest/Get-PAMRequest.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/5d96fa08a7ab9495ea82f55bde05b621f03e62cc/MicrosoftIdentityManager/vlatest/Get-PAMRequest.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# Get-PAMRequest

## SYNOPSIS
Gets PAM requests from the MIM Service.

## SYNTAX

```
Get-PAMRequest [-User] <PAMUser> [-Active] [-Expired] [-Rejected] [-Pending] [-Closed] [-All]
 [[-Filter] <String>]
```

## DESCRIPTION
The **Get-PAMRequest** cmdlet gets activation requests that have been requested by a specified user.
You must specify the user object parameter that can be retrieved by calling the Get-PAMUser cmdlet.

## EXAMPLES

### Example 1: View requests from a user
```
PS C:\>Get-PAMRequest -User (Get-PAMUser -PrivDisplayName "contoso.Jen")
```

This command retrieves requests from a user that are stored in the MIM Service.

## PARAMETERS

### -Active
Indicates that returned request objects are filtered to be activation requests that are currently active.

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
Indicates that requests which are pending authorization are returned by this cmdlet.

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
Indicates that requests which are canceled are returned by this cmdlet.

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
Indicates that requests which have expired are returned by this cmdlet.

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
Indicates that requests that were pending approval and were rejected are returned by this cmdlet.

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

### -User
Specifies the user whose requests are to be returned.
Obtained from an earlier call to Get-PAMUser.

```yaml
Type: PAMUser
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMRequest

## NOTES

## RELATED LINKS

[Close-PAMRequest](xref:vlatest/Close-PAMRequest.md)

[New-PAMRequest](xref:vlatest/New-PAMRequest.md)

[Microsoft Identity Manager (xref:vlatest/MIMPAM.md)

