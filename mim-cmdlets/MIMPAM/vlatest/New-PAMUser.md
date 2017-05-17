---
external help file: Microsoft.IdentityManagement.AdminPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 82EDF13E-E87C-487E-A154-CEB4CC0E8622
updated_at: 5/17/2017 7:27 PM
ms.date: 5/17/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/New-PAMUser.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MIMPAM/vlatest/New-PAMUser.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/700d23db59d8a09b3e8f23225322beb52d5b1d73/mim-cmdlets/MIMPAM/vlatest/New-PAMUser.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# New-PAMUser

## SYNOPSIS
Creates a PAM user in the MIM Service and also a new user in the PAM Active Directory domain corresponding to an existing user in a source domain.

## SYNTAX

```
New-PAMUser [-SourceDomain] <String> [-SourceAccountName] <String> [[-PrivAccountName] <String>]
 [[-PrivPassword] <SecureString>] [[-Credentials] <PSCredential>] [-PrivOnly] [[-Container] <String>]
 [[-Session] <PAMSession>] [<CommonParameters>]
```

## DESCRIPTION
The **New-PAMUser** cmdlet creates a Privileged Access Management (PAM) user in the Microsoft Identity Manager (MIM) Service.
This user can then become a candidate assigned to one or more PAM Roles.

## EXAMPLES

### Example 1: Create a user in the PAM domain corresponding to an existing user in a domain
```
PS C:\> New-PAMUser -SourceDomain "CONTOSO.LOCAL" -SourceAccountName "PFuller"
```

This command creates a user in the PAM domain corresponding to an existing user PFuller in the CONTOSO.LOCAL domain.
You can use the return value as an argument to the *Candidates* parameter of the [New-PAMRole](./New-PAMRole.md) cmdlet.

### Example 2: Create a user on a single domain based on an existing user
```
PS C:\> New-PAMUser -PrivOnly -SourceDomain "PRIV.CONTOSO.LOCAL" -SourceAccountName "PF Admin"
```

This command assumes a user exists in the PAM domain named PRIV.CONTOSO.LOCAL but does not exist in any other domain.
The user record is created only in the MIM Service since the -*PrivOnly* parameter is specified.
The return value can be used as an argument to the *Candidates* parameter of the **New-PAMRole** cmdlet, particularly if the *Privileges* parameter of that cmdlet contains one or more group objects returned by **New-PAMGroup** with the *PrivOnly* parameter.

## PARAMETERS

### -Container
Specifies an alternate container to create the user in the PAM domain.

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

### -Credentials
Specifies credentials to authenticate to the domain where the existing user is located.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivAccountName
Specifies the privileged account name.
If you don't specify a privileged account name, this cmdlet automatically generates one from the configuration parameters and the source account name.

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

### -PrivOnly
Indicates that the user exists already in the PAM domain and does not create a new user in that domain.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivPassword
Specifies the initial password for the new Active Directory user in the PAM domain.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
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
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAccountName
Specifies the account name of the user in the source domain.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDomain
Specifies the NetBIOS name of the domain in which the existing user is located.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
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

[Remove-PAMUser](xref:MIMPAM/vlatest/Remove-PAMUser.md)

[Set-PAMUser](xref:MIMPAM/vlatest/Set-PAMUser.md)

[New-PAMGroup](xref:MIMPAM/vlatest/New-PAMGroup.md)

[New-PAMRole](xref:MIMPAM/vlatest/New-PAMRole.md)


