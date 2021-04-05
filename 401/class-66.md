# Class 36

## Review, Research, and Discussion

1. What are the advantages of storing tokens in “Cookies” vs “Local Storage”

    - Local Storage

      Pros: It's convenient.

        - It's pure JavaScript and it's convenient. If you don't have a back-end and you're relying on a third-party API, you can't always ask them to set a specific cookie for your site.

        - Works with APIs that require you to put your access token in the header like this: Authorization Bearer ${access_token}.

    - Cookies

      Pros: The cookie is not accessible via JavaScript; hence, it is not as vulnerable to XSS attacks as localStorage.

      - If you're using httpOnly and secure cookies, that means your cookies cannot be accessed using JavaScript. This means, even if an attacker can run JS on your site, they can't read your access token from the cookie.

      - It's automatically sent in every HTTP request to your server.

1. Explain 3rd party cookies.

    - Third-party cookies are those created by domains other than the one the user is visiting at the time, and are mainly used for tracking and online-advertising purposes. They also allow website owners to provide certain services, such as live chats.

1. How do pixel tags work?

    - A tracking pixel (also called 1x1 pixel or pixel tag) is a graphic with dimensions of 1x1 pixels that is loaded when a user visits a webpage or opens an email. Because it is so small, it can hardly be seen by visitors of a website or email recipients. These tracking pixels are partly or fully designed to be transparent, or camouflaged in the background color of the website so that they don't stand out to users. Users are usually not supposed to see the tracking pixel. The focus is mainly on the processes that are initiated by downloading the tracking pixel.

      Tracking pixels within the source code might look like this:

      ```html
      <img style="“position: absolute;" src="“Tracking">
      <img style="“display: none”;" src="“Tracking">
      <img src="“Tracking" width="“0”" height="“0”">
      ```

      The tracking pixel URL is the memory location on the server. When the user visits a website, the image with the tag is loaded from this server. Optical properties such as visibility, or a very small size are defined using the style attribute.

| Term      | Description |
| ----------- | ----------- |
|cookies|An HTTP cookie is a small piece of data stored on the user's computer by the web browser while browsing a website. Cookies were designed to be a reliable mechanism for websites to remember stateful information or to record the user's browsing activity.|
|authorization|Authorization is the function of specifying access rights/privileges to resources, which is related to general information security and computer security, and to access control in particular.|
|access control|In the fields of physical security and information security, access control is the selective restriction of access to a place or other resource while access management describes the process.|
|conditional rendering|Conditional rendering is a term to describe the ability to render different user interface (UI) markup if a condition is true or false. In React, it allows us to render different elements or components based on a condition.|
