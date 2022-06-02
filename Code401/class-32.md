# Reading Assignment 32

## Permissions & PostgreSQL

---

### DRF Permissions

- Together with authentication and throttling, permissions determined whether a request should be granted or denied access.
- Permission checks are always run at the start of the view before any other code is allowed to run. They typically check using the authentication information in the user and auth properties to determine access.
- The simplest style would be to deny access to all unauthenticated users and allow authenticated users.
- A less strict style is to allow access to authenticated users, and read-only access to unauthenticated users.
- Permissions in a REST framework are defined as a list of permission classes.
- When a check fails, either a 403 or 401 status code is returned according to a short list of rules.
- REST framework also supports object-level permissioning and are used to determine if a user can act on a certain object, often a model instance.
  - There are limitations to using object level permissions, in that generic views don't automatically apply to them for performance reasons when returning a list of objects in a queryset.
  - Often when using OLPs, you'll want to filter the queryset to only objects they are permitted to view.
- To set the default permisson policy globally, you can put it in settings.py for Django.
  - If not specified, it defaults to open access
  - It can also be set on a per-view basis.
- API Reference;
  - AllowAny is open access to authenticated or unauthenticated
  - IsAuthenticated allows access only to authenticated users
  - IsAdminUser allows access only to users with admin level access
  - IsAuthenticatedOrReadOnly allows read-only access to unauthenticated users and full access to authenticated users.
- You can also set custom permissions by overriding BasePermission and implement one or both of two methods.
- There is also a list of third party packages available for use with Django Rest Framework.
