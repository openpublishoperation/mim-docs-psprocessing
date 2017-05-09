---
external help file: Microsoft.ResourceManagement.Automation.dll-Help.xml
online version: 
schema: 2.0.0
updated_at: 5/9/2017 3:47 PM
ms.date: 5/9/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/FIMAutomation/vlatest/Get-AuthenticationWorkflowRegistrationTemplate.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/FIMAutomation/vlatest/Get-AuthenticationWorkflowRegistrationTemplate.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/bba03e1e0b7bea04619c48b98278723b1a8fc13d/mim-cmdlets/FIMAutomation/vlatest/Get-AuthenticationWorkflowRegistrationTemplate.md
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
Returns an object of type AuthenticationWorkflowRegistrationTemplate that corresponds to an authentication workflow defined within the target Forefront Identity Manager service instance.
The workflow is specified by passing the name of the workflow as parameter.

## SYNTAX

```
Get-AuthenticationWorkflowRegistrationTemplate -AuthenticationWorkflowName <String> [-Uri <String>]
 [-Credential <PSCredential>]
```

## DESCRIPTION
Returns an object of type AuthenticationWorkflowRegistrationTemplate that corresponds to an authentication workflow defined within the target Forefront Identity Manager service instance.
The workflow is specified by passing the name of the workflow as parameter.
The registration workflow template contain a collection of gate registration templates which correspond to the interactive gates (authentication activities) contained within the authentication workflow. 
Each registration gate in turn contains a Data property which is an array of name/value pairs of data required to register for the gate.

        Use the returned template objects to register a user for an authentication workflow using the Register-AuthenticationWorkflow cmdlet.

## EXAMPLES

### --------------  Get a specific authentication workflow registration template --------------
```
$template = Get-AuthenticationWorkflowRegistrationTemplate -AuthenticationWorkflowName "Password Reset AuthN Workflow"
```

In this example command will the authentication workflow template if the workflow with the specified name exists in the FIM Database.

## PARAMETERS

### -AuthenticationWorkflowName
The display name of the authentication workflow which you wish to return.

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
The uniform resource identifier for the Forefront Identity Manager service.

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
The user credentials required to access the Forefront Identity Manager service.

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

[Register-AuthenticationWorkflow]()

[Unregister-AuthenticationWorkflow]()

[Confirm-AuthenticationWorkflowRegistration]()

