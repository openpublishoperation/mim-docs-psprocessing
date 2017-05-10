---
external help file: Microsoft.ResourceManagement.Automation.dll-Help.xml
online version: 
schema: 2.0.0
updated_at: 5/9/2017 3:47 PM
ms.date: 5/9/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/FIMAutomation/vlatest/Unregister-AuthenticationWorkflow.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/live/mim-cmdlets/FIMAutomation/vlatest/Unregister-AuthenticationWorkflow.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/bba03e1e0b7bea04619c48b98278723b1a8fc13d/mim-cmdlets/FIMAutomation/vlatest/Unregister-AuthenticationWorkflow.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Unregister-AuthenticationWorkflow

## SYNOPSIS
Unregisters a user for a Forefront Identity Manager service authentication workflow.

## SYNTAX

```
Unregister-AuthenticationWorkflow -UserName <String> -AuthenticationWorkflowName <String> [-Uri <String>]
 [-Credential <PSCredential>]
```

## DESCRIPTION
Unregisters a user for a Forefront Identity Manager service authentication workflow.

## EXAMPLES

### --------------  Unregister a user for an authentication workflow --------------
```
Unregister-AuthenticationWorkflow -UserName "domain\user1" -AuthenticationWorkflowName "Password Reset AuthN Workflow"
```

The command unregister the user "domain\user1" from the workflow specified by the workflow name parameter.

## PARAMETERS

### -UserName
The username of the user for which you wish to unregister. 
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
The display name of the authentication workflow which you wish to unregister the user from.

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

### None

## NOTES

## RELATED LINKS

[Get-AuthenticationWorkflowRegistrationTemplate]()

[Register-AuthenticationWorkflow]()

[Confirm-AuthenticationWorkflowRegistration]()

