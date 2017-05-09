---
external help file: Microsoft.ResourceManagement.Automation.dll-Help.xml
online version: 
schema: 2.0.0
updated_at: 5/9/2017 3:47 PM
ms.date: 5/9/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/FIMAutomation/vlatest/ConvertTo-FIMResource.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/FIMAutomation/vlatest/ConvertTo-FIMResource.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/bba03e1e0b7bea04619c48b98278723b1a8fc13d/mim-cmdlets/FIMAutomation/vlatest/ConvertTo-FIMResource.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# ConvertTo-FIMResource

## SYNOPSIS
Deserializes FIMResource objects from the given file.

## SYNTAX

```
ConvertTo-FIMResource [-File <String>] [-WhatIf] [-Confirm]
```

## DESCRIPTION
The ConvertTo-FIMResource cmdlet deserializes XML resources used elsewhere in themmseeWindows PowerShell™ cmdlet set.
The cmdlet returns ExportObject, ImportObject, and MatchObjects.
This is the complement cmdlet to ConvertFrom-FIMResource .

The cmdlet deserializes the objects by usingXmlObjectSerializerin Windows .NET.

To help distinguish ConvertTo-FIMResource from ConvertFrom-FIMResource , remember that you are converting to FIM resources from a file.

For more information about themmseeWindows PowerShell™ cmdlet set see about_FIM.

## EXAMPLES

### ------------------------ EXAMPLE 1 ------------------------
```
$pilot =  ConvertTo-FIMResource  -file pilot.xml $matches =  Join-FIMConfig  -source $pilot -target $production -defaultJoin "DisplayName"
```

This is a simple example of how you can deserialize ExportObject instances that were serialized on another system.

## PARAMETERS

### -Confirm
Prompts you for confirmation before running the cmdlet.

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

### -File
{{Fill File Description}}

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

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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

## INPUTS

### None
This cmdlet takes no input.

## OUTPUTS

### FIMResource
The return type could be ImportObject\[\], ExportObject\[\], or MatchObject\[\], depending on which type is stored in the file.
You only get back homogeneous types from this deserialization.

## NOTES

## RELATED LINKS

[Export-FIMConfig]()

[Join-FIMConfig]()

[Compare-FIMConfig]()

[Import-FIMResource]()

[ConvertFrom-FIMResource]()

[Import-Clixml]()

