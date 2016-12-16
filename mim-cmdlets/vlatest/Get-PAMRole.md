---
external help file: MIMPAM_Cmdlets.xml
online version: 0332854c-eb3a-4ea8-bfec-a72618778663
schema: 2.0.0
ms.assetid: 0BAAE78C-6BB9-41C5-B0CC-76A85AA90A8A
updated_at: 12/16/2016 10:21 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/MicrosoftIdentityManager/vlatest/Get-PAMRole.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/MicrosoftIdentityManager/vlatest/Get-PAMRole.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/5d96fa08a7ab9495ea82f55bde05b621f03e62cc/MicrosoftIdentityManager/vlatest/Get-PAMRole.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# Get-PAMRole

## SYNOPSIS
Gets PAM roles from the MIM Service.

## SYNTAX

```
Get-PAMRole [[-DisplayName] <String>] [[-Session] <PAMSession>] [-Active] [[-Filter] <String>]
```

## DESCRIPTION
The **Get-PAMRole** cmdlet gets Privileged Access Management (PAM) roles from the Microsoft Identity Manager (MIM) Service.

## EXAMPLES

### Example 1: Retrieve a single PAM role
```
PS C:\>$Role = Get-PAMRole -DisplayName "IT"
```

This command retrieves a single PAM role with a specified display name from the MIM Service.

## PARAMETERS

### -Active
Indicates that this cmdlet gets roles with activation requests that are currently active.

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

### -DisplayName
Specifies a matching value for the DisplayName attribute of a PAM role resource in the MIM Service.

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

### -Filter
Specifies a clause to use as a filter.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Session
Specifies a session with the PAM domain and the MIM Service.

```yaml
Type: PAMSession
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMRole

## NOTES

## RELATED LINKS

[New-PAMRole](xref:vlatest/New-PAMRole.md)

[Remove-PAMRole](xref:vlatest/Remove-PAMRole.md)

[Set-PAMRole](xref:vlatest/Set-PAMRole.md)

[Microsoft Identity Manager (xref:vlatest/MIMPAM.md)

