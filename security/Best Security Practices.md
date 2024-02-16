---
tags:
  - security
---
# Best Security Practices

Here's a list of best security practices for computers:

- [[#Encryption]]
- [[#Backups and Managing them]]
- [[#Passwords]]
- [[#Computer Sleep Timers]]
- [[#Least Privilege]]
- [[#Disabling Unnecessary Accounts]]
- [[#Disabling AutoRun and AutoPlay]]

## Encryption

Encrypt drives, files or folders if they are sensitive information. It's also a good idea to encrypt your USB drives

## Backups and Managing them

It's generally a good idea to keep a backup or manage your access keys in case you lose them, this could be integrated into active directory.

## Passwords

A good password is something that is greater than 12 characters and that is a mix of lower case, upper case and special characters.

You should **always** change default passwords as this is one of the most common things that attackers will look for; people not changing the default credentials from "admin" and "root".

Generally, you should always require passwords on everything that you hold dear. This means:

- no blank passwords
- no automated logins
- no passwords that are less than 8 characters

### BIOS/UEFI Passwords

In the BIOS or UEFI, you can set passwords to prevent a couple of changes i.e.,

- setting an administrator password on the BIOS to prevent changes
- prevent booting into the operating system without the user password

### Storage

I would personally use a password manager to store all your passwords, this could be something local like KeePassXC.

>I wouldn't necessarily recommend using something cloud based as they are prime targets to being hacked, also, should you really want your passwords being stored somewhere in the cloud?

### Rotation

Passwords should generally be changed on a monthly, bimonthly or even weekly basis depending on what they unlock.

### Resetting Passwords

Resetting the password should not be trivial i.e., there should be various authentication steps put in place to ensure that the person trying to reset their password is the correct person and not an attacker.

### Password Lock Outs

This is where a user is given a set number of times to login to their account, if they cannot, have them contact IT for support.

## Computer Sleep Timers

Whenever a user physically leaves their computer and goes somewhere else, an attacker could in theory snatch the computer and try to do some digging (this happened when the FBI targeted a deep web user).

Naturally, setting a some timer after the user's last input which locks the computer is generally a good idea. Along with this, when the computer is locked out, it should require a password to log back in.

Or, to prevent physical theft, use some type of physical lock that binds the computer or laptop to an anchor preventing people from running away with it.

## Least Privilege

In the world of IT, your users should have the bare minimum permissions relative to what they need to do i.e., you only get what you need to do your job.

All user applications should run with the most minimal privileges possible, to protect the rest of the computer system from anything possibly malicious. For example, Joe from accounting should not have universal administrative access.

## Disabling Unnecessary Accounts

Here, you should:

- disable or remove any unnecessary accounts
- disable the guest account
- disable interactive logins for accounts that don't need them

>Also change their default passwords.

## Disabling AutoRun and AutoPlay

>Windows only.

This is where, when a drive is mounted, Windows will execute whatever is located in `autorun.inf`. This feature was removed in Windows 7 and onwards because (what I assume) it was a security risk and there some hacks using it.

There's a similar feature called "AutoPlay" for [[Bluetooth]] devices. This can be disabled in Settings > Bluetooth & devices > AutoPlay.
