---
external help file: Microsoft.DirectoryServices.MetadirectoryServices.Config.dll-Help.xml
online version: 
schema: 2.0.0
updated_at: 5/9/2017 3:47 PM
ms.date: 5/9/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/Microsoft.DirectoryServices.MetadirectoryServices.Config/vlatest/Import-MIISServerConfig.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/Microsoft.DirectoryServices.MetadirectoryServices.Config/vlatest/Import-MIISServerConfig.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/bba03e1e0b7bea04619c48b98278723b1a8fc13d/mim-cmdlets/Microsoft.DirectoryServices.MetadirectoryServices.Config/vlatest/Import-MIISServerConfig.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Import-MIISServerConfig

## SYNOPSIS
Server import of management agent files.

## SYNTAX

```
Import-MIISServerConfig [-Path] <String> [-Skip <String>] [-WarningAction <ActionPreference>]
 [-WarningVariable <String>] [-WhatIf] [-Confirm]
```

## DESCRIPTION
This cmdlet imports all of the the Microsoft Online Directory Synchronization Tool management agent configuration XML files and the metaverse  configuration XML from the provided path.
The user should use Set-MIISADMAConfiguration, Set-MIISExtMAConfiguration and Set-MIISECMA2Configuration cmdlets to ensure that the management agents conform to the usage environment.

## EXAMPLES

### --------------  EXAMPLE 1 --------------
```
Import-MIISServerConfig -path: "<path to the configuration XMLs>" -verbose
```

VERBOSE: Metaverse Schema Updated.
            VERBOSE: Management Agent Created: C:\Program Files\Microsoft Online Directory
            Sync\ma\Exch\MA-{1D2C95FB-F61F-45A7-B6D5-F4124D5F7002}.XML
            VERBOSE: Management Agent Created: C:\Program Files\Microsoft Online Directory
            Sync\ma\Exch\MA-{CB7D5198-66E8-49EC-9C0F-406A55FD4317}.XML
            VERBOSE: Metaverse Schema Updated With IAF.

Description-----------

### --------------  EXAMPLE 2 --------------
```
Import-MIISServerConfig -Path "C:\Program Files\Microsoft Online Directory Sync\ma\Exch"
```

This example imports the management agent files from the C:\Program Files\Microsoft Online Directory Sync\ma\Exch directory.
The directory specified must contain the XML file that defines the default management agents and the metaverse schema.

## PARAMETERS

### -Path
The directory that contains the XML that defines the default management agents and the metaverse  schema

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

### -Skip
The list of management agents which have not to be imported, delimited by ; symbol

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

## INPUTS

## OUTPUTS

## NOTES
The files imported are shipped templates.
The user should use Set-MIISADMAConfiguration, Set-MIISExtMAConfiguration, and Set-MIISECMA2Configuration cmdlets to ensure that the Management Agents conform to the usage environment.

## RELATED LINKS

[Unkown]()

