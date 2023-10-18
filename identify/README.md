### ```PeerID```
---
This is a networking identifier. It follows the rules of [libp2p identity](https://github.com/libp2p/specs/blob/master/peer-ids/peer-ids.md) and could be changed easily, because revealing your peer id is often equal to reveal ip address.

### ```SwnID```
---
Identifier, used to perform authentication on the SWN networking level. 

***Key type:***
- RSA: is only supported key type, used for SwnID (v0.0.1-beta)

***Where is it used:***
- swn-auth libp2p protocol: challenge-response protocol, as described in [swn-specs/auth](github.com/neonyxhub/swn-specs/authentification). Used to mark the connection authorized or not authorized to perform access control on swn level. This marker could be passed through on other app units. 


### ```DeviceID```
---
Identifier, used to perform swn-auth, without revealing your SwnID.

***Type:***
- SHA256 for RSA: deviceId is equal to first 12 symbols of SwnId, **only if SwnID is RSA type**

***Where is it used:***
- swn-auth: described in [swn-specs/auth](github.com/neonyxhub/swn-specs/authentification)
- identifying: now this info is placed only in local storage and used only in duo identify+auth