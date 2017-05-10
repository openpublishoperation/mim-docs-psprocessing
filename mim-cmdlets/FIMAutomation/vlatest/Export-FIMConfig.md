---
external help file: Microsoft.ResourceManagement.Automation.dll-Help.xml
online version: http://technet.microsoft.com/en-us/library/dd315352.aspx
schema: 2.0.0
updated_at: 5/9/2017 3:47 PM
ms.date: 5/9/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/FIMAutomation/vlatest/Export-FIMConfig.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/FIMAutomation/vlatest/Export-FIMConfig.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/bba03e1e0b7bea04619c48b98278723b1a8fc13d/mim-cmdlets/FIMAutomation/vlatest/Export-FIMConfig.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Export-FIMConfig

## SYNOPSIS
Extracts configuration resources from the mmsee mmsshort Service.

## SYNTAX

```
Export-FIMConfig [-Uri <String>] [-Credential <PSCredential>] [-AllLocales] [-SchemaConfig] [-PolicyConfig]
 [-PortalConfig] [-OnlyBaseResources] [-CustomConfig <String[]>] [-MessageSize <Int32>]
```

## DESCRIPTION
The Export-FIMConfig cmdlet extracts configuration resources from themmsshortService.
You can use the Export-FIMConfig cmdlet to follow references recursively that are contained in its resources to extract a full representation of the service's configuration.
If a reference points to a resource that is not marked as a configuration resource, the cmdlet downloads the entire representation but it does not follow the non-configuration resource's references.
The cmdlet returns a collection ofExportObjectinstances.

The following are the pre-defined groupings of configuration for export.

Policy Configuration is defined as the following resource types:

ManagementPolicyRule, Set, WorkflowDefinition, EmailTemplate, FilterScope, ActivityInformationConfiguration, Function, SynchronizationRule, SynchronizationFilter

Schema Configuration is defined as the following resource types:

AttributeTypeDescription, BindingDescription, ObjectTypeDescription, ConstantSpecifier, SchemaSupportedLocales

Portal Configuration is defined as the following resource types:

Homepage Configuration, PortalUIConfiguration, Configuration, NavigationBarConfiguration, SearchScopeConfiguration, Configuration, ObjectVisualizationConfiguration

Custom Configuration is defined by the provided XPath filter.
For example /ContosoContact or /Person\[DisplayName='Administrator'\].

For more information about themmseeWindows PowerShell™ cmdlet set see about_FIM.

## EXAMPLES

### ------------------------ EXAMPLE 1 ------------------------
```
$pilot =  Export-FIMConfig  -uri http://localhost:5725/ResourceManagementService -policyConfig -portalConfig
```

This example retrieves basic policy and portal configuration resources.

### ------------------------ EXAMPLE 2 ------------------------
```
$pilot =  Export-FIMConfig  -policyConfig -customConfig ("/ConstosoCustomResource", "/Group")
```

This example retrieves custom resource type and groups in addition to policy configuration.

### ------------------------ EXAMPLE 3 ------------------------
```
$pilot =  Export-FIMConfig  -uri http://pilot:5725/ResourceManagementService -policyConfig $pilot |  ConvertFrom-FIMResource  -file pilot.xml $pilot =  ConvertTo-FIMResource  -file pilot.xml $production =  Export-FIMConfig  -uri http://production:5725/ResourceManagementService -policyConfig $matches =  Join-FIMConfig  -source $pilot -target $production -defaultJoin "DisplayName" $imports = $matches |  Compare-FIMConfig  $imports |  ConvertFrom-FIMResource  -file imports.xml $UndoneImports = $imports |  Import-FIMConfig  -uri http://production:5725/ResourceManagementService
```

This is an end-to-end scenario for migrating configuration from a pilotmmsshortenvironment to a productionmmsshortenvironment.

### ------------------------ EXAMPLE 4 ------------------------
```
$pilot =  Export-FIMConfig  -customConfig "/Request[Target=/Person[DisplayName='Administrator']]" $pilot |  ConvertFrom-FIMResource  -file report.xml
```

This example shows how to extract additional, non-configuration information that may be useful in other scenarios.
Scripters can take theExportObjectinstances from the output and use them for other purposes.
One such purpose is generating reports.

## PARAMETERS

### -AllLocales
{{Fill AllLocales Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
{{Fill Credential Description}}

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

### -CustomConfig
{{Fill CustomConfig Description}}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MessageSize
{{Fill MessageSize Description}}

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

### -OnlyBaseResources
{{Fill OnlyBaseResources Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PolicyConfig
{{Fill PolicyConfig Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PortalConfig
{{Fill PortalConfig Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SchemaConfig
{{Fill SchemaConfig Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Uri
{{Fill Uri Description}}

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

### None

## OUTPUTS

### ExportObject[]

## NOTES

## RELATED LINKS

[about_CommonParameters](http://technet.microsoft.com/en-us/library/dd315352.aspx)

[Join-FIMConfig]()

[Compare-FIMConfig]()

[Import-FIMConfig]()

[ConvertFrom-FIMResource]()

[ConvertTo-FIMResource]()

