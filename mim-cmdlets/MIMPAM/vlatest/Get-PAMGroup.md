---
external help file: Microsoft.IdentityManagement.AdminPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 811219BB-DF83-431F-AE84-812B137BAC7A
updated_at: 4/24/2017 10:54 PM
ms.date: 4/24/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/MIMPAM/vlatest/Get-PAMGroup.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/MIMPAM/vlatest/Get-PAMGroup.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/3e9264276b5141f0a82bd9905d67bb4900c9c2b3/mim-cmdlets/MIMPAM/vlatest/Get-PAMGroup.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Get-PAMGroup

## SYNOPSIS
Gets groups from the MIM Service that are intended for PAM activation.

## SYNTAX

```
Get-PAMGroup [[-SourceAccountName] <String>] [[-PrivAccountName] <String>] [[-PrivDisplayName] <String>]
 [[-Filter] <String>] [[-Session] <PAMSession>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-PAMGroup** cmdlet gets groups from the Microsoft Identity Manager (MIM) Service that are intended for Privileged Access Management (PAM) activation.

## EXAMPLES

### Example 1: Get all groups in the MIM Service for PAM
```
PS C:\> $PamGroup = Get-PAMGroup
```

This command gets all groups in the MIM Service for PAM.

## PARAMETERS

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

### -PrivAccountName
Specifies the matching value for the account name of the group in the PAM domain.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivDisplayName
Specifies the matching value for the DisplayName attribute of a group resource in the MIM Service.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Session
Specifies a session with the PAM domain and MIM Service.

```yaml
Type: PAMSession
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAccountName
Specifies the matching value for the account name of the group in the source domain.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMGroup

## NOTES

## RELATED LINKS

[New-PAMGroup](xref:MIMPAM/vlatest/New-PAMGroup.md)

[Remove-PAMGroup](xref:MIMPAM/vlatest/Remove-PAMGroup.md)

[Set-PAMGroup](xref:MIMPAM/vlatest/Set-PAMGroup.md)

[Microsoft Identity Manager (xref:MIMPAM/vlatest/MIMPAM.md)
