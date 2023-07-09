# SOIDC - Authorisation Code Grant

## SOIDC - Vulnerability Proof

The model is based on the message flow provided in the official Solid OIDC Primer. 
It uses a special handshake designed to mimic HTTPS connections, which can be found [here](/https/README.md).

![MSC of ...](/msc/msc_soidc.png)

## Results

| Property  | Holds | Note |
| ------------- | ------------- | ------------- |
| Finish Initiator | Yes  | The initiator finishes the protocol. |
| Finish Responder | Yes  | The responder finishes the protocol. |
| Secret k from Initiator | Yes  | The established communication key k remains secret if talking to the responder. |
| Secret k from Responder | No  | The established communication key k is revealed by the responder if talking to an attacker. |
| Authentication Initiator  | Yes  | The initiator is able to authenticate the responder. |
| Authentication Responder  | No  | The responder is unable to authenticate the initiator. |

The attack...

![MSC of ...](/msc/msc_attack_issuer_auth.png)

# SOIDC - Proposed Fix

## Proposed Version

Fix...

![MSC of ...](/msc/msc_soidc_fix_nopkce.png)

## Results

| Property  | Holds | Note |
| ------------- | ------------- | ------------- |
| Finish Initiator | Yes  | The initiator finishes the protocol. |
| Finish Responder | Yes  | The responder finishes the protocol. |
| Secret k from Initiator | Yes  | The established communication key k remains secret if talking to the responder. |
| Secret k from Responder | No  | The established communication key k is revealed by the responder if talking to an attacker. |
| Authentication Initiator  | Yes  | The initiator is able to authenticate the responder. |
| Authentication Responder  | No  | The responder is unable to authenticate the initiator. |


