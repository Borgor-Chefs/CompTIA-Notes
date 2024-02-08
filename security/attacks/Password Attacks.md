---
tags:
  - security
  - attack
---
# Password Attacks

>NEVER STORE YOUR PASSWORDS IN PLAINTEXT.

These are types of attacks that attackers can use to try and obtain your passwords.

The goal of a hashing function is; given an input, create a unique output that is different from it's closest neighbours i.e., the hash for "AAB" is very different from "AAA" and "AAC". And, for it to be impossible to reverse the function i.e., give it a hash and it will return the input.

An intended side effect of the hashing function is that it should be slow enough so that attackers can't rapidly computer hashes but fast enough so that it's not computationally exhausting.

## Brute Force

Basically, given a hash (usually SHA256) of a password, the attacker will try every single possible combination of characters to try and break the hash and reverse engineer your password.

## Dictionary Attacks

Since humans like to use real words in their passwords, attackers can download dictionaries (collections of English words, or another language) and combine words in sequences to try and break the hashes.

Sometimes, people will substitute letters for numbers like how "password" might become "p@ssw0rd". During the cracking process, attackers (at least the smarter ones) will substitute letters for their common substituted counterparts.

## Optimization Techniques

Both [[#Brute Force]] and [[#Dictionary Attacks]] are computationally expensive and time consuming to only use one computer. Hackers with enough infrastructure will distribute the load to all their slave computers to speed up the process.

They will either use slave computers or a vast array of GPUs to crack hashes, similar to how someone would mine Bitcoin using GPUs and distributed computation.
