---
tags:
  - protocol
  - security
  - authentication
---
# Kerberos

Essentially, authenticate once and never again. There's no need to re-authenticate to access something else on the network after you've authenticated once. This authentication method supports single sign on (SSO).

You'd typically find Kerberos with Windows domains (and most likely [[Active Directory]]).

This was developed in the 1980s at MIT.

Microsoft started using Kerberos with Windows 2000, based on the Kerberos 5.0 open standard.

Kerberos is compatible with other operating systems and devices.

## SSO with Kerberos

![[Pasted image 20240131215825.png]]

SSO with Kerberos works with cryptographic tickets. When you sign on in the morning at work, your request goes to the Kerberos ticket service which authenticates you to the network and will give you a cryptographic ticket. This ticket gets presented to other device on the network allowing you to access them without having to re-authenticate.

This system is Kerberos-specific and (apparently) won't work some other things. There are also other SSO methods that can be used such as; smart-cards, SAML, etc.
