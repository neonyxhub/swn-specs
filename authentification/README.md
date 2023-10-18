### Overview
---
Swn Authentication is the process that SHOULD be used after the connection between peers is established. It prevents DDOS on other protocols, which are supported by SWN. After the successful auth connection is marked as authenticated and this status could be used both inside the SWN processes and in other app units (CWN, PWN if we speak about whole Neonyx stack)

### Auth process
---
- Challenge-response with RSA SwnID:

![[modules-swn-auth.svg]]

Each message in this process is separated with ```\n``` symbol, that is how we understand when previous message ended.
Right now dropping stream is not followed by any additional info written to auth stream, except default stream dropping libp2p process. Future proccess will be described [todo](#todo)

### TODO
---
- [ ] Drop stream with additional data on each stage
- [ ] Discuss which keys could be used in swnauth process