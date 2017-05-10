---
external help file: Microsoft.ResourceManagement.Automation.dll-Help.xml
online version: 
schema: 2.0.0
updated_at: 5/9/2017 3:47 PM
ms.date: 5/9/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/FIMAutomation/vlatest/Confirm-AuthenticationWorkflowRegistration.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/FIMAutomation/vlatest/Confirm-AuthenticationWorkflowRegistration.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/bba03e1e0b7bea04619c48b98278723b1a8fc13d/mim-cmdlets/FIMAutomation/vlatest/Confirm-AuthenticationWorkflowRegistration.md
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
Use to determine if a user is a registered for a specific authentication workflow.

## SYNTAX

```
Confirm-AuthenticationWorkflowRegistration -UserName <String> -AuthenticationWorkflowName <String>
 [-Uri <String>] [-Credential <PSCredential>]
```

## DESCRIPTION
Use to determine if a user is a registered for a specific authentication workflow.

## EXAMPLES

### --------------  Check to see if a user is register for a specific authentication workflow --------------
```
Confirm-AuthenticationWorkflowRegistration -UserName "domain\user1" -AuthenticationWorkflowName "Password Reset AuthN Workflow"
```

The command returns a boolean value (True or False) indicating that the specified user is registered for the workflow specified by the workflow name parameter.

## PARAMETERS

### -UserName
The username of the user for which you wish to check registration status. 
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
The display name of the authentication workflow for which you wish to check registration status.

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

### Boolean

## NOTES

## RELATED LINKS

[Get-AuthenticationWorkflowRegistrationTemplate]()

[Register-AuthenticationWorkflow]()

[Unregister-AuthenticationWorkflow]()

