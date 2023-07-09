# SOIDC - Authorisation Code Grant

## SOIDC With Late Handshake - Vulnerability Proof

The model is based on the version found [here](/soidc/soidc) and simulates an implementation error leading to a delay in the handshake timing.

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

Fixing the code leak and issuer authentication may be achieved by adding the issuer identity to the code during its transfer through the browser. By using the fix, the code verifier is no longer needed.

## Results

| Property  | Holds | Note |
| ------------- | ------------- | ------------- |
| Finish Initiator | Yes  | The initiator finishes the protocol. |
| Finish Responder | Yes  | The responder finishes the protocol. |
| Secret k from Initiator | Yes  | The established communication key k remains secret if talking to the responder. |
| Secret k from Responder | No  | The established communication key k is revealed by the responder if talking to an attacker. |
| Authentication Initiator  | Yes  | The initiator is able to authenticate the responder. |
| Authentication Responder  | No  | The responder is unable to authenticate the initiator. |


