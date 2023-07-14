# SOIDC - With Diffie Hellman Key Exchange

The model is based on the version found [here](/soidc/soidc-lateHS) and uses the HTTPS handshake using Diffie Hellman as explained [here](/https).

# DH Results Compared To Simple

| Property  | Holds in Simple | Holds in DH | Time of DH | Note on DH |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| Finish App | Yes  | Yes | 0h05 | The app finishes the protocol. |
| Finish Browser | Yes  | Yes | 0h05 | The browser finishes the protocol. |
| Finish Issuer | Yes  | Yes | 0h05 | The issuer finishes the protocol. |
| Authentication App | No | ?  | 0h45 | Fatal Error: out of memory, 7.060 rules left |
| Authentication Browser | Yes | ? | 1h00 | Fatal Error: out of memory, 29.496 rules left |
| Authentication Issuer  | No | ? | 1h15 | Fatal Error: out of memory, 12.763 rules left |

# DH Results With Fix Compared To Simple

| Property  | Holds in Simple | Holds in DH | Time of DH | Note on DH |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| Finish App | Yes  | Yes | 0h05 | The app finishes the protocol. |
| Finish Browser | Yes  | Yes | 0h05 | The browser finishes the protocol. |
| Finish Issuer | Yes  | Yes | 0h05 | The issuer finishes the protocol. |
| Authentication App | Yes | Yes  | 0h10 | The app is able to authenticate the browser and the issuer. |
| Authentication Browser | Yes | Yes | 0h10 | The browser is able to authenticate the app and the issuer. |
| Authentication Issuer  | Yes | Yes | 0h10 | The issuer is able to authenticate the app and the browser. |

# DH Results With Fix (No PKCE) Compared To Simple

| Property  | Holds in Simple | Holds in DH | Time of DH | Note on DH |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| Finish App | Yes  | Yes | 0h05 | The app finishes the protocol. |
| Finish Browser | Yes  | Yes | 0h05 | The browser finishes the protocol. |
| Finish Issuer | Yes  | Yes | 0h05 | The issuer finishes the protocol. |
| Authentication App | Yes | Yes  | 0h10 | The app is able to authenticate the browser and the issuer. |
| Authentication Browser | Yes | Yes | 0h10 | The browser is able to authenticate the app and the issuer. |
| Authentication Issuer  | Yes | Yes | 0h10 | The issuer is able to authenticate the app and the browser. |
