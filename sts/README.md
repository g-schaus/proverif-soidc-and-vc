
# STS Handshake

This model uses a Diffie Hellman Key Exchange with added signatures to prevent man in the middle attacks.
Its goal is to provide mutual authentication between initiator and responder, while sharing a secret communication key.

![MSC of ...](/msc/msc_sts.png)

# Results

| Property  | Holds |
| ------------- | ------------- |
| Finish Initiator | Yes  |
| Finish Responder | Yes  |
| Secret k | Yes  |
| Authentication Initiator  | Yes  |
| Authentication Responder  | Yes  |

As seen above, all properties provide the expected outcome.
