Uses encryption to send and receive data to avoid Man-in-the-middle (MiTM) attack.

HTTPS is becoming the standard because it is more secure.

HTTP request data looks like this during transfer:
![[Pasted image 20260901202526.png]]

HTTPS looks like this:
![[Pasted image 20260901202543.png]]


You can check if website uses HTTPS using address bar.

## Flow
![[Pasted image 20260902104829.png]]

**Key exchange** is making a common encrypted key using one public key and two private keys ( one client and server each ).

**Handshake**: The process of two communicating sides exchange messages to acknowledge and verify each other.

## cURL For HTTPS:

**SSL certificate:** _digital certificate that_ authenticates a website's identity and enables an encrypted connection.

To skip ssl check : use `cURL -k`

