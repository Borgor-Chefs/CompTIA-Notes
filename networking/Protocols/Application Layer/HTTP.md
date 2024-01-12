Tags: [#networking #application_layer]
[[Networking Ports|Standard port]]: HTTP is 80, HTTPS is 443.
[Link](https://en.wikipedia.org/wiki/HTTP).

# HTTP (Hypertext Transfer Protocol)

The most widely used protocol to send websites over the internet.
Whenever you prefix a URL with `http://` this is the protocol that you're using to request information from the URL.

The same goes for `ftp://` or even nonprotocols such as `steam://` or `discord://`, these would be application specifiers or their own protocol.

The current valid version of HTTP are 1.1, 2 and 3.

## HTTPS (Secure HTTP)

Unlike HTTP, this encrypts data before being sent over the internet. The encryption method used is TLS (formerly SSL).

This is the standard today, you shouldn't use HTTP in a professional setting.

Some examples of websites that SHOULD use HTTPS are:

- banks
- e-commerce
- emails
