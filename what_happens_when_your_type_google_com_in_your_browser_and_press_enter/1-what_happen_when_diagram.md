# Task 1: The Infrastructure Diagram (1-what_happen_when_diagram)

This file should contain the **URL** to your hosted diagram. Below is a logic map you can use to build your visual in tools like `diagrams.net` or `Mermaid.js`.

## Mermaid Diagram Structure

```mermaid
graph TD
    subgraph Client_Side [User Browser]
        A((Type https://www.google.com)) --> B{DNS Cache?}
    end

    subgraph Internet_Infrastructure [Network Layer]
        B -- No --> DNS[DNS Request: Resolve IP]
        DNS --> C[TCP/IP 3-Way Handshake]
        C --> D[HTTPS/SSL Handshake: Port 443]
    end

    subgraph Security_Perimeter [Security Layer]
        D --> FW{Firewall Check}
    end

    subgraph Google_Infrastructure [Server Stack]
        FW -- Authorized --> LB[Load Balancer]
        LB --> WS[Web Server: Serves Static Content]
        WS --> AS[Application Server: Process Logic]
        AS --> DB[(Database: Retrieve Data)]
        
        DB -.-> AS
        AS -.-> WS
        WS -.-> LB
    end

    LB -.->|Encrypted Response| A
    
    style D fill:#f96,stroke:#333,stroke-width:2px
    style FW fill:#f9f,stroke:#333,stroke-width:2px
    style LB fill:#bbf,stroke:#333,stroke-width:2px
```
