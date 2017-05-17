---
external help file: Microsoft.ResourceManagement.Automation.dll-Help.xml
online version: 
schema: 2.0.0
updated_at: 5/17/2017 2:42 AM
ms.date: 5/17/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/FIMAutomation/vlatest/Register-AuthenticationWorkflow.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/FIMAutomation/vlatest/Register-AuthenticationWorkflow.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/b087c1fa22e293ca887d71e98791a50333e0c2ab/mim-cmdlets/FIMAutomation/vlatest/Register-AuthenticationWorkflow.md
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

### Example 1: Register User for an Authentication Workflow
```
PS C:\> Register-AuthenticationWorkflow -UserName "domain\user1" -AuthenticationWorkflowRegistrationTemplate $Template
```

This command calls to register user domain\user1 using the specified template.

### Example 2: Set Workflow template data and register a user for the workflow 
```
PS C:\> $Template = Get-AuthenticationWorkflowRegistrationTemplate -AuthenticationWorkflowName "Password Reset AuthN Workflow"
          $Usertemplate = $template.Clone()
          $Usertemplate.GateRegistrationTemplates[0].Data[0].Value="answer1"
          $Usertemplate.GateRegistrationTemplates[0].Data[1].Value="answer2"
          $Usertemplate.GateRegistrationTemplates[0].Data[2].Value="answer3"

          Register-AuthenticationWorkflow -UserName "domain\user1" -AuthenticationWorkflowRegistrationTemplate $Usertemplate
```

This example uses the **Get-AuthenticationWorkflowRegistrationTemplate** cmdlet to get the password reset workflow template and assigned to the $Template variable.
Then a copy of the template is created and assigned to $usertemplate variable.

Assuming the workflow has only one Questions and Answers Gate, 3 answers are set as part of the gate data for the first 3 questions of the gate data.

After the data is set for the gate, the register command is called to register user "domain\user1" using the specified template.

## PARAMETERS

### -UserName
Specifies the username of the user for which this cmdlet registers. 
Provide the username in the format: domain\username.

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
Specifies an authentication workflow registration template that has been filled in with the gate registration data for the specified user.

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
Specifies the user credentials required to access Forefront Identity Manager service.

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

[Confirm-AuthenticationWorkflowRegistration](xref:FIMAutomation/vlatest/Confirm-AuthenticationWorkflowRegistration.md)

[Get-AuthenticationWorkflowRegistrationTemplate](xref:FIMAutomation/vlatest/Get-AuthenticationWorkflowRegistrationTemplate.md)

[Unregister-AuthenticationWorkflow](xref:FIMAutomation/vlatest/Unregister-AuthenticationWorkflow.md)
