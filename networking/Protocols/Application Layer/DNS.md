---
tags:
  - networking
  - application_layer
---
# Domain Name System (DNS)

>[[Networking Ports|Standard port]]: 53
>[Link](https://en.wikipedia.org/wiki/Domain_Name_System).

This resolves domain names like www.google.com to an IP address like 8.8.8.8.

![[Pasted image 20230331192834.png]]

This works like a phone book where you take a name and map it to a phone number.

## Records

DNS stores "records" in a database, these records hold the domain name and the IP address of a given server.

All these records basically have the same format as they have the domain, record type, time-till-live (TTL). The other fields is what differentiates them.

>[Here](https://www.cloudflare.com/learning/dns/dns-records/) is a list of DNS records from CloudFlare.

### A Type

Here's a [sample](https://www.cloudflare.com/learning/dns/dns-records/dns-aaaa-record/) AAAA record:

|example.com|record type|value|TTL|
|-|-|-|-|
|(preferred subdomain)|AAAA|2001:0db8:85a3:0000:0000:8a2e:0370:7334|14400|
|(or root domain (@))|A|192.168.0.0|14400|

There are two types of records:

- A records, used for [[IP Address#IPv4|IPv4]] addresses
- AAAA records, used for [[IP Address#IPv6|IPv6]] addresses

There's pretty much no difference between the types of A records.

### MX Record

Here's a [sample](https://www.cloudflare.com/learning/dns/dns-records/dns-mx-record/) MX record:

|example.com|record type|priority|value|TTL|
|-|-|-|-|-|
|(preferred subdomain)|MX|10|mailhost1.example.com|45000|
|(or root domain (@))|MX|20|mailhost2.example.com|45000|

The lowest priority dictates which server the DNS provider will try and send the mail to first.

### TXT Record

Here's are some [sample](https://www.cloudflare.com/learning/dns/dns-records/dns-txt-record/) TXT records:

|example.com|record type|value|TTL|
|-|-|-|-|
|(preferred subdomain)|TXT|Some text goes here|45000|
|(or root domain (@))|TXT|"printer=lpr5"|45000|

TXT records also help in preventing spam/fake emails from domains of which they actually did not originate from.

#### Sender Policy Framework (SPF) TXT Records

>SPF TXT records list all the servers that are authorized to send email messages from a domain.  
>CloudFlare.

#### Domain Keys Identified Mail (DKIM)

>DKIM works by digitally signing each email using a public-private key pair. This helps verify that the email is actually from the domain it claims to be from. The public key is hosted in a TXT record associated with the domain. (Learn more about [public key encryption](https://www.cloudflare.com/learning/ssl/how-does-public-key-encryption-work/).)  
>CloudFlare.

#### Domain-based Message Authentication, Reporting & Conformance (DMARC)

>A DMARC TXT record references the domain's SPF and DKIM policies. It should be stored under the title \_dmarc.example.com. with 'example.com' replaced with the actual domain name. The 'value' of the record is the domain's DMARC policy (a guide to creating one can be found [here](https://dmarcguide.globalcyberalliance.org/#/dmarc/)).
>CloudFlare.
