---
title: Network access Let Everyone permissions apply to anonymous users (Windows 10)
description: Describes the best practices, location, values, policy management and security considerations for the Network access Let Everyone permissions apply to anonymous users security policy setting.
ms.assetid: cdbc5159-9173-497e-b46b-7325f4256353
ms.pagetype: security
ms.prod: W10
ms.mktglfcycl: deploy
ms.sitesec: library
author: brianlic-msft
---
# Network access: Let Everyone permissions apply to anonymous users
**Applies to**
-   Windows 10
Describes the best practices, location, values, policy management and security considerations for the **Network access: Let Everyone permissions apply to anonymous users** security policy setting.
## Reference
This policy setting determines what additional permissions are granted for anonymous connections to the device. If you enable this policy setting, anonymous users can enumerate the names of domain accounts and shared folders and perform certain other activities. This capability is convenient, for example, when an administrator wants to grant access to users in a trusted domain that does not maintain a reciprocal trust.
By default, the token that is created for anonymous connections does not include the Everyone SID. Therefore, permissions that are assigned to the Everyone group do not apply to anonymous users.
### Possible values
-   Enabled
    The Everyone SID is added to the token that is created for anonymous connections, and anonymous users can access any resource for which the Everyone group has been assigned permissions.
-   Disabled
    The Everyone SID is removed from the token that is created for anonymous connections.
-   Not defined
### Best practices
-   Set this policy to **Disabled**.
### Location
Computer Configuration\\Windows Settings\\Security Settings\\Local Polices\\Security Options
### Default values
The following table lists the actual and effective default values for this policy. Default values are also listed on the policy’s property page.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Server type or GPO</th>
<th align="left">Default value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Default Domain Policy</p></td>
<td align="left"><p>Not defined</p></td>
</tr>
<tr class="even">
<td align="left"><p>Default Domain Controller Policy</p></td>
<td align="left"><p>Not defined</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Stand-Alone Server Default Settings</p></td>
<td align="left"><p>Disabled</p></td>
</tr>
<tr class="even">
<td align="left"><p>DC Effective Default Settings</p></td>
<td align="left"><p>Disabled</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Member Server Effective Default Settings</p></td>
<td align="left"><p>Disabled</p></td>
</tr>
<tr class="even">
<td align="left"><p>Client Computer Effective Default Settings</p></td>
<td align="left"><p>Disabled</p></td>
</tr>
</tbody>
</table>
 
## Policy management
This section describes features and tools that are available to help you manage this policy.
### Restart requirement
None. Changes to this policy become effective without a device restart when they are saved locally or distributed through Group Policy.
## Security considerations
This section describes how an attacker might exploit a feature or its configuration, how to implement the countermeasure, and the possible negative consequences of countermeasure implementation.
### Vulnerability
An unauthorized user could anonymously list account names and shared resources and use the information to attempt to guess passwords, perform social engineering attacks, or launch DoS attacks.
### Countermeasure
Disable the **Network access: Let Everyone permissions apply to anonymous users** setting.
### Potential impact
None. This is the default configuration.
## Related topics
[Security Options](security-options.md)
 
 