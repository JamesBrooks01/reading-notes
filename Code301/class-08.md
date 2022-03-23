# Reading Assignment 08

## APIs

---

### API Design Best Practices

---

- What does REST stand for?
  - Representational State Transfer
- REST APIs are designed around a ____.
  - Resources, which refers to any kind of data, or service that can be accessed by a client.
- What is an identifer of a resource? Give an example.
  - A URL that provides a unique identifier for it. For example `https://examplewebsite.com/identifier1/page1`
- What are the most common HTTP verbs?
  - `GET`, `POST`, `PUT`, `PATCH`, `DELETE`
- What should the URIs be based on?
  - Nouns(the resource), and not verbs(the operations on the resources)
- Give an example of a good URI.
  - `https://basic-store.com/orders`
- What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
  - A web API that exposes a large number of small resources. Having a 'chatty' API is considered bad.
- What status code does a successful GET request return?
  - 200
- What status code does an unsuccessful GET request return?
  - 404 if the resource doesn't exist and 204 if the resource exists but has no response body.
- What status code does a successful POST request return?
  - 201
- What status code does a successful DELETE request return?
  - 204
