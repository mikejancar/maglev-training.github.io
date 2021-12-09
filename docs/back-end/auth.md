---
sidebar_position: 2
---

# Authentication / Authorization

For _now_, I'm thinking we will use Github authentication. Eventually I'd like us to have our own OIDC/Oauth2 implementation, but I don't want to get side tracked with security yet.

## External Users

Will create accounts by logging in with Github.

## Internals (Service Accounts)

I considered using Azure AD for service-service communication, because it would have been easier, but I think using Kubernetes RBAC and principles will be the right way to go to stick with our "portable cloud native" guidance.
