---
external help file: Microsoft.DirectoryServices.MetadirectoryServices.Config-Help.xml
online version: 
schema: 2.0.0
updated_at: 5/17/2017 7:27 PM
ms.date: 5/17/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/Microsoft.DirectoryServices.MetadirectoryServices.Config/vlatest/Add-MIISADMARunProfileStep.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/Microsoft.DirectoryServices.MetadirectoryServices.Config/vlatest/Add-MIISADMARunProfileStep.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/700d23db59d8a09b3e8f23225322beb52d5b1d73/mim-cmdlets/Microsoft.DirectoryServices.MetadirectoryServices.Config/vlatest/Add-MIISADMARunProfileStep.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Add-MIISADMARunProfileStep

## SYNOPSIS
Adds run profile step to the run profile of Active Directory management agent.

## SYNTAX

```
Add-MIISADMARunProfileStep [-MAName] <String> -ProfileName <String> -StepType <String> -Partition <String>
 [-BatchSize <Int32>] [-PageSize <Int32>] [-TimeLimit <Int32>] [-WarningAction <ActionPreference>]
 [-WarningVariable <String>] [-WhatIf] [-Confirm]
```

## DESCRIPTION
This cmdlet adds run profile step to the run profile of Active Directory management agent.
If run profile does not exist, it will be created.
Management agent should already exist.

## EXAMPLES

### --------------  EXAMPLE 1 --------------
```
Add-MIISADMARunProfileStep -MAName "AD_MA" -Partition "DC=MIMOneBox12R2AD,DC=COM" -StepType "FI" -ProfileName "MyRunProfile"
```

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

### -Partition
Partition which new step should be assigned to

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

### -StepType
Type of the new run profile step.
Possible values (short and long form make the same effect):
				"FI", "FULL IMPORT",
				"FS", "FULL SYNCHRONIZATION",
				"FIFS", "FULL IMPORT AND FULL SYNCHRONIZATION",
				"FIDS", "FULL IMPORT AND DELTA SYNCHRONIZATION",
				"DI", "DELTA IMPORT",
				"DS", "DELTA SYNCHRONIZATION",
				"DIDS", "DELTA IMPORT AND DELTA SYNCHRONIZATION",
				"EXP", "EXPORT"

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

### -ProfileName
Run profile name

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

### -BatchSize
{{Fill BatchSize Description}}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PageSize
{{Fill PageSize Description}}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeLimit
{{Fill TimeLimit Description}}

```yaml
Type: Int32
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



