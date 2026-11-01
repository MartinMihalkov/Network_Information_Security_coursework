This file describes the current infrastructure of PharmaDist.

The topology contains two devices:
- **gw** - acts as a router, routing traffic from server to the internet.
- **srv** - a server, which will run all the services needed for the project.

All nodes are based on Debian GNU/Linux.

The IP Addressing scheme is as follows:

| Hostname | IP | Gateway |
| :--- | :--- | :--- |
| **Gw** | 10.0.1.2/24 (lan1) | 10.0.3.1 |
| **Gw** | 10.0.2.2/24 (lan2) | 10.0.3.1 |
| **Gw** | 10.0.3.2/24 (wan) | 10.0.3.1 |
| **Srv** | 10.0.1.10/24 (lan1) | 10.0.1.2 |

## Gw
A Linux machine acting like a router towards the Internet.

### Configuration
- IP forwarding is enabled
- NAT Masquerading is enabled, to allow accessing the Internet

## Srv
A Linux server, on which multiple services should run in the future.

Currently both nodes can ping each other and the Srv can ping the Internet.
