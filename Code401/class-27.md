# Reading Assignment 27

## Django Models

---

### Using Models

- Django accesses and manages data through Python objects referred to as models.
  - These models define the structure of stored data including the types or perhaps the max size, default values, etc.
- The definition of the model is independent of the underlying database, you don't even need to interact with it, just define the structure and write some other code and Django handles the dirty work.
- Before coding the models, it is good practice to take the time to define the data needing to be stored and the relationships between the different objects.
  - When designing the models, it is best to have different models for each object.
- Models are often defined within the `models.py` file and are implemented as subclasses of `django.db.models.Model` and can have fields, methods, and metadata.
  - A field is a column of data that we desire to store in the database table and the number a model can have is arbitrary as is the type.
    - There are numerous arguments and types that can be applied to a field with the arguments often defining rules for what can be in the field and types defining what datatype will be contained within.
  - For the metadata, one of the most useful features is to define the default ordering of the records when a query is made.
  - The models can also have methods, and at minimum it should have a `__str__()` method to return a human-readable string.
  - Another common method is a `get_absolute_url()` for returning a URL for display of individual models on the website.
- Once the models are defined they can be used to create, update, and delete records and then to run queries to get records from the database.
  - To create a record you define an instance of the class then call `save()` on it.
  - You can also use dot notation to alter the fields later. This also uses `save()` to save the modified values.
  - To search for the records you use the model's `objects` attribute.
    - `all()` would return all the records for a model.
    - `filter()` allows you to filter the QuerySet to match a specified text or numeric field against a criteria.
- After defining the models, you need to re-run the database migrations to add them to the database.

---

### Django Admin

- Once you define the models, to add real data you use the Django Admin site.
- The Django admin application can use the models to automatically build a site area to create, view, update, and delete records.
- This can save time during development and makes it easy to test the models and get a feel for if you have the right data.
- It is recommended that the admin application be used for internal data management as it isn't the best interface for all users and reveals unnecessary detail about the model.
- The only mandatory thing to do to use Django Admin application is register the models you add.
- To register the models, you open `admin.py`, import the model names and add the line of code `admin.site.register("name of model")`
- To login to the admin site you need an account with the Staff status enabled.
  - The best way to create a user with all the access needed is with `manage.py`.
    - In the same directory as `manage.py` run the following command to create a superuser
      - `python3 manage.py createsuperuser` and then input a username, email, and strong password.
- Once logged in by going to the `/admin` path and inputting the credentials you can see all the models grouped by application.
  - You can click on records to edit them, or click the add button to create a record of that type.
