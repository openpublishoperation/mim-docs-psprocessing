---
external help file: Microsoft.IdentityManagement.AdminPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: D41947C3-21DE-4585-824D-B164891FC6D7
updated_at: 4/24/2017 10:54 PM
ms.date: 4/24/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/Get-PAMRequest.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/Get-PAMRequest.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/3e9264276b5141f0a82bd9905d67bb4900c9c2b3/mim-cmdlets/MIMPAM/vlatest/Get-PAMRequest.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Get-PAMRequest

## SYNOPSIS
Gets PAM requests from the MIM Service.

## SYNTAX

### Basic (Default)
```
Get-PAMRequest [-User] <PAMUser> [-Active] [-Expired] [-Rejected] [-Pending] [-Closed] [-All]
 [[-Filter] <String>] [<CommonParameters>]
```

### Extended
```
Get-PAMRequest [-User] <PAMUser> [[-Filter] <String>] [-Extended] [<CommonParameters>]
```

## DESCRIPTION
The **Get-PAMRequest** cmdlet gets activation requests that have been requested by a specified user.
You must specify the user object parameter that can be retrieved by calling the [Get-PAMUser](./Get-PAMUser.md) cmdlet.

## EXAMPLES

### Example 1: View requests from a user
```
PS C:\> Get-PAMRequest -User (Get-PAMUser -PrivDisplayName "contoso.Jen")
```

This command retrieves requests from a user that are stored in the MIM Service.

## PARAMETERS

### -Active
Indicates that returned request objects are filtered to be activation requests that are currently active.

```yaml
Type: SwitchParameter
Parameter Sets: Basic
Aliases: 

Required: False
Position: 2
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

### -Expired
Indicates that requests which have expired are returned by this cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: Basic
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Rejected
Indicates that requests that were pending approval and were rejected are returned by this cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: Basic
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pending
Indicates that this cmdlet returns PAM requests that are pending.

```yaml
Type: SwitchParameter
Parameter Sets: Basic
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Closed
Indicates that requests which are canceled are returned by this cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: Basic
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -All
Indicates that requests which are pending authorization are returned by this cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: Basic
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Extended
Indicates that the cmdlet returns requests with all the extended properties.

```yaml
Type: SwitchParameter
Parameter Sets: Extended
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -User
Specifies the user whose requests are to be returned.
Obtained from an earlier call to [Get-PAMUser](./Get-PAMUser.md).

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMRequest

## NOTES

## RELATED LINKS

[Close-PAMRequest](xref:MIMPAM/vlatest/Close-PAMRequest.md)

[New-PAMRequest](xref:MIMPAM/vlatest/New-PAMRequest.md)

[Microsoft Identity Manager (xref:MIMPAM/vlatest/MIMPAM.md)
