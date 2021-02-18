# Class 04

## Review, Research, and Discussion

1. _Name 3 advantages to Test Driven Development_

    - TDD reduces time spent on rework

    - You are able to identify the errors and problems quickly

    - Writing the tests first requires you to really consider what you want from the code.

1. _In what case would you need to use beforeEach() or afterEach() in a test suite?_

    - If you have some work you need to do repeatedly for many tests, you can use `beforeEach` and `afterEach`.

1. _What is one downside of Test Driven Development?_

    - No silver bullet – Tests help to seek out bugs, but they can not find bugs that you simply introduce within the test code and in implementation code

1. _What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?_

    - The most important difference between `class` and `prototype` based inheritance is that a class defines a type which can be instantiated at runtime, whereas a prototype is itself an object instance.

1. _Why REST?_

    - REST makes efficient use of bandwidth

    - REST supports many data formats

| Term      | Description |
| ----------- | ----------- |
| functional programming  |Functional programming (often abbreviated FP) is the process of building software by composing pure functions, avoiding shared state, mutable data, and side-effects. Functional programming is declarative rather than imperative, and application state flows through pure functions.|
| object-oriented programming|Object-oriented programming (OOP) is a programming paradigm based on the concept of "objects", which can contain data and code: data in the form of fields (often known as attributes or properties), and code, in the form of procedures (often known as methods).|
| class  |Classes are a template for creating objects. They encapsulate data with code to work on that data.|
| `super`  |The super keyword is used to access and call functions on an object's parent.|
| `this`      |In most cases, the value of this is determined by how a function is called (runtime binding).|
| Test Driven Development |Test-driven development is a software development process relying on software requirements being converted to test cases before software is fully developed, and tracking all software development by repeatedly testing the software against all test cases.|
| Jest      |Jest is a JavaScript testing framework maintained by Facebook, Inc. designed and built by Christoph Nakazawa with a focus on simplicity and support for large web applications.|
| Continuous Integration|Continuous Integration (CI) is a development practice where developers integrate code into a shared repository frequently, preferably several times a day.|
| REST| REST is a style that allows the use of HTTP verbs. Representational State Transfer|
| Data Model|A data model (or datamodel) is an abstract model that organizes elements of data and standardizes how they relate to one another and to the properties of real-world entities.|

## Data Modeling

### nosql vs sql

- SQL databases are primarily called as Relational Databases (RDBMS); whereas NoSQL database are primarily called as non-relational or distributed database.

- SQL databases are table based databases whereas NoSQL databases are document based, key-value pairs, graph databases or wide-column stores. This means that SQL databases represent data in form of tables which consists of n number of rows of data whereas NoSQL databases are the collection of key-value pair, documents, graph databases or wide-column stores which do not have standard schema definitions which it needs to adhered to.

- SQL databases have predefined schema whereas NoSQL databases have dynamic schema for unstructured data.

- SQL databases are vertically scalable whereas the NoSQL databases are horizontally scalable. SQL databases are scaled by increasing the horse-power of the hardware. NoSQL databases are scaled by increasing the databases servers in the pool of resources to reduce the load.

- SQL databases uses SQL ( structured query language ) for defining and manipulating the data, which is very powerful. In NoSQL database, queries are focused on collection of documents. Sometimes it is also called as UnQL (Unstructured Query Language). The syntax of using UnQL varies from database to database.

- SQL database examples: MySql, Oracle, Sqlite, Postgres and MS-SQL. NoSQL database examples: MongoDB, BigTable, Redis, RavenDb, Cassandra, Hbase, Neo4j and CouchDb

[back to README](../README.md)
