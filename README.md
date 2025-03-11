# C3_SSO_setup_cfk
Setup IDP (Identity Provider) Azure EntraID 

Step 1 - Establish trust between the IdP and Confluent Platform

You can sign up with a free trial on Azure   Microsoft Azure or login to Azure via Okta https://portal.azure.com/#home

Register OIDC client Application (Add Redirect URi once the CFK cluster is deployed )

Create Client Secret 

Add group claims in Token Configuration.

Capture IDP endpoints required to fetch, authorize, and verify tokens from OpenID Connect metadata document URL

https://login.microsoftonline.com/0893715b-959b-4906-a185-2789e1ead045/v2.0/.well-known/openid-configuration

Token endpoint URL (token_endpoint) : 

Authorization endpoint URL (authorization_endpoint)

JSON Web Key Set (JWKS) URL (jwks_uri)

Issuer URL (issuer)

Example: 



token_endpoint":"https://login.microsoftonline.com/0893715b-959b-4906-a185-2789e1ead045/oauth2/v2.0/token
authorization_endpoint":"https://login.microsoftonline.com/0893715b-959b-4906-a185-2789e1ead045/oauth2/v2.0/authorize
jwks_uri":"https://login.microsoftonline.com/0893715b-959b-4906-a185-2789e1ead045/discovery/v2.0/keys
issuer":"https://login.microsoftonline.com/0893715b-959b-4906-a185-2789e1ead045/v2.0
 

Open image-20250307-102709.png
image-20250307-102709.png
Application Endpoints
 
