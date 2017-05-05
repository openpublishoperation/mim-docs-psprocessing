---
external help file: Microsoft.IdentityManagement.RequestorPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: D99CB1FD-186C-422D-90A3-AF61B5E77594
updated_at: 4/24/2017 10:54 PM
ms.date: 4/24/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/MIMPAM/vlatest/Get-PAMRoleForRequest.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/MIMPAM/vlatest/Get-PAMRoleForRequest.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/3e9264276b5141f0a82bd9905d67bb4900c9c2b3/mim-cmdlets/MIMPAM/vlatest/Get-PAMRoleForRequest.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Get-PAMRoleForRequest

## SYNOPSIS
Gets PAM roles from the MIM Service.

## SYNTAX

### FilterSet (Default)
```
Get-PAMRoleForRequest [[-Filter] <String>] [-Active] [<CommonParameters>]
```

### DisplayNameSet
```
Get-PAMRoleForRequest [[-DisplayName] <String>] [-Active] [<CommonParameters>]
```

## DESCRIPTION
The **Get-PAMRoleForRequest** cmdlet gets Privileged Access Management (PAM) roles from the Microsoft Identity Manager (MIM) Service that the user is authorized to request.

## EXAMPLES

### Example 1: Get all available roles that a user can request
```
PS C:\> Get-PAMRoleForRequest
```

This command displays all available roles a user can request.

### Example 2: Get a list of roles and select a role by name
```
PS C:\> $Role = Get-PAMRoleForRequest | ? { $_.DisplayName -eq "CorpAdmins" }
```

This command gets the list of roles and selects a role named CorpAdmins.
The returned object result can then be provided to the [New-PAMRequest](./New-PAMRequest.md) cmdlet.

## PARAMETERS

### -Active
Indicates that that this cmdlet returns roles for which the user has an active request.

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

### -DisplayName
Specifies the display name of the role that will be requested.

```yaml
Type: String
Parameter Sets: DisplayNameSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filter
Specifies a clause to use as a filter.

```yaml
Type: String
Parameter Sets: FilterSet
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

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMRoleForRequest

## NOTES

## RELATED LINKS

[New-PAMRequest](xref:MIMPAM/vlatest/New-PAMRequest.md)

[Microsoft Identity Manager (xref:MIMPAM/vlatest/MIMPAM.md)
