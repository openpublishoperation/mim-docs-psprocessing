---
external help file: Microsoft.ResourceManagement.Automation.dll-Help.xml
online version: 
schema: 2.0.0
updated_at: 5/17/2017 2:42 AM
ms.date: 5/17/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/FIMAutomation/vlatest/ConvertTo-FIMResource.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/FIMAutomation/vlatest/ConvertTo-FIMResource.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/b087c1fa22e293ca887d71e98791a50333e0c2ab/mim-cmdlets/FIMAutomation/vlatest/ConvertTo-FIMResource.md
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
The **ConvertTo-FIMResource** cmdlet deserializes XML resources used elsewhere in themmseeWindows PowerShell™ cmdlet set.
The cmdlet returns ExportObject, ImportObject, and MatchObjects.
This is the complement cmdlet to the **ConvertFrom-FIMResource** cmdlet.

The cmdlet deserializes the objects by usingXmlObjectSerializerin Windows .NET.

To help distinguish **ConvertTo-FIMResource** from **ConvertFrom-FIMResource**, remember that you are converting to FIM resources from a file.


## EXAMPLES

### Example 1: Deserialize an ExportObject
```
$Pilot =  ConvertTo-FIMResource  -File pilot.xml $Matches =  Join-FIMConfig  -Source $Pilot -Target $Production -defaultJoin "DisplayName"
```

This command shows how you can deserialize ExportObject instances that were serialized on another system. The command stores the result to the variable named $Pilot.

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
Specifies the filename that this cmdlet deserializes.

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

[Compare-FIMConfig](Compare-FIMConfig.md)

[ConvertFrom-FIMResource](xref:FIMAutomation/vlatest/ConvertFrom-FIMResource.md)

[Export-FIMConfig](xref:FIMAutomation/vlatest/Export-FIMConfig.md)

[Import-FIMResource](Import-FIMResource.md)

[Join-FIMConfig](xref:FIMAutomation/vlatest/Join-FIMConfig.md)
