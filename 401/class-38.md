# Class 08

## Review, Research, and Discussion

1. _When is Basic Authorization used vs. Bearer Authorization?_

    - Basic Authentication is used when creating an account for the first time. Sent as user ID/password pairs. This is not secure as the user ID and password are passed over the network as clear text.

    - Bearer Auth has tokens that are used for authentication. The client must send this token in the Authorization header when making requests. This is more secure than basic as the tokens are encrypted.

1. _What does the JSON Web Token package do?_

    - the JSON Web Token package helps create and manage JWTs for you to use in a server/api. You can do many things with this library.

1. _What considerations should we make when creating and storing a SECRET?_

    - You probably don't want to store it anywhere in plaintext.

| Term      | Description |
| ----------- | ----------- |
| encryption  |In cryptography, encryption is the process of encoding information. This process converts the original representation of the information, known as plaintext, into an alternative form known as ciphertext. Ideally, only authorized parties can decipher a ciphertext back to plaintext and access the original information.|
| token | token is the encrypted key used to verify who someone is in Bearer Auth|
| bearer | bearer auth involves security tokens called bearer tokens. The name “Bearer authentication” can be understood as “give access to the bearer of this token.”  |
| secret | This is the thing that makes bearer auth work. It's a secret part to the token that isn't publicly known. It helps to encrypt the rest of the token. |
| JSON Web Token   |JSON Web Token is an Internet proposed standard for creating data with optional signature and/or optional encryption whose payload holds JSON that asserts some number of claims. The tokens are signed either using a private secret or a public/private key.|

## Role Based Access Control

- RBAC is an approach to restricting system access to authorized users.

- Each user is only given access to the things that are deemed necessary for them.

Benefits of RBAC?

- With proper implementation, the assignment of access rights becomes systematic and repeatable.

- Much easier to audit user rights, and to correct any issues identified.

RBAC Implementation

- Inventory your systems

- Analyze your workforce and create roles

- Assign people to roles

- Never make one-off changes

- Audit

[back to README](../README.md)
