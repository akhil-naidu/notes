Express is a Fast, unopinionated, minimalist web framework for Nodejs. It is used to create a http server and listens on a particular port. The possibilites we acheive in using such frameworks are limitless. We can create an entire MVC structured frameworks on top of it, but we would like to use it as a API server.

Express provides us with an express class with multiple utility functions and methods, the list is as follows.
1. express is a functions which returns us an object, that contains multiple methods.
2. Few of the important mentods are `use`, `listen`, `get`, `post`, and other HTTP methods.
3. `express` also consists a `Router` method, which can be triggered using `express.Router()` which provides us a `router` that can be used for HTTP methods. 
4. Any data that is shared via browser or http are in strings. In order to conver the string to it's valid format we require a body-parser. Express also provides a `body-parser` by default. We can use the following command `app.use(express.json({ extended: true }));` to use the default body parser provided by express.
