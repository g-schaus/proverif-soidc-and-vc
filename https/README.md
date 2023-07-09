
# HTTPS Handshake

## Simple Variant

The first model...

![MSC of ...](/msc/msc_https.png)

## With Modified Diffie Hellman Key Exchange

The second model uses a modified Diffie Hellman Key Exchange.

![MSC of ...](/msc/msc_https_dh.png)

## Results

| Property  | Holds |
| ------------- | ------------- |
| Finish Initiator | Yes  |
| Finish Responder | Yes  |
| Secret k from Initiator | Yes  |
| Secret k from Responder | No  |
| Authentication Initiator  | Yes  |
| Authentication Responder  | No  |

As the responder is not able to authenticate the initiator, a secret key may be established with an attacker.
This fact is shown in the results as expected and completely normal for a uni-directional authentication protocol like https.
