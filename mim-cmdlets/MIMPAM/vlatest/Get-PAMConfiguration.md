---
external help file: Microsoft.IdentityManagement.AdminPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: D7C0CC30-3987-4F5B-9789-B10D01C839BF
updated_at: 4/24/2017 10:54 PM
ms.date: 4/24/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/Get-PAMConfiguration.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/Get-PAMConfiguration.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/3e9264276b5141f0a82bd9905d67bb4900c9c2b3/mim-cmdlets/MIMPAM/vlatest/Get-PAMConfiguration.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Get-PAMConfiguration

## SYNOPSIS
Gets PAM scenario configuration settings from the MIM Service.

## SYNTAX

```
Get-PAMConfiguration [<CommonParameters>]
```

## DESCRIPTION
The **Get-PAMConfiguration** cmdlet gets Privileged Access Management (PAM) configuration settings from the Microsoft Identity Manager (MIM) Service.
You can change the configuration settings by calling [Set-PAMConfiguration](./Set-PAMConfiguration.md).

## EXAMPLES

### Example 1: Get PAM configuration
```
PS C:\> Get-PAMConfiguration
```

This command gets the PAM configuration from the MIM service

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMConfiguration

## NOTES

## RELATED LINKS

[Set-PAMConfiguration](xref:MIMPAM/vlatest/Set-PAMConfiguration.md)
