---
external help file: Microsoft.ResourceManagement.Automation.dll-Help.xml
online version: 
schema: 2.0.0
updated_at: 5/17/2017 2:42 AM
ms.date: 5/17/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/FIMAutomation/vlatest/Confirm-AuthenticationWorkflowRegistration.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/FIMAutomation/vlatest/Confirm-AuthenticationWorkflowRegistration.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/b087c1fa22e293ca887d71e98791a50333e0c2ab/mim-cmdlets/FIMAutomation/vlatest/Confirm-AuthenticationWorkflowRegistration.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Confirm-AuthenticationWorkflowRegistration

## SYNOPSIS
Determines if a user is a registered for a specific authentication workflow.

## SYNTAX

```
Confirm-AuthenticationWorkflowRegistration -UserName <String> -AuthenticationWorkflowName <String>
 [-Uri <String>] [-Credential <PSCredential>]
```

## DESCRIPTION
The **Confirm-AuthenticationWorkflowRegistration** cmdlet determines if a user is a registered for a specific authentication workflow.

## EXAMPLES

### Example 1: Check to see if a user is register for a specific authentication workflow
```
PS C:\> Confirm-AuthenticationWorkflowRegistration -UserName "domain\user1" -AuthenticationWorkflowName "Password Reset AuthN Workflow"
```

This command returns a boolean value (True or False) indicating that the specified user is registered for the workflow specified by the workflow name parameter.

## PARAMETERS

### -UserName
Specifies the username of the user for which you wish to check registration status. 
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

### -AuthenticationWorkflowName
Specifies the display name of the authentication workflow for which you wish to check registration status.

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

### Boolean

## NOTES

## RELATED LINKS

[Get-AuthenticationWorkflowRegistrationTemplate](xref:FIMAutomation/vlatest/Get-AuthenticationWorkflowRegistrationTemplate.md)

[Register-AuthenticationWorkflow](xref:FIMAutomation/vlatest/Register-AuthenticationWorkflow.md)

[Unregister-AuthenticationWorkflow](xref:FIMAutomation/vlatest/Unregister-AuthenticationWorkflow.md)
