---
external help file: MIMPAM_Cmdlets.xml
online version: c4e502ea-abf6-4cf5-afe8-85d544bda79d
schema: 2.0.0
ms.assetid: D229B024-CB6B-4D9B-9BE8-8FD1C1E5FEBA
updated_at: 12/16/2016 10:21 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/MicrosoftIdentityManager/vlatest/New-PAMRequest.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/MicrosoftIdentityManager/vlatest/New-PAMRequest.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/5d96fa08a7ab9495ea82f55bde05b621f03e62cc/MicrosoftIdentityManager/vlatest/New-PAMRequest.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# New-PAMRequest

## SYNOPSIS
Creates a PAM activation request in the MIM Service.

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
New-PAMRequest [[-Role] <PAMRoleForRequest>] [[-Justification] <String>]
 [[-RequestedTTL] <Nullable [System.TimeSpan]>] [[-RequestedTime] <Nullable [System.DateTime]>]
```

### UNNAMED_PARAMETER_SET_2
```
New-PAMRequest [[-RoleDisplayName] <String>] [[-Justification] <String>]
 [[-RequestedTTL] <Nullable [System.TimeSpan]>] [[-RequestedTime] <Nullable [System.DateTime]>]
```

## DESCRIPTION
The **New-PAMRequest** cmdlet creates a Privileged Access Management (PAM) activation request in the Microsoft Identity Manager (MIM) Service.
You must specify a role, using either the *Role* or *RoleDisplayName* parameters that indicates the security groups to which the user is requesting to be added.

## EXAMPLES

### Example 1: Create a new request for a PAM role
```
PS C:\>New-PAMRequest -role $Role
```

This command creates a new request for a PAM role. 
The variable Role is assumed to have been set by a previous use of the cmdlet Get-PAMRoleForRequest.

## PARAMETERS

### -Justification
Specifies an optional text parameter to be included in the activation request.

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

### -RequestedTime
Specifies an optional delayed start time for the activation.

```yaml
Type: Nullable [System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestedTTL
Specifies an optional override of the time to live (TTL) for the activation request.
If you don't specify this parameter, then the role default TTL is used instead.

```yaml
Type: Nullable [System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Role
Specifies the PAM role in the MIM Service being requested, returned by Get-PAMRoleForRequest.

```yaml
Type: PAMRoleForRequest
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RoleDisplayName
Specifies the display name of the PAM role in the MIM Service being requested.

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True(ByValue)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMRequest

## NOTES

## RELATED LINKS

[Close-PAMRequest](xref:vlatest/Close-PAMRequest.md)

[Get-PAMRequest](xref:vlatest/Get-PAMRequest.md)

[Get-PAMRoleForRequest](xref:vlatest/Get-PAMRoleForRequest.md)

[Microsoft Identity Manager (xref:vlatest/MIMPAM.md)

