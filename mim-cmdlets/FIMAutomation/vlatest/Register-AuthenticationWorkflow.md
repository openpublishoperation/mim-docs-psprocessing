---
external help file: Microsoft.ResourceManagement.Automation.dll-Help.xml
online version: 
schema: 2.0.0
updated_at: 5/9/2017 3:47 PM
ms.date: 5/9/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/FIMAutomation/vlatest/Register-AuthenticationWorkflow.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/FIMAutomation/vlatest/Register-AuthenticationWorkflow.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/bba03e1e0b7bea04619c48b98278723b1a8fc13d/mim-cmdlets/FIMAutomation/vlatest/Register-AuthenticationWorkflow.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Register-AuthenticationWorkflow

## SYNOPSIS
Registers a user for a Forefront Identity Manager service authentication workflow.

## SYNTAX

```
Register-AuthenticationWorkflow -UserName <String>
 -AuthenticationWorkflowRegistrationTemplate <AuthenticationWorkflowRegistrationTemplate> [-Uri <String>]
 [-Credential <PSCredential>]
```

## DESCRIPTION
Registers a user for a Forefront Identity Manager service authentication workflow. 
In order to register a user, an authentication workflow registration template that contains that users registration data must be created and supplied to this cmdlet.

## EXAMPLES

### --------------  Register User for an Authentication Workflow --------------
```
Register-AuthenticationWorkflow -UserName "domain\user1" -AuthenticationWorkflowRegistrationTemplate $template
```

In this example, the cmdlet is called to register user "domain\user1" using the specified template.

### --------------  Set Workflow template data and register a user for the workflow --------------
```
$template = Get-AuthenticationWorkflowRegistrationTemplate -AuthenticationWorkflowName "Password Reset AuthN Workflow"
          $usertemplate = $template.Clone()
          $usertemplate.GateRegistrationTemplates[0].Data[0].Value="answer1"
          $usertemplate.GateRegistrationTemplates[0].Data[1].Value="answer2"
          $usertemplate.GateRegistrationTemplates[0].Data[2].Value="answer3"

          Register-AuthenticationWorkflow -UserName "domain\user1" -AuthenticationWorkflowRegistrationTemplate $usertemplate
```

In this example, the Get-AuthenticationWorkflowRegistrationTemplate cmdlet is called to retrieve the password reset workflow template and assigned to the $template variable.
            Then a copy of the template is created and assigned to $usertemplate variable.

            Assuming the workflow has only one Questions and Answers Gate, 3 answers are set as part of the gate data for the first 3 questions of the gate data

            After the data is set for the gate, the register command is called to register user "domain\user1" using the specified template.

## PARAMETERS

### -UserName
The username of the user for which you wish to register. 
Please provide the username in the format: domain\username.

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

### -AuthenticationWorkflowRegistrationTemplate
An authentication workflow registration template that has been filled in with the gate registration data for the specified user.

```yaml
Type: AuthenticationWorkflowRegistrationTemplate
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
The user credentials required to access Forefront Identity Manager service.

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

### None

## NOTES

## RELATED LINKS

[Get-AuthenticationWorkflowRegistrationTemplate]()

[Unregister-AuthenticationWorkflow]()

[Confirm-AuthenticationWorkflowRegistration]()

