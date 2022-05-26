# Reading Assignment 31

## Django REST Framework & Docker

---

### Beginner’s Guide to Docker

- Docker is a way to isolate and run applications regardless of operation system, language, packages or databases.
- The downside to using it is the complexity it can operate at, but a little knowledge goes a long way.
- Docker is essentially a bunch of Linux containers which are a type of virtualization.
- Virtualization and more specifically virtual machines was an early solution to the problem of needing multiple programmers on a single machine.
- A good analogy is that of a house and an apartment;
  - A virtual machine is a house, stand-alone, with their own infrastructure
  - Docker is like an apartment, it shares common infrastructure but is sized to meet the needs of the owner.
- The way we have been doing it, through virtual environments are good, but they can only be used for python packages and can't run a production database or other services.
- When starting off, understanding Images and Containers are important concepts to grasp;
  - An image is a snapshot of the code at a specific time
  - A container is the final code.
- The `Dockerfile` is the list of instructions to create the image
- Images can be layered
- Containers are the running instance of an image
- `docker-compose.yml` controls how the container runs

---

### Django for APIs - Library Website

- The Django REST framework works alongside the Django web framework to build web APIs.
- The most important takeaway from the article is that Django creates webpages, while Django REST creates web APIs.
- Once the REST API is installed, you need to include it in Django's settings.py under Installed Apps
- Under the Django REST framework, the output when going to a url is serialized json data
- The REST framework relies on a model, a url and a serializer file.
- A serializer translates complex data like a queryset or model instance into a format like JSON.
- 
