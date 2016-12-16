---
Module Name: MIMPAM
Module Guid: 50335111-1302-416A-AE08-C487BC2E7994
Download Help Link: http://go.microsoft.com/fwlink/?LinkId=533892
Help Version: 1.0.0.0
Locale: en-US
ms.assetid: A821A0A5-E511-4606-A532-CC8D813B1758
updated_at: 12/16/2016 10:24 PM
ms.date: 12/16/2016
content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/MIMPAM.md
original_content_git_url: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/master/mim-cmdlets/MicrosoftIdentityManager/vlatest/MIMPAM.md
gitcommit: https://github.com/MicrosoftDocs/mim-docs-powershell/blob/d76fe71a336b890697ca5b79f29d35c57acf4cc6/mim-cmdlets/MicrosoftIdentityManager/vlatest/MIMPAM.md
uid: MicrosoftIdentityManager/vlatest/MIMPAM.md
ms.topic: conceptual
author: tarameyer
ms.author: femila
keywords: powershell, cmdlet
manager: femila
open_to_public_contributors: true
ms.service: identity-manager
---

# MIMPAM Module
## Description
This reference provides cmdlet descriptions and syntax for all Microsoft Identity Manager (MIM) Privileged Access Management (PAM) administrator specific and requestor cmdlets. It lists the cmdlets in alphabetical order based on the verb at the beginning of the cmdlet.

## MIMPAM Cmdlets
### [Close-PAMRequest](./Close-PAMRequest.md)
Closes the specified user's PAM activation request.

### [Close-PAMRequestForControl](./Close-PAMRequestForControl.md)
Cancels current PAM activation requests from other users.

### [Get-PAMConfiguration](./Get-PAMConfiguration.md)
Gets PAM scenario configuration settings from the MIM Service.

### [Get-PAMGroup](./Get-PAMGroup.md)
Gets groups from the MIM Service that are intended for PAM activation.

### [Get-PAMRequest](./Get-PAMRequest.md)
Gets PAM requests from the MIM Service.

### [Get-PAMRequestForReview](./Get-PAMRequestForReview.md)
Gets PAM activation requests for this user from the MIM Service.

### [Get-PAMRequestToApprove](./Get-PAMRequestToApprove.md)
Gets PAM activation requests from another user that are pending approval.

### [Get-PAMRole](./Get-PAMRole.md)
Gets PAM roles from the MIM Service.

### [Get-PAMRoleForRequest](./Get-PAMRoleForRequest.md)
Gets PAM roles from the MIM Service.

### [Get-PAMUser](./Get-PAMUser.md)
Gets users who can request activation from the MIM Service.

### [New-PAMDomainConfiguration](./New-PAMDomainConfiguration.md)
Updates a domain in an existing forest to add configuration data required by PAM.

### [New-PAMGroup](./New-PAMGroup.md)
Creates a representation of a security group in the MIM Service and a foreign principal group in Active Directory.

### [New-PAMRequest](./New-PAMRequest.md)
Creates a PAM activation request in the MIM Service.

### [New-PAMRole](./New-PAMRole.md)
Creates a PAM role in the MIM Service.

### [New-PAMSession](./New-PAMSession.md)
Creates a session for PAM administration with a different server.

### [New-PAMTrust](./New-PAMTrust.md)
Creates a trust relationship of the PAM domain from a domain in an existing forest.

### [New-PAMUser](./New-PAMUser.md)
Creates a PAM user in the MIM Service and also a new user in the PAM Active Directory domain corresponding to an existing user in a source domain.

### [Remove-PAMDomainConfiguration](./Remove-PAMDomainConfiguration.md)
Updates a domain in an existing forest to remove configuration data required by PAM.

### [Remove-PAMGroup](./Remove-PAMGroup.md)
Removes a PAM group from the MIM Service.

### [Remove-PAMRole](./Remove-PAMRole.md)
Removes a PAM role from the MIM Service.

### [Remove-PAMTrust](./Remove-PAMTrust.md)
Removes a trust relationship of the PAM forest from an existing forest that was established by the New-PAMTrust cmdlet.

### [Remove-PAMUser](./Remove-PAMUser.md)
Removes a user from the MIM Service and the PAM domain.

### [Set-PAMConfiguration](./Set-PAMConfiguration.md)
Updates PAM scenario configuration settings in the MIM Service.

### [Set-PAMGroup](./Set-PAMGroup.md)
Updates a PAM group in the MIM Service.

### [Set-PAMRequestToApprove](./Set-PAMRequestToApprove.md)
Updates a PAM activation request in the MIM Service from another user that is pending approval.

### [Set-PAMRole](./Set-PAMRole.md)
Updates a PAM role in the MIM Service.

### [Set-PAMUser](./Set-PAMUser.md)
Updates a PAM user in the MIM Service and PAM domain.

### [Test-PAMDomainConfiguration](./Test-PAMDomainConfiguration.md)
Verifies a domain has been prepared for its user and group resources to be managed by PAM.

### [Test-PAMTrust](./Test-PAMTrust.md)
Verifies whether a trust relationship exists from the source forest in the PAM domain.

