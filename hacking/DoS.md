---
tags:
  - security
  - attack
  - networking
---
# Denial of Service Attack

This is where an attacker will try to overload your service (usually using an exploit) to try and bring down the service entirely.

This attack isn't necessarily perpetrated by some evil hacker gang, it could be a rival company/service trying to disturb your service so that your customers will go to their website.

Also, this type of attack can be used as a smokescreen; drawing your attention to one particular part of your network as a decoy, but in reality the attacker is really after another part of your network.

Finally, this attack doesn't have to be complicated. It could simply be someone going up to your building and turning off the power.

## Potential Causes

- human error
    - a "layer 2 loop without STP" causes an exponential increase in traffic and therefore a DoS attack
    - running out of bandwidth because someone or something is downloading something
    - a waterline breaks
    - the power to your service goes out
- an attacker is targeting your network

## Distributed DoS (DDoS)

If there is only one IP that is bombarding your system, to resolve this, it is as simple as filtering out that single IP from contacting your service.

Naturally, hackers are aware of this tactic so it's much more efficient to have a botnet i.e., an army of over a million computers, all with unique IP addresses, to try and bombard your service. Usually, these computers are IoT devices made with poor security practices and or are located in different parts of the world.

An army of computers doing this is known as a distributed denial of service attack.

## Mitigation

Here are some methods to mitigate DDoS attacks:

- using a third-party cloud provider like CloudFlare to off load your burden onto them
- block suspicious or DDoS like activity with your firewall

>To a certain degree, it's almost impossible to fully protect yourself as even though your firewall is dropping connections, if there's 1000 requests per second, you're not going to have a good time.
