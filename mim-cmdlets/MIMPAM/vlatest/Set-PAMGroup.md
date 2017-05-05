---
external help file: Microsoft.IdentityManagement.AdminPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 597F16FD-39FB-45EA-A65B-3973C3E18DA2
updated_at: 4/24/2017 10:54 PM
ms.date: 4/24/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/MIMPAM/vlatest/Set-PAMGroup.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/MIMPAM/vlatest/Set-PAMGroup.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/3e9264276b5141f0a82bd9905d67bb4900c9c2b3/mim-cmdlets/MIMPAM/vlatest/Set-PAMGroup.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Set-PAMGroup

## SYNOPSIS
Updates a PAM group in the MIM Service.

## SYNTAX

```
Set-PAMGroup [-Group] <PAMGroup> [[-SourceAccountName] <String>] [[-SourceDomain] <String>]
 [[-SourceAccountSID] <String>] [[-PrivAccountName] <String>] [[-PrivDisplayName] <String>]
 [[-PrivDescription] <String>] [[-Active] <Boolean>] [[-Session] <PAMSession>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-PAMGroup** cmdlet updates a Privileged Access Management (PAM) group in the Microsoft Identity Manager (MIM) Service.
The group in other existing domains is not modified.

## EXAMPLES

### Example 1: Change an attribute of a group
```
PS C:\> Set-PAMGroup -Group (Get-PAMGroup -PrivDisplayName "contoso.corpadmins") -PrivDescription "For IT Use"
```

This command changes the description of a group with a specified display name in the MIM Service and the PAM domain.

## PARAMETERS

### -Active
Specifies whether the group is active for activation.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Group
Specifies the group to be updated, returned by [Get-PAMGroup](./Get-PAMGroup.md).

```yaml
Type: PAMGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PrivAccountName
Specifies the account name of the group in the PAM domain.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivDescription
Specifies the description of the group in the PAM domain.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivDisplayName
Specifies the display name of the group in the PAM domain.

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

### -Session
Specifies the session with the PAM domain and MIM Service.

```yaml
Type: PAMSession
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAccountName
Specifies that this cmdlet overrides the account name of the group in the source domain.

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

### -SourceAccountSID
Specifies that this cmdlet overrides the security identifier of the group in the source domain.

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

### -SourceDomain
Specifies the NetBIOS name of the domain in which the source group is located.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMGroup

## NOTES

## RELATED LINKS

[Get-PAMGroup](xref:MIMPAM/vlatest/Get-PAMGroup.md)

[New-PAMGroup](xref:MIMPAM/vlatest/New-PAMGroup.md)

[Remove-PAMGroup](xref:MIMPAM/vlatest/Remove-PAMGroup.md)

[Microsoft Identity Manager (xref:MIMPAM/vlatest/MIMPAM.md)
