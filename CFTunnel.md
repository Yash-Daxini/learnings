### Use of CF Tunnel

- Cloudflare Tunnel allows you to connect your local web server to Cloudflare's edge network through an outbound-only connection. This means:

- You do not need to expose your server to the public internet.

- Cloudflare handles incoming HTTPS requests and securely routes them to your local service.

- We can't access the locally hosted application from the internet directly. To access it, we need to either expose it or create a tunnel that allows external access to the local application. CF Tunnel provides a way to create such tunnels, enabling secure access to local applications from remote locations.

### How CF Tunnel works

- Cloudflared tunnel establishes outbound connections (tunnels) between the local machine and Cloudflare's network. This allows users to expose their local applications to the internet securely without needing to open ports on their router or firewall.

- When cloudflared tunnel created locally on machine, it creates a secure connection to Cloudflare's edge network. This connection allows traffic to be routed through Cloudflare and access the local application securely. The tunnel can be configured to route traffic to specific ports or applications running on the local machine.

- After requesting URL provided by cloudflared tunnel, request goes to CF edge server and then is forwarded to the local machine through the established tunnel. The response from the local application is then sent back through the same tunnel to the Cloudflare edge server, which returns it to the client.
