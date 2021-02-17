# Class 13

## Sending Form Data

- Once the form data has been validated on the client-side, it is okay to submit the form.

### Client/ Server Architecture

At it's most basic, the web uses a client/server architecture that can be summarized as follows. A client (usually a web browser) sends a request to a server (most of the time a web server like Apache, Nginx, IIS, Tomcat, etc.), using the HTTP protocol. The server answers the request using the same protocol.

### On the client side: defining how to send the data

The `form` element defines how the data will be sent.

#### The action attribute

- The `action` attribute defines where the data gets sent. Its value must be a valid relative or absolute URL. If this attribute isn't provided, the data will be sent to the URL of the page containing the form -- the current page.

#### The method attribute

- The `method` attribute defined how data is sent. The HTTP protocol provides several ways to perform a request; HTML form data can be transmitted via a number of different methods, the most common being the `GET` method and the `POST` method.

The Get Method

- used by the browser to ask the server to send back a given resource. The data is appended to the URL as a series of name/value pairs.

The Post Method

- the post method is a little different. It's the method the browser uses to talk to the server when asking for a response that takes into account the data provided in the body of the HTTP request. If a form is sent using this method, the data is appended to the body of the HTTP request.

- When the form is submitted using the `POST` method, you get no data appended to the URL.

[back to README](../README.md)
