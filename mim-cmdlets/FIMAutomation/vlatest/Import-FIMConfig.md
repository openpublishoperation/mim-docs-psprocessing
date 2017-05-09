---
external help file: Microsoft.ResourceManagement.Automation.dll-Help.xml
online version: 
schema: 2.0.0
updated_at: 5/9/2017 3:47 PM
ms.date: 5/9/2017
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/FIMAutomation/vlatest/Import-FIMConfig.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/FIMAutomation/vlatest/Import-FIMConfig.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/bba03e1e0b7bea04619c48b98278723b1a8fc13d/mim-cmdlets/FIMAutomation/vlatest/Import-FIMConfig.md
ms.topic: reference
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: True
ms.service: identity-manager
---

# Import-FIMConfig

## SYNOPSIS
Imports changes into the target FIM Service by using Web service calls.

## SYNTAX

```
Import-FIMConfig [-Uri <String>] [-Credential <PSCredential>] [-Timeout <Int32>] [-ImportObject <ImportObject>]
 [-WhatIf] [-Confirm]
```

## DESCRIPTION
The Import-FIMConfig cmdlet takes in a list of ImportObject instances.
Each ImportObject represents one atomic Web service call to make.
Each Web service call can contain multiple attribute-level changes.
As the cmdlet creates resources, the cmdlet resolves references automatically in subsequent update and create operations.

All ImportObject instances sent to Import-FIMConfig are run.
You can construct ImportObject instances from custom Windows PowerShell™ scripts or Microsoft .NET code and provide them to Import-FIMConfig for processing.

For more information about ImportObject instances and about themmseeWindows PowerShell cmdlet set, see about_FIM.

## EXAMPLES

### ------------------------ EXAMPLE 1 ------------------------
```
$UndoneImports = $imports |  Import-FIMConfig  -uri http://localhost:5725/ResourceManagementService $undoneImports |  ConvertFrom-FIMResource  -file undone.xml
```

This is a simple example of importing.

Note that this example stores the return value to inspect that all changes were made successfully.

### ------------------------ EXAMPLE 2 ------------------------
```
<?xml version="1.0" encoding="utf-8"?> <Results xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"> <ImportObject> <SourceObjectIdentifier>urn:uuid:e41e9332-2a9b-4b78-bfd4-61a9476c1a92</SourceObjectIdentifier> <ObjectType>Set</ObjectType> <State>Create</State> <Changes> <ImportChange> <Operation>None</Operation> <AttributeName>DisplayName</AttributeName> <AttributeValue>All Helpdesk Nav Bar Set</AttributeValue> <FullyResolved>true</FullyResolved> <Locale>Invariant</Locale> </ImportChange> <ImportChange> <Operation>None</Operation> <AttributeName>ExplicitMember</AttributeName> <AttributeValue>urn:uuid:576d7226-3742-4927-85b9-9ea1248d9e6e</AttributeValue> <FullyResolved>false</FullyResolved> <Locale>Invariant</Locale> </ImportChange> <ImportChange> <Operation>None</Operation> <AttributeName>ObjectType</AttributeName> <AttributeValue>Set</AttributeValue> <FullyResolved>true</FullyResolved> <Locale>Invariant</Locale> </ImportChange> </Changes> <AnchorPairs> <JoinPair> <AttributeName>DisplayName</AttributeName> <AttributeValue>All Helpdesk Nav Bar Set</AttributeValue> </JoinPair> </AnchorPairs> </ImportObject> <ImportObject> <SourceObjectIdentifier>urn:uuid:f453b03f-70b4-47c0-a849-29777c8d0a39</SourceObjectIdentifier> <ObjectType>ManagementPolicyRule</ObjectType> <State>Create</State> <Changes> <ImportChange> <Operation>None</Operation> <AttributeName>ActionParameter</AttributeName> <AttributeValue>*</AttributeValue> <FullyResolved>true</FullyResolved> <Locale>Invariant</Locale> </ImportChange> <ImportChange> <Operation>None</Operation> <AttributeName>ActionType</AttributeName> <AttributeValue>Read</AttributeValue> <FullyResolved>true</FullyResolved> <Locale>Invariant</Locale> </ImportChange> <ImportChange> <Operation>None</Operation> <AttributeName>Disabled</AttributeName> <AttributeValue>False</AttributeValue> <FullyResolved>true</FullyResolved> <Locale>Invariant</Locale> </ImportChange> <ImportChange> <Operation>None</Operation> <AttributeName>DisplayName</AttributeName> <AttributeValue>Helpdesk Users can read Unlock Users Nav Bar</AttributeValue> <FullyResolved>true</FullyResolved> <Locale>Invariant</Locale> </ImportChange> <ImportChange> <Operation>None</Operation> <AttributeName>GrantRight</AttributeName> <AttributeValue>True</AttributeValue> <FullyResolved>true</FullyResolved> <Locale>Invariant</Locale> </ImportChange> <ImportChange> <Operation>None</Operation> <AttributeName>ObjectType</AttributeName> <AttributeValue>ManagementPolicyRule</AttributeValue> <FullyResolved>true</FullyResolved> <Locale>Invariant</Locale> </ImportChange> <ImportChange> <Operation>None</Operation> <AttributeName>PrincipalSet</AttributeName> <AttributeValue>urn:uuid:e41e9332-2a9b-4b78-bfd4-61a9476c1a92</AttributeValue> <FullyResolved>false</FullyResolved> <Locale>Invariant</Locale> </ImportChange> <ImportChange> <Operation>None</Operation> <AttributeName>ResourceCurrentSet</AttributeName> <AttributeValue>urn:uuid:e41e9332-2a9b-4b78-bfd4-61a9476c1a92</AttributeValue> <FullyResolved>false</FullyResolved> <Locale>Invariant</Locale> </ImportChange> </Changes> <AnchorPairs> <JoinPair> <AttributeName>DisplayName</AttributeName> <AttributeValue>Helpdesk Users can read Unlock Users Nav Bar</AttributeValue> </JoinPair> </AnchorPairs> </ImportObject> </Results>
```

This is an example of an ImportObject that creates a ManagementPolicyRule resource with the references to Set resources that have not been created yet.

Note that you would include the ImportObjects inside a file and load them by using ConvertTo-FIMResource .
This is an example on how to script batch operations inmmsshort.

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

### -ImportObject
{{Fill ImportObject Description}}

```yaml
Type: ImportObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Timeout
{{Fill Timeout Description}}

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

### ImportObject[]

## OUTPUTS

### ImportObject[]
A list of ImportObject instances not committed to the FIM service.
In the case of AuthN or AuthZ faults, the user is expected to approve the changes and continue importing where the process left off.

## NOTES

## RELATED LINKS

[Export-FIMConfig]()

[Join-FIMConfig]()

[Compare-FIMConfig]()

[ConvertFrom-FIMResource]()

[ConvertTo-FIMResource]()

