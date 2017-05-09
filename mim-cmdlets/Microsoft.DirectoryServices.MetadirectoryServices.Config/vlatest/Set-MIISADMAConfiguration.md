---
external help file: Microsoft.DirectoryServices.MetadirectoryServices.Config.dll-Help.xml
online version: 
schema: 2.0.0
updated_at: 5/9/2017 3:47 PM
ms.date: 5/9/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/Microsoft.DirectoryServices.MetadirectoryServices.Config/vlatest/Set-MIISADMAConfiguration.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/Microsoft.DirectoryServices.MetadirectoryServices.Config/vlatest/Set-MIISADMAConfiguration.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/bba03e1e0b7bea04619c48b98278723b1a8fc13d/mim-cmdlets/Microsoft.DirectoryServices.MetadirectoryServices.Config/vlatest/Set-MIISADMAConfiguration.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Set-MIISADMAConfiguration

## SYNOPSIS
Sets the Microsoft Identity Integration Server (MIIS) SourceAD management agent configuration.

## SYNTAX

```
Set-MIISADMAConfiguration [-MAName] <String> -Credentials <PSCredential> -Forest <String> [-Container <String>]
 [-Partitions <String>] [-WarningAction <ActionPreference>] [-WarningVariable <String>] [-WhatIf] [-Confirm]
```

## DESCRIPTION
This cmdlet modifies the MIIS SourceAD management agent configuration to include the credentials provided and the target Active Directory forest, and it reconfigures the agent to sync all containers in all domains of the forest.

## EXAMPLES

### --------------  EXAMPLE 1 --------------
```
Set-MIISADMAConfiguration -MAName: "SourceAD" -Forest:"contoso.com" -Credential: <pscredential object>
```

### --------------  EXAMPLE 2 --------------
```
Set-MIISADMAConfiguration -MAName "SourceAD"
```

Configure the SourceAD management agent.

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
Credentials for authenticating with Active Directory.
Credentials must have replication permissions in Active Directory.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Container
The distinguished name of the container to synchronize

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Forest
The DNS name of the root domain of the forest that you want to connect to.

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

### -Partitions
{{Fill Partitions Description}}

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Unkown]()

