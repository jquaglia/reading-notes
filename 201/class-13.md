# Class 13

## The past present & future of local storage for web applications

### Storage in Web

Cookies have 3 huge downsides.

- Cookies are included with every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over

- Cookies are included with every HTTP request, thereby sending data unencrypted over the internet (unless your entire web application is served over SSL)

- Cookies are limited to about 4 KB of data — enough to slow down your application, but not enough to be terribly useful

Ideal web storage would have

- a lot of storage space

- on the client

- that persists beyond a page refresh

- and isn't transmitted to the server

### What is HTML5 storage

- It's a way for web pages to store named key/value pairs locally, within the client web browser.

- From js code, access HTML5 storage through `localStorage` object on the global window object.

- data is always stored as a string. (this is why we need to use `parseInt()`)

- data is stored in named key value pairs.

### Beyond named key-value pairs: competing visions

- Web SQL database is suppported in 4 browsers

  - safari

  - chrome

  - opera

  - iphone

  - android

- One issue is that SQL doesn't have a standard that everyone follows, they all use their own specification

- IndexedDB API is another competing vision for advanced, persistent, local storage for web apps.

- this has only been implemented in a beta version of firefox 4 (Mozilla said they will never use Web SQL)

[back to README](../README.md)
