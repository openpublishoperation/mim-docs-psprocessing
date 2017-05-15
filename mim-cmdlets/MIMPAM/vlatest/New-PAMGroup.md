---
external help file: Microsoft.IdentityManagement.AdminPamCmdlets.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: F6C3AAA3-E9D1-4CFF-B5A9-A937C5D61AF0
updated_at: 5/15/2017 3:45 PM
ms.date: 5/15/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/MIMPAM/vlatest/New-PAMGroup.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/MIMPAM/vlatest/New-PAMGroup.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/9b28322895cedef17814e137aefa9d68fe2293a6/mim-cmdlets/MIMPAM/vlatest/New-PAMGroup.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# New-PAMGroup

## SYNOPSIS
Creates a representation of a security group in the MIM Service and a foreign principal group in Active Directory.

## SYNTAX

```
New-PAMGroup [-SourceGroupName] <String> [-SourceDomain] <String> [[-Credentials] <PSCredential>]
 [[-SourceDC] <String>] [-PrivOnly] [[-Container] <String>] [[-Session] <PAMSession>] [<CommonParameters>]
```

## DESCRIPTION
The **New-PAMGroup** cmdlet creates a representation of a group in the Microsoft Identity Manager (MIM) Service.
Also, unless the *PrivOnly* parameter is specified, the **New-PAMGroup** cmdlet creates a foreign principal group in the Privileged Access Management (PAM) domain that has the same security identifier as an existing source security group.

## EXAMPLES

### Example 1: Create a new foreign principal group in the Active Directory forest PAM domain
```
PS C:\> $PAMGroup = New-PAMGroup -SourceGroupName "CorpAdmins" -SourceDomain "CORP" -SourceDC "CORPDC" -Credentials $Cred -CloneSIDHistory 1
```

This command creates a new foreign principal group in the Active Directory forest privileged access management (PAM) domain.
The security ID (SID) of the group will be copied from the group CorpAdmins in the domain CORP. 
The SIDHistory mechanism will be used to copy the SID from the originating Windows Server CORPDC. 
The credentials in the variable $Cred, obtained from a previous call to get-credential, will be used to authenticate to the CORPDC.
The returned data structure can be used as an argument to the [New-PAMRole](./New-PAMRole.md) cmdlet.

### Example 2: Create a representation in the MIM Service for a security group which already exists in the PAM domain
```
PS C:\> $PAMGroup = New-PAMGroup -PrivOnly -SourceDomain "priv.contoso.local" -SourceGroupName "Domain Admins"
```

This command creates a representation in the MIM Service for a security group which already exists in the PAM domain when the *PrivOnly* parameter is specified.
The value of the *SourceDomain* parameter must be the same as the PAM domain name.

## PARAMETERS

### -Container
Specifies an alternate container to create the group in the PAM domain.

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

### -Credentials
Specifies the credentials to authenticate as an administrator to the domain where the source group is located.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivOnly
Indicates the group already exists in the PAM domain, but not in MIM, and is not based on any existing group in a separate existing forest.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
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
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDC
Specifies the NetBIOS name of the Windows Server with the Active Directory Domain Services role in the source domain.

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
Specifies the NetBIOS name of the domain in which the existing group is located.

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

### -SourceGroupName
Specifies the account name of the security group in the source domain.

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

### Microsoft.IdentityManagement.PamCmdlets.Model.PAMGroup

## NOTES

## RELATED LINKS

[Get-PAMGroup](xref:MIMPAM/vlatest/Get-PAMGroup.md)

[Remove-PAMGroup](xref:MIMPAM/vlatest/Remove-PAMGroup.md)

[Set-PAMGroup](xref:MIMPAM/vlatest/Set-PAMGroup.md)

[Microsoft Identity Manager (xref:MIMPAM/vlatest/MIMPAM.md)
