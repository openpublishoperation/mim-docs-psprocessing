---
external help file: Microsoft.ResourceManagement.Automation.dll-Help.xml
online version: 
schema: 2.0.0
updated_at: 5/17/2017 2:42 AM
ms.date: 5/17/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/FIMAutomation/vlatest/ConvertFrom-FIMResource.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/FIMAutomation/vlatest/ConvertFrom-FIMResource.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/b087c1fa22e293ca887d71e98791a50333e0c2ab/mim-cmdlets/FIMAutomation/vlatest/ConvertFrom-FIMResource.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# ConvertFrom-FIMResource

## SYNOPSIS
Serializes FIMResource objects and stores them in the given file.

## SYNTAX

```
ConvertFrom-FIMResource [-Objects <BaseObject>] [-ObjectType <String>] [-File <String>] [-WhatIf] [-Confirm]
```

## DESCRIPTION
The **ConvertFrom-FIMResource** cmdlet serializes into XML resources used elsewhere in the Forefront Identity Manager (FIM) Automation snap-in.
The cmdlet takes ExportObject, ImportObject, or MatchObject instances as input.
With this cmdlet, you can save intermediate work and transfer it among computers.

The cmdlet serializes the resources by using XmlObjectSerializer in Microsoft .NET.
You must use this cmdlet instead of **Export-Clixml** because that cmdlet does not preserve nested and complex types.

To help distinguish **ConvertTo-FIMResource** from **ConvertFrom-FIMResource**, remember that you are converting from FIM resources to a file.

## EXAMPLES

### Example 1: Serialize ExportObject objects 
```
$Pilot =  Export-FIMConfig  -Uri http://localhost:5725/ResourceManagementService -PolicyConfig $Pilot |  ConvertFrom-FIMResource  -File pilot.xml
```

This command shows how you can serialize ExportObject objects for transport across a firewall.

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
Specifies the filename that contains the objects that this cmdlet converts.

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

### -Objects
Specifies the objects that this cmdlet converts.

```yaml
Type: BaseObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ObjectType
Specifies the object type.

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

### ExportObject[] | ImportObject[] | MatchObject[]
Specifies the resources that this cmdlet serializes.

## OUTPUTS

### None
There is no return value.

## NOTES

## RELATED LINKS

[Compare-FIMConfig](xref:FIMAutomation/vlatest/Compare-FIMConfig.md)

[ConvertTo-FIMResource](xref:FIMAutomation/vlatest/ConvertTo-FIMResource.md)

[Export-FIMConfig](xref:FIMAutomation/vlatest/Export-FIMConfig.md)

[Import-FIMResource](xref:FIMAutomation/vlatest/Import-FIMResource.md)

[Join-FIMConfig](xref:FIMAutomation/vlatest/Join-FIMConfig.md)
