# SOIDC - Authorisation Code Grant With Late Handshake

## Vulnerability Proof

The model is based on the version found [here](/soidc/soidc) and simulates an implementation error leading to a delay in the handshake timing.

![MSC of ...](/msc/msc_soidc_lateHS.png)

## Results

| Property  | Holds | Note |
| ------------- | ------------- | ------------- |
| Finish App | Yes  | The app finishes the protocol. |
| Finish Browser | Yes  | The browser finishes the protocol. |
| Finish Issuer | Yes  | The issuer finishes the protocol. |
| Secret code | No  | The established code is leaked to the attacker. |
| Secret password | Yes  | The established password remains secret. |
| Authentication App  | No  | The app is unable to authenticate the browser and the issuer. |
| Authentication Browser  | Yes  | The browser is able to authenticate the app and the issuer. |
| Authentication Issuer  | No  | The issuer is unable to authenticate the app and the browser. |

The lack of app authentication leads to a possible mixup attack explained in the following msc.

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



