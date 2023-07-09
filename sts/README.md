
# STS Handshake

This model uses a Diffie Hellman Key Exchange with added signatures to prevent man in the middle attacks.
Its goal is to provide mutual authentication between initiator and responder, while sharing a secret communication key.

![MSC of ...](/msc/msc_sts.png)

# Results

| Property  | Holds | Note |
| ------------- | ------------- | ------------- |
| Finish Initiator | Yes  | The initiator finishes the protocol. |
| Finish Responder | Yes  | The responder finishes the protocol. |
| Secret k | Yes  | The established communication key k remains secret. |
| Authentication Initiator  | Yes  | The initiator is able to authenticate the responder. |
| Authentication Responder  | Yes  | The responder is able to authenticate the initiator. |

All properties provide the expected outcome.
