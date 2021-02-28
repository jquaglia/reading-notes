# Class 11

## Review, Research, and Discussion

1. _Why is access control important?_

    - Access control is important because if you give users access to things that they don't need to use, there is more oppurtunity for things to go wrong. A standard user doesn't need admin privelidges on their company's network.

1. _Describe an application that would need access control._

    - An app that would need access control could be almost anything. How about a company website that has data for public use. A standard user might just want to see the data but an admin may need to update or change the data regularly.

1. _What is a role used for?_

    - Role's are used for access control. They help determine the privelidges that each account has.  

1. _Why is role based access control more scalable than discretionary or mandatory access control?_

    - Roles based access control is more scalable because there is no case by case basis. If someone needs different access, you can just add the role they need to their account. No need to manually assign everything they need access to.

| Term      | Description |
| ----------- | ----------- |
| Role Based Access Control | role-based access control or role-based security is an approach to restricting system access to authorized users. |
| Authorization | Authorization is a security mechanism used to determine user/client privileges or access levels related to system resources, including computer programs, files, services, data and application features. Authorization is normally preceded by authentication for user identity verification. |
| Capablities | A role is a named collection of functional user access. A capability refers to the functions that can be assigned to each user. |

## Event Driven Applications

Event-Driven Programming is a logical pattern that we can choose to confine our programming within to avoid issues of complexity and collision.

### Overview

- Every time you interact with a webpage through it's user interface, an event is happening.

- This can be a click, pressing a key, hovering your mouse.

- Event driven programming makes use of the following concepts:

  - An event handler is a callback function that will be called when an event is triggered.

  - A main loop listens for event triggers and calls the associated event handler for that event.

### EventEmitter

- Node.js natively provides us with a module called EventEmitter that allows us to get started incorporating event-driven programming in our project right away.

- It's not too difficult to create and you can find faster versions published on npm.

- You access the EventEmitter class through the `events` module. Once imported we’ll need to create a new object from the class to start using it.

```javascript
const EventEmitter = require('events').EventEmitter;
const myEventEmitter = new EventEmitter;
```

- Use the `on` method to trigger an event.

- EventEmitter has an `emit` mthod that we can use to trigger the event.

### Removing Listeners

- to remove event listeners we can use the `removeListener` or `removeAllListeners` method.

### Object Oriented Programming + Event-Driven Programming

- These two make for a very valuable combination in a wide variety of situations and I think it can be beneficial to understand and conceptualize why.

- The Object Oriented approach promotes the idea that all behavior of an individual unit (or object) be handled from code within that unit.

- Using this approach, applications are built with many different units that all speak to and interact with each other.

- We might have an object whose sole purpose is to process the incoming and outgoing mail messages for our client.

- This object would contain all of its own behavioral functions.

- We might have a `sendMail` function that delivers our mail to a server. We might also have a `receiveMail` function that tells the server to deliver us any new mail it has for us. We’ll call the object responsible for these server interactions our `Mailbox`.

- Now if we are building other units that want to make use of our sendMail function, they can access it through `Mailbox.sendMail`.

- But what happens when we later-on decide we also want to log the mail every time we send it?

- We now need to either modify our sendMail function to incorporate this behavior, or create another function that is triggered immediately after the sendMail function.

- In which case the object responsible for triggering the sendMail function must be sure to also trigger the log function.

- This could get out of hand when we begin to scale our app.

- This is where we can make use of Event-driven programming. By registering event listeners we can actually reverse the flow of communication between our objects.

- Rather than on object needing to reach inside another object to trigger a function, our objects can just emit events and whichever objects are listening to those event will process it in the way they have been told to.

- The source of an objects behavior is now entirely contained within itself, rather than needing to be accessed by external objects.

[back to README](../README.md)
