---
external help file: MIMPAM_Cmdlets.xml
online version: 82edf13e-e87c-487e-a154-ceb4cc0e8622
schema: 2.0.0
ms.assetid: 4066D446-6EE0-4D1C-B4EE-5069E32D9567
updated_at: 12/16/2016 10:24 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/Get-PAMUser.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/Get-PAMUser.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/d76fe71a336b890697ca5b79f29d35c57acf4cc6/mim-cmdlets/MicrosoftIdentityManager/vlatest/Get-PAMUser.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# Get-PAMUser

## SYNOPSIS
Gets users who can request activation from the MIM Service.

## SYNTAX

```
Get-PAMUser [[-SourceDisplayName] <String>] [[-SourceDomain] <String>] [[-SourceAccountName] <String>]
 [[-PrivDisplayName] <String>] [[-Session] <PAMSession>] [[-Filter] <String>]
```

## DESCRIPTION
The **Get-PAMUser** cmdlet gets users from the Microsoft Identity Manager (MIM) Service that optionally match filter conditions. 
This array of users can be provided to the New-PAMRole or Set-PAMRole cmdlet assigned as candidate users.

## EXAMPLES

### Example 1: Get users in the MIM Service by name
```
PS C:\>$Users = Get-PAMUser -SourceDisplayName "PFuller"
```

This command gets users in the MIM Service that have the display name attribute in the source domain with a value of PFuller.

## PARAMETERS

### -Filter
Specifies a clause to use as a filter.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivDisplayName
Specifies the matching value for the DisplayName of the user in the PAM domain.

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
Specifies the session with the PAM domain and MIM Service.

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
Specifies the matching value for the AccountName attribute of a user resource in MIM Service.

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

### -SourceDisplayName
Specifies the matching value for DisplayName attribute of a user resource in MIM Service.

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

### -SourceDomain
Specifies the matching value for the Domain attribute of a user resource in MIM Service.

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

## INPUTS

### 
Specifies a clause to use as a filter.

## OUTPUTS

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMUser

## NOTES

## RELATED LINKS

[New-PAMUser](xref:MicrosoftIdentityManager/vlatest/New-PAMUser.md)

[Remove-PAMUser](xref:MicrosoftIdentityManager/vlatest/Remove-PAMUser.md)

[Set-PAMUser](xref:MicrosoftIdentityManager/vlatest/Set-PAMUser.md)

[Microsoft Identity Manager (xref:MicrosoftIdentityManager/vlatest/MIMPAM.md)

