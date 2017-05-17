---
external help file: Microsoft.DirectoryServices.MetadirectoryServices.Config.dll-Help.xml
online version: 
schema: 2.0.0
updated_at: 5/17/2017 7:27 PM
ms.date: 5/17/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/Microsoft.DirectoryServices.MetadirectoryServices.Config/vlatest/Set-MIISECMA2Configuration.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/Microsoft.DirectoryServices.MetadirectoryServices.Config/vlatest/Set-MIISECMA2Configuration.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/700d23db59d8a09b3e8f23225322beb52d5b1d73/mim-cmdlets/Microsoft.DirectoryServices.MetadirectoryServices.Config/vlatest/Set-MIISECMA2Configuration.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Set-MIISECMA2Configuration

## SYNOPSIS
Sets configuration details for the extensible connectivity management agent 2.0.

## SYNTAX

```
Set-MIISECMA2Configuration [-MAName] <String> -ParameterUse <String> [-Credentials <PSCredential>]
 [-WarningAction <ActionPreference>] [-WarningVariable <String>] [-WhatIf] [-Confirm]
```

## DESCRIPTION
The Set-MIISECMA2Configuration cmdlet modifies the Microsoft Identity Integration Server (MIIS) extensible connectivity management agent 2.0 to include the credentials that are used to synchronize accounts and to update the domains that are synchronized.

## EXAMPLES

### --------------  EXAMPLE 1 --------------
```
Set-MIISECMA2Configuration -MAName:"TargetWebService" -ConnectTo:"https://provisioning.microsoftonline.com" -Credentials:"<PSCredential object>"
```

Configure ConnectTo and Credentials parameters of the management agent.

## PARAMETERS

### -MAName
The name of the management agent to update.
Get this name from the MIIS tool.

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

### -Credentials
Credentials for authenticating with the custom container.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WarningAction
@{Text=}

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: wa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WarningVariable
@{Text=}

```yaml
Type: String
Parameter Sets: (All)
Aliases: wv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
@{Text=}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
@{Text=}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParameterUse
{{Fill ParameterUse Description}}

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS



