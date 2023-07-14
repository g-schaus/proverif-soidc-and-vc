# SOIDC - With Diffie Hellman Key Exchange

The model is based on the version found [here](/soidc/soidc) and uses the HTTPS handshake using Diffie Hellman as explained [here](/https).

# Results

| Property  | Holds | Note |
| ------------- | ------------- | ------------- |
| Finish App | Yes  | The app finishes the protocol. |
| Finish Browser | Yes  | The browser finishes the protocol. |
| Finish Issuer | Yes  | The issuer finishes the protocol. |
| Authentication App  | Yes  | The app is able to authenticate the browser and the issuer. |
| Authentication Browser  | Yes  | The browser is able to authenticate the app and the issuer. |
| Authentication Issuer  | ? | Fatal Error: out of memory. |

The verification time is quite long  for this version of the protocol:
- Completion Properties take around 1h30 to 2h
- Authentication Properties take aroud 2h30 to 3h

Unfortunately, the issuer was unable to finish verification as the fatal out of memory error occured each time.
