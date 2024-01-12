Tags: [#networking #transport_layer]

# UDP (User Datagram Protocol)

![[Pasted image 20230331172002.png]]

This protocol is similar to TCP with the following differences:

- it doesn't guarantee that all data will be received
- it is connectionless (there is no three way handshake)

In this case, the sender doesn't really care if the receiver receives everything. UDP is most commonly used in video games because TCP could potentially break the flow of things since it could miss a packet, resend it and then you would rubber band back into place.

![[Pasted image 20230331172029.png]]

Because there is no overhead nor data guarantee, UDP is actually faster than TCP.
