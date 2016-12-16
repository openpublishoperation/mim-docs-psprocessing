---
external help file: MIMPAM_Cmdlets.xml
online version: 4066d446-6ee0-4d1c-b4ee-5069e32d9567
schema: 2.0.0
ms.assetid: 82817A34-561D-4DCB-BCD4-0EF58B8B32C7
updated_at: 12/16/2016 10:39 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/Set-PAMUser.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/Set-PAMUser.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/91e8680653c5bbea5afddb262c8a143482b14fd5/mim-cmdlets/MicrosoftIdentityManager/vlatest/Set-PAMUser.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# Set-PAMUser

## SYNOPSIS
Updates a PAM user in the MIM Service and PAM domain.

## SYNTAX

```
Set-PAMUser [-User] <PAMUser> [[-SourcePhoneNumber] <String>] [[-SourceEmailAddress] <String>]
 [[-PrivPINCode] <String>] [[-SourceAccountSID] <String>] [[-Session] <PAMSession>]
 [[-PrivAccountActive] <Boolean]>] [[-PrivDisplayName] <String>] [[-SourceDisplayName] <String>]
 [[-PrivDescription] <String>] [[-SourceDescription] <String>] [[-SourceDomain] <String>]
 [[-SourceAccountName] <String>] [[-PrivAccountName] <String>]
```

## DESCRIPTION
The **Set-PAMUser** cmdlet updates a Privileged Access Management (PAM) user in the Microsoft Identity Manager (MIM) Service and PAM domain. 
The user object in other existing domains is not modified.

## EXAMPLES

### Example 1: Deactivate a user in the PAM domain
```
PS C:\>Set-PAMUser -User (Get-PAMUser -PrivDisplayName "contoso.jen") -PrivAccountActive $False
```

This command changes an attribute of the user with a specified display name in the MIM Service and the PAM domain.

## PARAMETERS

### -PrivAccountActive
Specifies whether the account is active for login in the PAM domain.

```yaml
Type: Boolean]
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
Specifies the user object to be updated, the cmdlet returns the object through the Get-PAMUser cmdlet.

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

## INPUTS

## OUTPUTS

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMUser

## NOTES

## RELATED LINKS

[Get-PAMUser](xref:MicrosoftIdentityManager/vlatest/Get-PAMUser.md)

[New-PAMUser](xref:MicrosoftIdentityManager/vlatest/New-PAMUser.md)

[Remove-PAMUser](xref:MicrosoftIdentityManager/vlatest/Remove-PAMUser.md)



