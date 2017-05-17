---
external help file: Microsoft.ResourceManagement.Automation.dll-Help.xml
online version: 
schema: 2.0.0
updated_at: 5/17/2017 2:42 AM
ms.date: 5/17/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/FIMAutomation/vlatest/Get-AuthenticationWorkflowRegistrationTemplate.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/FIMAutomation/vlatest/Get-AuthenticationWorkflowRegistrationTemplate.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/b087c1fa22e293ca887d71e98791a50333e0c2ab/mim-cmdlets/FIMAutomation/vlatest/Get-AuthenticationWorkflowRegistrationTemplate.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Get-AuthenticationWorkflowRegistrationTemplate

## SYNOPSIS
Gets an object of type AuthenticationWorkflowRegistrationTemplate that corresponds to an authentication workflow defined within the target Forefront Identity Manager service instance.


## SYNTAX

```
Get-AuthenticationWorkflowRegistrationTemplate -AuthenticationWorkflowName <String> [-Uri <String>]
 [-Credential <PSCredential>]
```

## DESCRIPTION
The **Get-AuthenticationWorkflowRegistrationTemplate** cmdlet gets an object of type **AuthenticationWorkflowRegistrationTemplate** that corresponds to an authentication workflow defined within the target Forefront Identity Manager service instance.
The workflow is specified by passing the name of the workflow as parameter.
The registration workflow template contain a collection of gate registration templates which correspond to the interactive gates (authentication activities) contained within the authentication workflow. 
Each registration gate in turn contains a Data property which is an array of name/value pairs of data required to register for the gate.

        

## EXAMPLES

### Example 1: Get a specific authentication workflow registration template
```
$Template = Get-AuthenticationWorkflowRegistrationTemplate -AuthenticationWorkflowName "Password Reset AuthN Workflow"
```

This command authenticates the workflow template if the workflow with the specified name exists in the FIM Database.

## PARAMETERS

### -AuthenticationWorkflowName
Specifies the display name of the authentication workflow which this cmdlet gets.

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

### -Uri
Specifies the uniform resource identifier (URI) for the Forefront Identity Manager service.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Http://localhost:5725/ResourceManagementService
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

## INPUTS

## OUTPUTS

### AuthenticationWorkflowRegistrationTemplate

## NOTES

## RELATED LINKS

[Confirm-AuthenticationWorkflowRegistration](Confirm-AuthenticationWorkflowRegistration.md)

[Register-AuthenticationWorkflow](xref:FIMAutomation/vlatest/Register-AuthenticationWorkflow.md)

[Unregister-AuthenticationWorkflow](xref:FIMAutomation/vlatest/Unregister-AuthenticationWorkflow.md)
