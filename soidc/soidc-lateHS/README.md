# SOIDC - Authorisation Code Grant

## SOIDC With Late Handshake - Vulnerability Proof

The first model...

![MSC of ...](/msc/msc_soidc_lateHS.png)



## Results

| Property  | Holds | Note |
| ------------- | ------------- | ------------- |
| Finish Initiator | Yes  | The initiator finishes the protocol. |
| Finish Responder | Yes  | The responder finishes the protocol. |
| Secret k from Initiator | Yes  | The established communication key k remains secret if talking to the responder. |
| Secret k from Responder | No  | The established communication key k is revealed by the responder if talking to an attacker. |
| Authentication Initiator  | Yes  | The initiator is able to authenticate the responder. |
| Authentication Responder  | No  | The responder is unable to authenticate the initiator. |

Both models have the following properties...

The attack...

![MSC of ...](/msc/msc_attack_app_auth.png)

# SOIDC - Proposed Fix

## Proposed Version

Fix...

## Results

| Property  | Holds | Note |
| ------------- | ------------- | ------------- |
| Finish Initiator | Yes  | The initiator finishes the protocol. |
| Finish Responder | Yes  | The responder finishes the protocol. |
| Secret k from Initiator | Yes  | The established communication key k remains secret if talking to the responder. |
| Secret k from Responder | No  | The established communication key k is revealed by the responder if talking to an attacker. |
| Authentication Initiator  | Yes  | The initiator is able to authenticate the responder. |
| Authentication Responder  | No  | The responder is unable to authenticate the initiator. |


