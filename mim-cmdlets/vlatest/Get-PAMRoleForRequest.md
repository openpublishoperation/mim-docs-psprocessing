---
external help file: MIMPAM_Cmdlets.xml
online version: d229b024-cb6b-4d9b-9be8-8fd1c1e5feba
schema: 2.0.0
ms.assetid: D99CB1FD-186C-422D-90A3-AF61B5E77594
updated_at: 12/16/2016 10:21 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/MicrosoftIdentityManager/vlatest/Get-PAMRoleForRequest.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/MicrosoftIdentityManager/vlatest/Get-PAMRoleForRequest.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/5d96fa08a7ab9495ea82f55bde05b621f03e62cc/MicrosoftIdentityManager/vlatest/Get-PAMRoleForRequest.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# Get-PAMRoleForRequest

## SYNOPSIS
Gets PAM roles from the MIM Service.

## SYNTAX

```
Get-PAMRoleForRequest [[-Filter] <String>] [-Active]
```

## DESCRIPTION
The **Get-PAMRoleForRequest** cmdlet gets Privileged Access Management (PAM) roles from the Microsoft Identity Manager (MIM) Service that the user is authorized to request.

## EXAMPLES

### Example 1: Get all available roles that a user can request
```
PS C:\>Get-PAMRoleForRequest
```

This command displays all available roles a user can request.

### Example 2: Get a list of roles and select a role by name
```
PS C:\>$Role = Get-PAMRoleForRequest | ? { $_.DisplayName -eq "CorpAdmins" }
```

This command gets the list of roles and selects a role named CorpAdmins.
The returned object result can then be provided to the New-PAMRequest cmdlet.

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

### -Filter
Specifies a clause to use as a filter.

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

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMRoleForRequest

## NOTES

## RELATED LINKS

[New-PAMRequest](xref:vlatest/New-PAMRequest.md)

[Microsoft Identity Manager (xref:vlatest/MIMPAM.md)

