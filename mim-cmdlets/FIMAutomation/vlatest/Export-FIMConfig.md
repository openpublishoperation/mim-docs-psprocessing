---
external help file: Microsoft.ResourceManagement.Automation.dll-Help.xml
online version: http://technet.microsoft.com/en-us/library/dd315352.aspx
schema: 2.0.0
updated_at: 5/17/2017 2:42 AM
ms.date: 5/17/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/FIMAutomation/vlatest/Export-FIMConfig.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/FIMAutomation/vlatest/Export-FIMConfig.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/b087c1fa22e293ca887d71e98791a50333e0c2ab/mim-cmdlets/FIMAutomation/vlatest/Export-FIMConfig.md
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
The **Export-FIMConfig** cmdlet extracts configuration resources from themmsshortService.
You can use the **Export-FIMConfig** cmdlet to follow references recursively that are contained in its resources to extract a full representation of the service's configuration.
If a reference points to a resource that is not marked as a configuration resource, the cmdlet downloads the entire representation but it does not follow the non-configuration resource's references.
The cmdlet returns a collection of **ExportObjectinstances**.

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

### Example 1: Get basic policy and portal configurations
```
$Pilot =  Export-FIMConfig  -uri http://localhost:5725/ResourceManagementService -PolicyConfig -PortalConfig
```

This command gets basic policy and portal configuration resources and stores the information in the variable named $Pilot.

### Example 2: Get custom resource types and groups
```
$Pilot =  Export-FIMConfig  -policyConfig -customConfig ("/ConstosoCustomResource", "/Group")
```

This command gets custom resource type and groups in addition to policy configuration and stores the information in the variable named $Pilot.

### Example 3: Get an end-to-end scenariofor migrating configuration
```
$Pilot =  Export-FIMConfig  -uri http://pilot:5725/ResourceManagementService -policyConfig $Pilot |  ConvertFrom-FIMResource  -File pilot.xml $Pilot =  ConvertTo-FIMResource  -File pilot.xml $Production =  Export-FIMConfig  -uri http://production:5725/ResourceManagementService -policyConfig $Matches =  Join-FIMConfig  -Source $Pilot -Target $production -DefaultJoin "DisplayName" $Imports = $Matches |  Compare-FIMConfig  $imports |  ConvertFrom-FIMResource  -file imports.xml $UndoneImports = $imports |  Import-FIMConfig  -uri http://production:5725/ResourceManagementService
```

This command is an end-to-end scenario for migrating configuration from a pilotmmsshortenvironment to a productionmmsshortenvironment.

### Example 4: Extract non-configuration information for use in other scenarios
```
$Pilot =  Export-FIMConfig  -customConfig "/Request[Target=/Person[DisplayName='Administrator']]" $Pilot |  ConvertFrom-FIMResource  -file report.xml
```

This command shows how to extract additional, non-configuration information that may be useful in other scenarios.
Scripters can take the ExportObjectinstances from the output and use them for other purposes.
One such purpose is generating reports.

## PARAMETERS

### -AllLocales
Indicates that the cmdlet uses all locales.

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
Specifies the user credentials required to access the Forefront Identity Manager service.

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
Specifies an array of custom configurations.

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
Specifies the size of the message.

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
Indicates that the cmdlet only uses base resources in the operation.

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
Indicates that the cmdlet uses policy configuration in the operation.

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
Indicates that the cmdlet uses portal configuration in the operation.

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
Indicates that the cmdlet uses schema configuration in the operation.

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
Specifies the uniform resource identifier (URI) for the Forefront Identity Manager service.

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

[Join-FIMConfig](xref:FIMAutomation/vlatest/Join-FIMConfig.md)

[Compare-FIMConfig](Compare-FIMConfig.md)

[Import-FIMConfig](Import-FIMConfig.md)

[ConvertFrom-FIMResource](ConvertFrom-FIMResource.md)

[ConvertTo-FIMResource](xref:FIMAutomation/vlatest/ConvertTo-FIMResource.md)
