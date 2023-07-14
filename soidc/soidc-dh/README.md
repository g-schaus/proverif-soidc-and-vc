# SOIDC - With Diffie Hellman Key Exchange

The model is based on the version found [here](/soidc/soidc) and uses the HTTPS handshake using Diffie Hellman as explained [here](/https).

# Results Without Fix

| Property  | Holds in Simple | Holds in DH | Time of DH | Note on DH |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| Finish App | Yes  | Yes | ... | The app finishes the protocol. |
| Finish Browser | Yes  | Yes | ... | The browser finishes the protocol. |
| Finish Issuer | Yes  | Yes | ... | The issuer finishes the protocol. |
| Authentication App | Yes | Yes  | 1h15 | The app is able to authenticate the browser and the issuer. |
| Authentication Browser | Yes | Yes | 1h15 | The browser is able to authenticate the app and the issuer. |
| Authentication Issuer  | No | ? | 2h30 | Fatal Error: out of memory, 2.553 rules left |
