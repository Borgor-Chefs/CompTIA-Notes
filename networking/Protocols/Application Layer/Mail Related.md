Tags: [#networking #application_layer]

# Mail Related Protocols

These are protocols related to mail.

## SMTP (Simple Mail Transfer Protocol)

>[[Standard Ports|Standard port]]: 25
>[Link](https://en.wikipedia.org/wiki/Simple_Mail_Transfer_Protocol).

![[Pasted image 20230331195951.png]]

This protocol uses [[TCP|TCP]] to send transfer mail over the internet. It uses TCP to deliver mail because you want to make sure that the mail was actually sent.

## POP3 (Post Office Protocol Ver. 3)

>[[Standard Ports|Standard port]]: 110
>[Link](https://en.wikipedia.org/wiki/Post_Office_Protocol).

![[Pasted image 20230331200510.png]]

Where SMTP is used to send email, POP3 is used to receive email. All POP3 does is download emails from your mail server to your computer. Usually, POP3 deletes the email when you download it but it can be configured to simply copy it over to your machine.

This protocol, unlike IMAP4, doesn't sync the emails between your machine and the mail server. POP3 is commonly used in email applications such as Microsoft Outlook.

## IMAP (Internet Mail Access Protocol Ver. 4)

>[[Standard Ports|Standard port]]: 143
>[Link](https://en.wikipedia.org/wiki/Internet_Message_Access_Protocol).

![[Pasted image 20230331200651.png]]

Like POP3, this protocol is used to receive email however it has many more features than POP3 such as:

- you can sync your emails and folders between your computer and mail server
- you can access and manage (CRUD) your emails from your computer (over the internet)

IMAP4 is commonly used in email applications such as Microsoft Outlook.
