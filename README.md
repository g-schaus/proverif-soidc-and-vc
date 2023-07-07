# Solid OpenID Connect and VC-based Third Authentication Protocols
This repository contains different proverif models depicting Solid Open ID Connect and an alternate VC-based suggestion.
All accessible and verified models are listed below:

| Variant  | Vulnerable | Note |
| ------------- | ------------- | ------------- |
| HTTPS  | No  | HTTPS should only authenticate in one direction, works. |
| HTTPS using DH  | No  | HTTPS should only authenticate in one direction, works. |
| SOIDC  | Yes  | Attack is provided. |
| SOIDC using DH  | ?  | Verification termination issues. |
| SOIDC with late HS  | Yes  | Attack is provided. |
| SOIDC proposed fix  | No  | Works. |
| STS  | No  | Works. |
| VC based version  | No  | Works. |
