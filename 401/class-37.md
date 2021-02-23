# Class 07

## Review, Research, and Discussion

1. _Write the following steps in the correct order:_

    - Register your application to get a client_id and client_secret

    - Ask the client if they want to sign in via a third party

    - Redirect to a third party authentication endpoint

    - Make a request to a third-party API endpoint

    - Receive authorization code

    - Make a request to the access token endpoint

    - Receive access token

1. _What can you do with an authorization code?_

    - The authorization code is a temporary code that the client will exchange for an access token. The code itself is obtained from the authorization server where the user gets a chance to see what the information the client is requesting, and approve or deny the request.

1. _What can you do with an access token?_

    - Access tokens are the thing that applications use to make API requests on behalf of a user. The access token represents the authorization of a specific application to access specific parts of a user's data. Access tokens must be kept confidential in transit and in storage.

1. _What’s a benefit of using OAuth instead of your own basic authentication?_

    - While the OAuth 2 “password” grant type is a more complex interaction than Basic authentication, the implementation of access tokens is worth it. Managing an API program without access tokens can provide you with less control, and there is zero chance of implementing an access token strategy with Basic authentication.

| Term      | Description |
| ----------- | ----------- |
| Client ID  |The client_id is a public identifier for apps.|
| Client Secret|The client_secret is a secret known only to the application and the authorization server.|
| Authentication Endpoint  |Endpoint authentication is a security mechanism designed to ensure that only authorized devices can connect to a given network, site or service.|
| Access Token Endpoint  |The token endpoint is where apps make a request to get an access token for a user. This section describes how to verify token requests and how to return the appropriate response and errors. Authorization Code.|
| API Endpoint      ||For APIs, an endpoint can include a URL of a server or service. Each endpoint is the location from which APIs can access the resources they need to carry out their function.
| Authorization Code |An authorization code is an alphanumeric password that authorizes its user to purchase, sell or transfer items, or to enter information into a security-protected space.|
| Acess Token      |In computer systems, an access token contains the security credentials for a login session and identifies the user, the user's groups, the user's privileges, and, in some cases, a particular application.|

## Bearer Authorization

- JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object.

- This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

- Although JWTs can be encrypted to also provide secrecy between parties, we will focus on signed tokens.

- Signed tokens can verify the integrity of the claims contained within it, while encrypted tokens hide those claims from other parties.

- Authorization is the most common scenario for using JWT.

- Information Exchange. JSON Web Tokens are a good way of securely transmitting information between parties. Because JWTs can be signed—for example, using public/private key pairs—you can be sure the senders are who they say they are.

- JSON Web Token structure - 3 parts. Header, Payload, Signature

- In authentication, when the user successfully logs in using their credentials, a JSON Web Token will be returned.

- Since tokens are credentials, great care must be taken to prevent security issues. In general, you should not keep tokens longer than required.

[back to README](../README.md)
