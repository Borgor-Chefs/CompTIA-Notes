---
tags:
  - security
  - phones
---
# Multi-Factor Authentication

As the name implies, this includes multiple steps to authenticate. Factors are usually:

- something you are
- something you have
    - a phone or laptop like an authenticator application like Microsoft Authenticator
    - a [[Physical Keys|security key]] like a pseudo-random token generator
- something you know
    -  a password or personal information
- something you do
- somewhere you are

Applications like Microsoft Authenticator is useful cost-wise because a company won't have to distribute physical tokens which are susceptible to being lost, tokens such as: a USB key or a separate company phone.

## Short Message Service (SMS)

Usually, companies or services will send you a text with a link and or code to be used to authenticate. This isn't a bad practice but it's not the greatest:

- the phone number can (sometimes) be sent to a different phone
- SMS messages can be intercepted i.e., the text message containing the code can be intercepted and used
- SMS messages can be spoofed i.e., a malicious link is sent

The better thing to do here is to use an authenticator application.

## Phone Call

This is another way that companies or services will get you to authenticate. A bot will call you can speak each digit of the code that you'll need to enter.

But, like [[#Short Message Service (SMS)|SMS]] there are similar disadvantages to doing this:

- the phone call can be intercepted
- the phone call can be forwarded
- the phone number can be changed to the attacker's phone
