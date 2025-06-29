## SSH

Its knonwn as Secure shell. Its most essential tool for remote access to servers and devices. SSH provides a secure channel over an unsecured network in a client-server architecture, allowing users to log into another computer over a network, execute commands, and manage files securely. 

SSH is a protocoal to connect to a remote servers securely. This connection is established using a client-server model, where the SSH client initiates the connection to the SSH server. The communication is encrypted, ensuring that data transmitted over the network remains confidential and secure.

SSH is primarily used for remote command line access, file transfers and tunneling traffic.

### How SSH Works
- When SSH client attempts to connect to an SSH server, it begins by establishing a TCP connection to the server's SSH port (default is port 22).
- Once TCP connection is established, the SSH client and server perform a handshake to negotiate encryption algorithms and exchange keys. This step ensures that both parties can communicate securely.
- After the handshake, the client authenticates itself to the server using various methods such as password authentication, public key authentication, or other methods.
