
# HTTPS Handshake

Its goal is to provide uni-directional authentication between initiator and responder, while sharing a secret communication key.

## Simple Variant With Nonce

The first model uses a simple structure utilizing a nonce _n_ for authentication purposes and a session key _ski_ for forward secrecy.

![MSC of ...](/msc/msc_https.png)

## With Modified Diffie Hellman Key Exchange

The second model uses a Diffie Hellman Key Exchange (DHKE) with added signatures to prevent man in the middle attacks. 
The DHKE is deliberately cut in half to only provide uni-directional authentication.

![MSC of ...](/msc/msc_https_dh.png)

## Results

| Property  | Holds | Note |
| ------------- | ------------- | ------------- |
| Finish Initiator | Yes  | The initiator finishes the protocol. |
| Finish Responder | Yes  | The responder finishes the protocol. |
| Secret k from Initiator | Yes  | The established communication key k remains secret if talking to the responder. |
| Secret k from Responder | No  | The established communication key k is revealed by the responder if talking to an attacker. |
| Authentication Initiator  | Yes  | The initiator is able to authenticate the responder. |
| Authentication Responder  | No  | The responder is unable to authenticate the initiator. |

As the responder is not able to authenticate the initiator, a secret key may be established with an attacker.
This fact is shown in the results as expected and completely normal for a uni-directional authentication protocol like https.
