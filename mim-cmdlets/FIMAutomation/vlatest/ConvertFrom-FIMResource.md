---
external help file: Microsoft.ResourceManagement.Automation.dll-Help.xml
online version: 
schema: 2.0.0
updated_at: 5/9/2017 3:47 PM
ms.date: 5/9/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/FIMAutomation/vlatest/ConvertFrom-FIMResource.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/FIMAutomation/vlatest/ConvertFrom-FIMResource.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/bba03e1e0b7bea04619c48b98278723b1a8fc13d/mim-cmdlets/FIMAutomation/vlatest/ConvertFrom-FIMResource.md
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
The ConvertFrom-FIMResource in the Windows PowerShell™ command-line interface serializes into XML resources used elsewhere in the Forefront Identity Manager (FIM) Automation snap-in.
The cmdlet takes ExportObject, ImportObject, or MatchObject instances as input.
With this cmdlet, you can save intermediate work and transfer it among computers.

The cmdlet serializes the resources by using XmlObjectSerializer in Microsoft .NET.
You must use this cmdlet instead ofExport-ClixmlbecauseExport-Clixmldoes not preserve nested and complex types.

To help distinguish ConvertTo-FIMResource from ConvertFrom-FIMResource , remember that you are converting from FIM resources to a file.

For more information about themmseeWindows PowerShell™ cmdlet set see about_FIM.

## EXAMPLES

### ------------------------ EXAMPLE 1 ------------------------
```
$pilot =  Export-FIMConfig  -uri http://localhost:5725/ResourceManagementService -policyConfig $pilot |  ConvertFrom-FIMResource  -file pilot.xml
```

This is a simple example of how you can serialize ExportObject objects to transport across a firewall.

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

### -Objects
{{Fill Objects Description}}

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
{{Fill ObjectType Description}}

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
The resources to serialize.

## OUTPUTS

### None
There is no return value.

## NOTES

## RELATED LINKS

[Export-FIMConfig]()

[Join-FIMConfig]()

[Compare-FIMConfig]()

[Import-FIMResource]()

[ConvertTo-FIMResource]()

[Export-Clixml]()

