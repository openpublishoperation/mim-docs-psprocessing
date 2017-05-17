---
external help file: Microsoft.ResourceManagement.Automation.dll-Help.xml
online version: 
schema: 2.0.0
updated_at: 5/17/2017 2:42 AM
ms.date: 5/17/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/FIMAutomation/vlatest/Compare-FIMConfig.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/FIMAutomation/vlatest/Compare-FIMConfig.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/b087c1fa22e293ca887d71e98791a50333e0c2ab/mim-cmdlets/FIMAutomation/vlatest/Compare-FIMConfig.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Compare-FIMConfig

## SYNOPSIS
Compares the attributes of MatchObject instances and to return an ordered list of changes you can use to make the target system look like the source system.

## SYNTAX

```
Compare-FIMConfig [-MatchObject <MatchObject>] [-WhatIf] [-Confirm]
```

## DESCRIPTION
The **Compare-FIMConfig** cmdlet accepts a list of MatchObject instances and performs an attribute-level comparison of the source and target resources.
The cmdlet returns a list of changes you can use to make to the target system look like the source system.
These changes are represented by ImportObject instances.

The list of changes is guaranteed to be in precedence order.
For example, if a Workflow Definition references an Email Template, then the cmdlet guarantees that the EmailTemplate exists prior to creating the WorkflowDefinition.

All resources are processed generically without regard to object type except for Management Policy Rule (MPR) resources.
These resources are processed in a special way.
The cmdlet guarantees that all dependent sets are updated prior to updating Workflow Definitions.

To avoid a common error: The **Compare-FIMConfig** cmdlet requires that no cycles exist in the configuration references in order to guarantee precedence order.
If a cycle exists, the cmdlet reports an error and does not generate correct changes.
To proceed, remove at least one reference in the cycle.

For more information about themmseeWindows PowerShell™ cmdlet set see about_FIM.

## EXAMPLES

### Example 1: Compare attributes
```
$Imports = $Matches |  Compare-FIMConfig
```

This command displays a simple example of comparison.

Note that you may inspect $Imports prior to committing it to the target system.

### Example 2: Display attribute-level changes
```
$Imports = $Matches |  Compare-FIMConfig  -FriendlyName Write-Host $imports[0].Changes
```

This command displays the specific attribute-level changes that the first ImportObject includes.

Note that inspecting $Imports no longer contains globally unique identifiers (GUIDs) in references, but instead the references are easily readable.

urn:\[ObjectType\]:\[AnchorAttributeName\]:{\[AnchorAttributeValue\]}

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

### -MatchObject
Specifies the object that this cmdlet compares.

```yaml
Type: MatchObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### MatchObject[]
The list of MatchObject instances to compare.

## OUTPUTS

### ImportObject[]
A list of ImportObject instances.
Each ImportObject contains an atomic change to make in the target system so that the target system is semantically equivalent to the source system.

## NOTES

## RELATED LINKS

[Export-FIMConfig](xref:FIMAutomation/vlatest/Export-FIMConfig.md)

[Join-FIMConfig](xref:FIMAutomation/vlatest/Join-FIMConfig.md)

[Import-FIMConfig](xref:FIMAutomation/vlatest/Import-FIMConfig.md)

[ConvertFrom-FIMResource](xref:FIMAutomation/vlatest/ConvertFrom-FIMResource.md)

[ConvertTo-FIMResource](xref:FIMAutomation/vlatest/ConvertTo-FIMResource.md)
