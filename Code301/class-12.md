# Reading Assignment 12

## CRUD

---

### Status Codes Based On REST Methods

---

- In your own words, describe what each group of status code represents:
  - 100’s = Codes in the 100s are informational and meant to tell a client that the request has been recieved and the server will try to process it.
  - 200’s = Codes in the 200s are codes indicating success and are meant to tell a client that the request was accepted.
  - 300’s = Codes in the 300s are codes indicating that the requested data isn't at that location anymore and a new request at the new location is required.
  - 400’s = Codes in the 400s are client error codes that indicate that something about the server request was invalid, such as a timeout, wrong URL or missing authentication.
  - 500’s = Codes in the 500s are server error codes that indicate a problem with the server, typically an overloaded or unreachable server. Sometimes, it can refer to an error causing request.
- What is a status code 202?
  - The request was acceppted and is often used in asynchronous processing. It tells a client that the request was accepted and will send the data when it is done processing.
- What is a status code 308?
  - A permanent redirect that tells the client to use another URL to access the resource and not to use the current URL anymore.
- What code would you use if an update didn’t return data to a client?
  - 204 for No Content
- What code would you use if a resource used to exist but no longer does?
  - If the data is being moved somewhere else, 307 for a temporary redirect, and 308 for a permanant redirect. IF the data used to exist and doesn't anymore without knowing where it now is, 410.
- What is the ‘Forbidden’ status code?
  - 403

### Build A REST API With Node.js, Express, & MongoDB

---

- Why do we need to pull our MongoDB database string out of our server and put it into our .env?
  - Mostly security purposes as it contains data about the user and the database password.
- What is middleware?
  - Code that runs before the request reaches one of the routes.
- What does app.use(express.json()) do?
  - Let the server accept JSON in the body.
- What does the /:id mean in a route?
  - A parameter we can access.
- What is the difference between PUT and PATCH?
  - PUT updates an entire object in memory, PATCH updates only the relevent part of the object.
- How do you make a default value in a schema?
  - By passing `default` as one of the keys and whatever you want the default to be as the value.
- What does a 500 error status code mean?
  - Something on the server failed.
- What is the difference between a status 200 and a status 201?
  - 201 defined that the object was sucessfully created, and is more specific than the generic success message that 200 is.
