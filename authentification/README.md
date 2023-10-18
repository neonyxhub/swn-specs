### Overview
---
Swn Authentication is the process that SHOULD be used after the connection between peers is established. It prevents DDOS on other protocols, which are supported by SWN. After the successful auth connection is marked as authenticated and this status could be used both inside the SWN processes and in other app units (CWN, PWN if we speak about whole Neonyx stack)

### Auth process
---
- Challenge-response with RSA SwnID:
- ![[modules-swn-auth.svg]]