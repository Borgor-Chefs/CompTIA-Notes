---
tags:
  - authentication
  - security
---
# Authentication Methods

There are various modes of authentication, but the most common are:

- [[Kerberos]]
- [[RADIUS]]
- [[TACACS]]

It's common for companies or services to also include [[Multi-Factor Authentication]]. MFA or 2FA can either be expensive if you have chips and readers physically installed somewhere or inexpensive if you're using something like Microsoft or Google authenticator.

## Which to Choose?

It's a matter of use case and what you already have.

If your devices only have RADIUS support or already talk to a RADIUS server, then you'll probably just use a RADIUS AAA server.

If you work with a lot or only Cisco devices that use TACACS+, you'll probably just use a TACACS+ AAA server.

If you're working with Windows devices in a Windows domain, you'll use Kerberos.
