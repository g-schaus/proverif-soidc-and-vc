# SOIDC - Authorisation Code Grant

## With Late Handshake - Vulnerability Proof

The model is based on the version found [here](/soidc/soidc) and simulates an implementation error leading to a delay in the handshake timing.

![MSC of ...](/msc/msc_soidc_lateHS.png)

## Results

| Property  | Holds | Note |
| ------------- | ------------- | ------------- |
| Finish App | Yes  | The app finishes the protocol. |
| Finish Browser | Yes  | The browser finishes the protocol. |
| Finish Issuer | Yes  | The issuer finishes the protocol. |
| Secret code | No  | The established code remains secret. |
| Secret password | Yes  | The established password remains secret. |
| Authentication App  | Yes  | The app is able to authenticate the browser and the issuer. |
| Authentication Browser  | Yes  | The browser is able to authenticate the app and the issuer. |
| Authentication Issuer  | Yes  | The issuer is able to authenticate the app and the browser. |

Query not attacker(check_reach_app[]) is false.

Query not attacker(check_reach_user[]) is false.

Query not attacker(check_reach_issuer[]) is false.

Query not attacker(free_code[]) is false.

Query not attacker(free_password[]) is true.

Query inj-event(appCompletesProtocol(m_96,m_97,m_98,m_99,m_100,m_101,m_102)) ==> inj-event(userSendsLastMessageToApp(m_96,m_97,m_98)) && inj-event(issuerSendsLastMessageToApp(m_99,m_100,m_101,m_102)) is false.

Query inj-event(userCompletesProtocol(m_96,m_97,m_98,m_99,m_100,m_101)) ==> inj-event(appSendsLastMessageToUser(m_100,m_101)) && inj-event(issuerSendsLastMessageToUser(m_96,m_97,m_98,m_99)) is true.

Query inj-event(issuerCompletesProtocol(m_96,m_97,m_98,m_99,m_100,m_101)) ==> inj-event(appSendsLastMessageToIssuer(m_99,m_100,m_101)) && inj-event(userSendsLastMessageToIssuer(m_96,m_97,m_98)) is false.

The lack of issuer authentication leads to a possible mixup attack explained in the following msc.

![MSC of ...](/msc/msc_attack_app_auth.png)

# SOIDC - Proposed Fix

## Proposed Version

Fixing the code leak and issuer authentication may be achieved by adding the issuer identity to the code during its transfer through the browser. 
By using the fix, the code verifier is no longer needed.

## Results

| Property  | Holds | Note |
| ------------- | ------------- | ------------- |
| Finish App | Yes  | The app finishes the protocol. |
| Finish Browser | Yes  | The browser finishes the protocol. |
| Finish Issuer | Yes  | The issuer finishes the protocol. |
| Secret code | Yes  | The established code remains secret. |
| Secret password | Yes  | The established password remains secret. |
| Authentication App  | Yes  | The app is able to authenticate the browser and the issuer. |
| Authentication Browser  | Yes  | The browser is able to authenticate the app and the issuer. |
| Authentication Issuer  | Yes  | The issuer is able to authenticate the app and the browser. |



