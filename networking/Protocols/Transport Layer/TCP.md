Tags: [#networking #transport_layer]

# TCP (Transmission Control Protocol)

This is a connection oriented protocol, meaning that it must first acknowledge a session between two computers that are communicating. It establishes a session by performing a "three way handshake".

Here are the messages sent in this handshake:

- `SYN`
- `SYN ACK`
- `ACK RECEIVED`

![[Pasted image 20230331171345.png]]

After this handshake, the two computer siwll begin to send messages between each other. TCP guarantees that the data sent will be received, if there are any missing packets, the receiver will request the sender to resend that packet.
