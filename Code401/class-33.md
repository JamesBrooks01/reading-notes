# Reading Assignment 33

## Authentication & Production Server

---

### JSON Web Tokens

- A JSON Web Token(JWT) is a standard that defines a compact, self-contained way to transmit info as a JSON object. It can be verified and trusted as it is digitally signed and can signed with a secret or public/private key.
- A signed token verifies the integrity of the claim, while a encrypted token hides the claims from other parties.
- They are most often used for Authorization and Information Exchange.
- It is structured into a Header, Payload, and Signature and are separated by dots.
  - The Header is the type of token and the algorithm used
  - The Payload is the claims which are the statements about the entity and other data. They are further seperated into Registered, Public, and Private.
  - The signature is created by taking the encrypted header, payload, a secret, and the specified algorithm and signing it.
- The output is three base64 strings that are seperated by dots and easily passed in HTML and HTTP environments.
- In authentication, when the user sucessfully logs in a JWT is created and these tokens shouldn't be kept any longer than required for security reasons.
- When the user wants to access a protected route or resource, the JWT would be sent with the request to sometimes be used by the route/resource to verify it's valid.
- The benefits of a JWT over other solutions like a SWT or SAML arel
  - Less verbose and therfore smaller and easier to pass in an HTTP and HTML environment.
  - It can use a public/private key pair.
  - JSON parsers are common in programming languages.

---

### DRF JWT Authentication

- When using a JWT, on the app side, it has a Access Token and a Refresh Token which are used for security purposes.
- For a Django Rest Framework, the recommended library is the SimpleJWT library for `djangorestframework`
- To authenticate and recieve the token, you use the `/api/token` route which only takes POST requests.
  - The response body will have the access token and refresh token.
  - The access token typically lasts 5 minutes before needing to be refreshed with `/api/token/refresh/` and posting the refresh token
  - The refresh token typically lasts 24 hours before the user needs to do a full login again.
- The reasons for having both tokens is for security and permissions reasons.

---

### Django Runserver Is Not Your Production Server

- Using Runserver is not to be used once the app reaches Production. Any server started with `runserver` isn't guaranteed to be performant and hasn't been built with security concerns in mind.
- When the tech reaches production; it should be reliable, well-tested, and been around for a while. It is usually consisting of multiple components, each designed to be good at one thing.
- When a request arrives at the server it should be passed and handled by a dedicated web server like Nginx.
- As an application, it is good at serving static files from the disk like CSS and JS files and handling multiple requests at a time,but if the request isn't for a static file, the webserver will pass it to the next component;
- The application server, which gets the requests and constructs python objects usable by Django. WSGI and Gunicorn are good examples.
- The Django app doesn't actually run like you typically think a server does where it waits for requests and reacts to them. It has a uwsgi.py that has a function to be called by the application server and gets a python object representing the request.
  - The function then calls the code and produces a response object passed to the WSGI server and is translated to a HTTP response and passed to the web server, then delivered to the user.
- In conclusion, when in production, use a web server like Nginx and Gunicorn for WSGI.
  - Or Heroku where you just specify Gunicorn in the Procfile.
