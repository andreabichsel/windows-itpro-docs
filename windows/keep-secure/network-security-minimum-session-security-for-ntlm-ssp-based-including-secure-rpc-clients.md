---
title: Network security Minimum session security for NTLM SSP based (including secure RPC) clients (Windows 10)
description: Describes the best practices, location, values, policy management and security considerations for the Network security Minimum session security for NTLM SSP based (including secure RPC) clients security policy setting.
ms.assetid: 89903de8-23d0-4e0f-9bef-c00cb7aebf00
ms.pagetype: security
ms.prod: W10
ms.mktglfcycl: deploy
ms.sitesec: library
author: brianlic-msft
---
# Network security: Minimum session security for NTLM SSP based (including secure RPC) clients
**Applies to**
-   Windows 10
Describes the best practices, location, values, policy management and security considerations for the **Network security: Minimum session security for NTLM SSP based (including secure RPC) clients** security policy setting.
## Reference
This policy setting allows a client device to require the negotiation of 128-bit encryption or NTLMv2 session security. These values are dependent on the **Network security: LAN Manager Authentication Level policy** setting value.
### Possible values
-   Require NTLMv2 session security
    The connection fails if strong encryption (128-bit) is not negotiated.
-   Require 128-bit encryption
    The connection fails if the NTLMv2 protocol is not negotiated.
### Best practices
Practices in setting this policy are dependent on your security requirements.
### Location
Computer Configuration\\Windows Settings\\Security Settings\\Local Policies\\Security Options
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
<td align="left"><p>Require 128-bit encryption</p></td>
</tr>
<tr class="even">
<td align="left"><p>DC Effective Default Settings</p></td>
<td align="left"><p>Require 128-bit encryption</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Member Server Effective Default Settings</p></td>
<td align="left"><p>Require 128-bit encryption</p></td>
</tr>
<tr class="even">
<td align="left"><p>Client Computer Effective Default Settings</p></td>
<td align="left"><p>Require 128-bit encryption</p></td>
</tr>
</tbody>
</table>
 
## Policy management
This section describes features and tools that are available to help you manage this policy.
### Restart requirement
None. Changes to this policy become effective without a device restart when they are saved locally or distributed through Group Policy.
### Policy conflicts
The settings for this security policy are dependent on the **Network security: LAN Manager Authentication Level policy** setting value. For info about this policy, see [Network security: LAN Manager authentication level](network-security-lan-manager-authentication-level.md).
## Security considerations
This section describes how an attacker might exploit a feature or its configuration, how to implement the countermeasure, and the possible negative consequences of countermeasure implementation.
### Vulnerability
Network traffic that uses the NTLM Security Support Provider (NTLM SSP) could be exposed such that an attacker who has gained access to the network can create man-in-the-middle attacks.
### Countermeasure
Enable all options that are available for the **Network security: Minimum session security for NTLM SSP based (including secure RPC) clients policy** setting.
### Potential impact
Client devices that enforce these settings cannot communicate with older servers that do not support them.
## Related topics
[Security Options](security-options.md)
 
 