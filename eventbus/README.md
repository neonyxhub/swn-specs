### Overview
---
SWN EventBus protocol is a basis protocol, which allows sovereign apps to communicate with each other.

### Event structure
---
All events are described in protobuf and MUST follow the following structure:
тут будет протобаф ивентов

### Event passing proccess
---
Events are passed within the libp2p protocol ```/swn/eventbus```. They MUST be separated in specified way: ```<event_length\n><event_protobuf_unmarshalled>```
