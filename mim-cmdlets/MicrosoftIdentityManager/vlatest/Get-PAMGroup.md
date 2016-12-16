---
external help file: MIMPAM_Cmdlets.xml
online version: f6c3aaa3-e9d1-4cff-b5a9-a937c5d61af0
schema: 2.0.0
ms.assetid: 811219BB-DF83-431F-AE84-812B137BAC7A
updated_at: 12/16/2016 10:39 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/Get-PAMGroup.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/Get-PAMGroup.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/91e8680653c5bbea5afddb262c8a143482b14fd5/mim-cmdlets/MicrosoftIdentityManager/vlatest/Get-PAMGroup.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# Get-PAMGroup

## SYNOPSIS
Gets groups from the MIM Service that are intended for PAM activation.

## SYNTAX

```
Get-PAMGroup [[-SourceAccountName] <System.String>] [[-PrivAccountName] <System.String>]
 [[-PrivDisplayName] <System.String>] [[-Filter] <String>] [[-Session] <PAMSession>]
```

## DESCRIPTION
The **Get-PAMGroup** cmdlet gets groups from the Microsoft Identity Manager (MIM) Service that are intended for Privileged Access Management (PAM) activation.

## EXAMPLES

### Example 1: Get all groups in the MIM Service for PAM
```
PS C:\>$PamGroup = Get-PAMGroup
```

This command returns all groups in the MIM Service for PAM.

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
Type: System.String
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
Type: System.String
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
Type: System.String
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

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMGroup

## NOTES

## RELATED LINKS

[New-PAMGroup](xref:MicrosoftIdentityManager/vlatest/New-PAMGroup.md)

[Remove-PAMGroup](xref:MicrosoftIdentityManager/vlatest/Remove-PAMGroup.md)

[Set-PAMGroup](xref:MicrosoftIdentityManager/vlatest/Set-PAMGroup.md)



