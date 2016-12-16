---
external help file: MIMPAM_Cmdlets.xml
online version: d41947c3-21de-4585-824d-b164891fc6d7
schema: 2.0.0
ms.assetid: D68A83DC-0EA8-4405-AD1F-C55E3ADE5AE0
updated_at: 12/16/2016 10:21 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/MicrosoftIdentityManager/vlatest/Close-PAMRequestForControl.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/MicrosoftIdentityManager/vlatest/Close-PAMRequestForControl.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/5d96fa08a7ab9495ea82f55bde05b621f03e62cc/MicrosoftIdentityManager/vlatest/Close-PAMRequestForControl.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# Close-PAMRequestForControl

## SYNOPSIS
Cancels current PAM activation requests from other users.

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Close-PAMRequestForControl [-All] [-Force]
```

### UNNAMED_PARAMETER_SET_2
```
Close-PAMRequestForControl [-Role] <PAMRole> [-Force]
```

### UNNAMED_PARAMETER_SET_3
```
Close-PAMRequestForControl [-User] <PAMUser> [-Force]
```

### UNNAMED_PARAMETER_SET_4
```
Close-PAMRequestForControl [-Request] <PAMRequest> [-Force]
```

## DESCRIPTION
The **Close-PAMRequestForControl** cmdlet cancels current Privileged Access Management (PAM) activation requests.
One of the All, Request, Role, or User parameters can be specified.

## EXAMPLES

### Example 1: Close requests from a specific user
```
PS C:\>Close-PAMRequestForControl -User (Get-PAMUser -PrivDisplayName "contoso.Jen")
```

This command closes all requests a specified user made.

## PARAMETERS

### -All
Indicates that all active requests are closed if the *Request*, *Role*, or *User* parameters are not specified.

```yaml
Type: SwitchParameter
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
Forces the command to run without asking for user confirmation.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Request
Specifies an object returned by an earlier call to Get-PAMRequest.

```yaml
Type: PAMRequest
Parameter Sets: UNNAMED_PARAMETER_SET_4
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True(ByValue)
Accept wildcard characters: False
```

### -Role
Specifies an object returned by an earlier call to Get-PAMRole.

```yaml
Type: PAMRole
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True(ByValue)
Accept wildcard characters: False
```

### -User
Specifies an object returned by an earlier call to Get-PAMUser.

```yaml
Type: PAMUser
Parameter Sets: UNNAMED_PARAMETER_SET_3
Aliases: 

Required: True
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

[Get-PAMRequest](xref:vlatest/Get-PAMRequest.md)

[Get-PAMRole](xref:vlatest/Get-PAMRole.md)

[Get-PAMUser](xref:vlatest/Get-PAMUser.md)

[Microsoft Identity Manager (xref:vlatest/MIMPAM.md)

