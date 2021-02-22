# Class 06

## Review Research and Discussion

1. _Explain what a “Singleton” is (in Computer Science terms)_

    - In software engineering, the singleton pattern is a software design pattern that restricts the instantiation of a class to one "single" instance. This is useful when exactly one object is needed to coordinate actions across the system. The term comes from the mathematical concept of a singleton.

1. _Explain how the Singleton pattern can be used with Node modules, specifically with classes_

    - You can use the Singleton pattern with classes to make 1 instance of a class. This way, you can use that single instance for multiple things instead of making a new instance.

    - When using with node, modules are cached after the first time they are loaded.

    ```javascript
    class Singleton {
      constructor() {
        this.message = 'I am an instance';
      }
    }
    module.exports = new Singleton();
    ```

    - The important part of this is that we are only exporting the instance of the class instead of the class. Node.js will cache and reuse the same object each time it's required.

1. _If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it_

    - I'm looking into this still.

| Term      | Description |
| ----------- | ----------- |
| Router Middleware  |Router-level middleware works in the same way as application-level middleware, except it is bound to an instance of express.Router().|
| Dynamic Module Loading |Dynamic loading is a mechanism by which a computer program can, at run time, load a library (or other binary) into memory, retrieve the addresses of functions and variables contained in the library, execute those functions or access those variables, and unload the library from memory.|
| Singleton Pattern  |In software engineering, the singleton pattern is a software design pattern that restricts the instantiation of a class to one "single" instance. This is useful when exactly one object is needed to coordinate actions across the system.|
| Mock Testing  |A mock is a test double that stands in for real implementation code during the unit testing process.|
| CRUD -> REST Method Matches  |

```javascript
Create = PUT with a new URI
         POST to a base URI returning a newly created URI
Read   = GET
Update = PUT with an existing URI
Delete = DELETE
```

## Authentication

### Securing Passwords

- Hashing is the greatest way for protecting passwords and considered to be pretty safe for ensuring the integrity of data or password.

- Cryptographic hash algorithms MD5, SHA1, SHA256, SHA512, SHA-3 are general purpose hash functions, designed to calculate a digest of huge amounts of data in as short a time as possible.

- The benefit of hashing is that if someone steals the database with hashed passwords, they only make off with the hashes and not the actual plaintext passwords.

- General-purpose hash function designed for speed,because they are often used to calculate checksum values for large data sets and files, to check for data integrity.

- Using a modern computer one can crack a 16 Character Strong password in less than an hour, thanks to GPU.

- Hash functions have infinite input length and a predefined output length, so there is inevitably going to be the possibility of two different inputs that produce the same output hash.

- To overcome such issues, we need algorithms which can make the brute force attacks slower and minimize the impact.

- Such algorithms are PBKDF2 and BCrypt, both of these algorithms use a technique called Key Stretching

## Basic Auth

- In the context of an HTTP transaction, `basic access authentication` is a method for an HTTP user agent to provide a user name and password wihen making a request.

- BA is the simplest technique for enforcing access controls to web resources because it does not require cookies, session indetifiers, or login pages; rather, HTTP BA uses standard fields in the HTTP header.

[back to README](../README.md)
