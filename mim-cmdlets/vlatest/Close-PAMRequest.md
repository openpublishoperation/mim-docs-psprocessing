---
external help file: MIMPAM_Cmdlets.xml
online version: d99cb1fd-186c-422d-90a3-af61b5e77594
schema: 2.0.0
ms.assetid: C4E502EA-ABF6-4CF5-AFE8-85D544BDA79D
updated_at: 12/16/2016 10:21 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/MicrosoftIdentityManager/vlatest/Close-PAMRequest.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/MicrosoftIdentityManager/vlatest/Close-PAMRequest.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/5d96fa08a7ab9495ea82f55bde05b621f03e62cc/MicrosoftIdentityManager/vlatest/Close-PAMRequest.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# Close-PAMRequest

## SYNOPSIS
Closes the specified user's PAM activation request.

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Close-PAMRequest [[-Role] <PAMRoleForRequest>] [[-Justification] <String>]
```

### UNNAMED_PARAMETER_SET_2
```
Close-PAMRequest [[-RoleDisplayName] <String>] [[-Justification] <String>]
```

### UNNAMED_PARAMETER_SET_3
```
Close-PAMRequest [[-Request] <Microsoft.IdentityManagement.PamCmdlets.Model.PAMRequest>]
```

## DESCRIPTION
The **Close-PAMRequest** cmdlet deactivates one or more of the user's Privileged Access Management (PAM) activation requests.
The *Request*, *Role*, or *RoleDisplayName* parameters must be specified.

## EXAMPLES

### Example 1: Close requests for a specific role
```
PS C:\>Close-PAMRequest -RoleDisplayName "IT"
```

This command closes request the user made earlier for a specific role.

## PARAMETERS

### -Justification
Optional parameter to provide a descriptive string to be recorded with this cancelation.

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_1, UNNAMED_PARAMETER_SET_2
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Request
Specifies the request to be deactivated.

```yaml
Type: Microsoft.IdentityManagement.PamCmdlets.Model.PAMRequest
Parameter Sets: UNNAMED_PARAMETER_SET_3
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True(ByValue)
Accept wildcard characters: False
```

### -Role
Specifies a role that was returned by Get-PAMRoleForRequest and provided to an earlier call to New-PAMRequest.

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
Specifies the display name of the role that was earlier requested for activation.

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

## NOTES

## RELATED LINKS

[Get-PAMRoleForRequest](xref:vlatest/Get-PAMRoleForRequest.md)

[New-PAMRequest](xref:vlatest/New-PAMRequest.md)

[Microsoft Identity Manager (xref:vlatest/MIMPAM.md)

