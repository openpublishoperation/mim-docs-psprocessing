---
external help file: Microsoft.IdentityManagement.AdminPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 82817A34-561D-4DCB-BCD4-0EF58B8B32C7
updated_at: 5/17/2017 7:27 PM
ms.date: 5/17/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/Set-PAMUser.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/Set-PAMUser.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/700d23db59d8a09b3e8f23225322beb52d5b1d73/mim-cmdlets/MIMPAM/vlatest/Set-PAMUser.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Set-PAMUser

## SYNOPSIS
Updates a PAM user in the MIM Service and PAM domain.

## SYNTAX

```
Set-PAMUser [-User] <PAMUser> [[-PrivAccountActive] <Boolean>] [[-PrivDisplayName] <String>]
 [[-SourceDisplayName] <String>] [[-PrivDescription] <String>] [[-SourceDescription] <String>]
 [[-SourceDomain] <String>] [[-SourceAccountName] <String>] [[-PrivAccountName] <String>]
 [[-SourcePhoneNumber] <String>] [[-SourceEmailAddress] <String>] [[-PrivPINCode] <String>]
 [[-SourceAccountSID] <String>] [[-Session] <PAMSession>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-PAMUser** cmdlet updates a Privileged Access Management (PAM) user in the Microsoft Identity Manager (MIM) Service and PAM domain. 
The user object in other existing domains is not modified.

## EXAMPLES

### Example 1: Deactivate a user in the PAM domain
```
PS C:\> Set-PAMUser -User (Get-PAMUser -PrivDisplayName "contoso.jen") -PrivAccountActive $False
```

This command changes an attribute of the user with a specified display name in the MIM Service and the PAM domain.

## PARAMETERS

### -PrivAccountActive
Specifies whether the account is active for login in the PAM domain.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivAccountName
Specifies the account name for the user in the PAM domain.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivDescription
Specifies the description of the user account in the MIM Service.

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

### -PrivDisplayName
Specifies the display name of the user in the MIM Service.

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

### -PrivPINCode
Specifies the PIN code if the user is required to complete an MFA challenge during activation requests.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
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
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAccountName
Specifies that the cmdlet overrides the account name of the user in the source domain.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAccountSID
Specifies that the cmdlet overrides the security identifier of the user in the source domain.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDescription
Specifies that the cmdlet overrides the description of the user in the source domain.

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

### -SourceDisplayName
Specifies that the cmdlet overrides the display name of the user in the source domain.

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
Specifies the NetBIOS name of the domain that the user's non-privileged account is located.

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

### -SourceEmailAddress
Specifies that the cmdlet overrides the email address of the user from the source domain.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourcePhoneNumber
Specifies that the cmdlet overrides the telephone number of the user from the source domain.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -User
Specifies the user object to be updated, the cmdlet returns the object through the [Get-PAMUser](./Get-PAMUser.md) cmdlet.

```yaml
Type: PAMUser
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMUser

## NOTES

## RELATED LINKS

[Get-PAMUser](xref:MIMPAM/vlatest/Get-PAMUser.md)

[New-PAMUser](xref:MIMPAM/vlatest/New-PAMUser.md)

[Remove-PAMUser](xref:MIMPAM/vlatest/Remove-PAMUser.md)


