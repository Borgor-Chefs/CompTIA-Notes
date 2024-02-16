---
tags:
  - security
  - attack
  - malware
---
# Cross-Site Scripting (XSS)

>Video with some examples, [here](https://www.youtube.com/watch?v=Cut0mTPBrjE&list=PLG49S3nxzAnna96gzhJrzkii4hH_mgW4b&index=40).

This is a form of attack where an attacker will try and store some form of script or payload in a website that will execute whenever the page loads in the user's browser. If the website you're using isn't secure in terms of how it was created, it is vulnerable to XSS.

This is technically malware because it takes advantage of vulnerabilities with JavaScript and or the website.

## Non-Persistent (Reflected) XSS

This is where an attacker will send the user with a link that when clicked, it will execute some code that scrapes credentials, session IDs, cookies and send them to the attacker. Then the website will load as normal.

The JavaScript payload is usually stored in the URL.

## Persistent (Stored) XSS

This is where an attacker stores some payload inside of the website, like in a comment, bio, description, etc. a place where a lot of people will go to. What will happen is when a user loads this specific page, they will unknowingly execute this malware and be hacked.

## Mitigations

For session IDs, ensure that the token that the user is given expires after some interval. Hackers love to steal session IDs because it allows them to trick the server into thinking that they are the person whom they stole it from.

Make sure that your website sanitizes any form of external JavaScript to prevent the persistent form of this attack.

As for non-persistent, tell your users not to be dumb.

>Another option (which is HIGHLY recommended if you ever use the dark web) is to disable JavaScript. Three letter agencies love using JavaScript to pull your real IP.
