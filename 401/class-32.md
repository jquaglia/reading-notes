# Class 02

## Review, Research, Discussion

1. _What’s the difference between `PUT` and `PATCH`?_

    - `PUT` method uses the request URI (Uniform Resource Indentifier) to supply a modified version of the requested resource

    - `PATCH` method supplies a set of instructions to modify the resource

    - Another difference is that when you want to update a resource with `PUT` request, you have to send the full payload as the request whereas with `PATCH`, you only send the parameters which you want to update.

        - [Link to Wikipedia info on this](https://en.wikipedia.org/wiki/Patch_verb#:~:text=The%20main%20difference%20between%20the,instructions%20to%20modify%20the%20resource.)

1. _Provide links to 3 services or tools that allow you to “mock” an API for development like `json-server`_

    1. [Nock](https://github.com/nock/nock)

    1. [Postman Mock Server](https://learning.postman.com/docs/designing-and-developing-your-api/mocking-data/setting-up-mock/)

    1. [Mockoon](https://mockoon.com/)

1. _Compare and contrast Swagger and APIDoc.js_

    - they both create documentation for your API

    - swagger is built around OpenAPI Specification that allows you to design, build, document, and consume REST APIs

    - apiDoc creates a documentation from API annotations in your source code

    - swagger-ui is more [popular](https://www.npmtrends.com/apidoc-vs-swagger-ui)

    - apidocjs and swagger both require documentation content on implemented method as customized comment data.

        - [Swagger Docs](https://swagger.io/docs/specification/about/)

        - [APIDocjs Docs](https://apidocjs.com/)

1. _Which HTTP status codes should be sent with each type of (un)successful API call?_

    - Informational responses (100–199)

    - Successful responses (200–299)

    - Redirects (300–399)

    - Client errors (400–499)

    - Server errors (500–599)

    -[MDN Docs on HTTP status codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)

1. _Compare and contrast SOAP and ReST_

    - SOAP (Simple Object Access Protocol)

    - REST (Representational State Transfer)

    - Both web service communication protocols

    - REST operates through a solitary, consistent interface to access named resources. It’s most commonly used when you’re exposing a public API over the Internet.

    - SOAP, on the other hand, exposes components of application logic as services rather than data. Additionally, it operates through different interfaces.

    - REST accesses data while SOAP performs operations through a more [standardized set](http://blog.smartbear.com/apis/understanding-soap-and-rest-basics/) of messaging patterns

        - [Great Info on REST vs SOAP](https://stackify.com/soap-vs-rest/)

| Term      | Description |
| ----------- | ----------- |
| Web Server  |   A web server is server software, or a system of one or more computers dedicated to running this software, that can satisfy client HTTP requests on the public World Wide Web or also on private LANs and WANs|
| Express     |   Express.js, or simply Express, is a back end web application framework for Node.js, released as free and open-source software under the MIT License. It is designed for building web applications and APIs|
| Routing     |   Routing is the process of selecting a path for traffic in a network or between or across multiple networks|
| WRRC        |   Web Request Response Cycle - cycle of essentially how the web works between different machines|

## Express

- Express is the most popular Node web framework

- Underlying library for a number of other popular [Node web frameworks](https://expressjs.com/en/resources/frameworks.html)

- Provides mechanisms to:

  - Write handlers for requests with different HTTP verbs at different URL paths (routes).

  - Integrate with "view" rendering engines in order to generate responses by inserting data into templates.

  - Set common web application settings like the port to use for connecting, and the location of templates that are used for rendering the response.

  - Add additional request processing "middleware" at any point within the request handling pipeline.

- [MDN Docs on Intro to Node/Express](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction)

## NPM

- npm is the world's largest software registry

- used to share, borrow, use packages and manage private development too

- 3 distinct components

  1. the website

  1. teh Command Line Interface (CLI)

  1. the registry

## TDD

- TDD (Test Driven Development)

- refers to a style of programmin in which three activities are tightly interwoven: coding, testing, and design

- a benefit is that many teams report significant reductions in defect rates, at the cost of a moderate increase in initial development effort

- the same team tend to report that these overheads are more than offset by a reduction in effort in projects' final phases

## CI/CD

- CI/CD (Continuous Integration, Continuous Delivery)

- CI ensures everyones changes will integrate to main branch

- does this via tests to determine if branch will merge correctly

- paves the way for CD

- Continuous Delivery is the process of developing code so that you could release it at any time

- Continuous Deployment is an extension of this. It is a process that allows you to actually deploy newly developed features into production with confidence

[back to README](README.md)
