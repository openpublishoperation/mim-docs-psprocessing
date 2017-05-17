---
external help file: Microsoft.ResourceManagement.Automation.dll-Help.xml
online version: 
schema: 2.0.0
updated_at: 5/17/2017 2:42 AM
ms.date: 5/17/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/FIMAutomation/vlatest/Join-FIMConfig.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/FIMAutomation/vlatest/Join-FIMConfig.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/b087c1fa22e293ca887d71e98791a50333e0c2ab/mim-cmdlets/FIMAutomation/vlatest/Join-FIMConfig.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Join-FIMConfig

## SYNOPSIS
Joins two lists of ExportObject instances by using join criteria.

## SYNTAX

```
Join-FIMConfig [-Target <ExportObject[]>] [-Source <ExportObject[]>] [-Join <Hashtable>]
 [-DefaultJoin <String>] [-WhatIf] [-Confirm]
```

## DESCRIPTION
The **Join-FIMConfig** cmdlet accepts two lists of ExportObject instances and joins them into MatchObject instances.

The cmdlet performs the join by using criteria specified as arguments to the cmdlet.
The join criteria are specific attributes to compare by using case-sensitive matching.

You may specify individual join criteria for each resource type.
For example, you may join on EmployeeID for Person and MailNickname for Groups.

You can also use multiple attributes as join criteria.
For example, you can join ConstantSpecifier resources on both the DisplayName and Value.

No default join criteria are provided.
To ensure that this tool joins on attributes or collections of attributes that are unique in your organization, you must specify the join criteria.

For migrating resources to an empty environment, it is often convenient to use ObjectID as the default join criteria.

To preserve joins or to join resources manually, you can provide MatchObject instances in the previous join parameter.
These MatchObject instances are used prior to join criteria in matching resources.


## EXAMPLES

### Example 1: Join all resources by Display name
```
$Matches =  Join-FIMConfig  -Source $Pilot -Target $Production -DefaultJoin "DisplayName"
```

This command joins all resources by DisplayName.

Note that $Pilot and $Production are different collections.

### Example 2:  Join all resources by properties
```
$Join = @{"Person" = "EmployeeID DisplayName"; "Group" = "Email DisplayName"} $Matches =  Join-FIMConfig  -Source $Pilot -Target $Production -Join $Join -DefaultJoin "DisplayName"
```

This command joins Person resources by EmployeeID, Group resources by Email and DisplayName (because DisplayName is not often unique), and everything else by display name.

Notice that you can join specific object types by multiple attributes.
In this example, Group is joined by using Email and DisplayName.
Also notice that explicit joins for object types specified in join take precedence over defaultJoin.
We recommend that you use EmployeeID or similar attributes for Person resources because DisplayName often is not sufficiently unique.

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

### -DefaultJoin


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

### -Join


```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Source


```yaml
Type: ExportObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Target


```yaml
Type: ExportObject[]
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

### MatchObject[]
A list of MatchObject instances.
Each MatchObject contains the full representation of the FIM object from each the source and target FIM services.

## NOTES

## RELATED LINKS

[Export-FIMConfig](xref:FIMAutomation/vlatest/Export-FIMConfig.md)

[Compare-FIMConfig](Compare-FIMConfig.md)

[Import-FIMConfig](xref:FIMAutomation/vlatest/Import-FIMConfig.md)

[ConvertFrom-FIMResource](ConvertFrom-FIMResource.md)

[ConvertTo-FIMResource](ConvertTo-FIMResource.md)
