# Reading Assignment 28

## Django CRUD and Forms

---

### Django Forms

- You an use HTML forms with Django to make CRUD requests and they are a relatively secure way to share data with a server.
- Just like other tasks with Django, using a form follows some of the same techniques where the view gets a request, performs the necessary actions then returns an HTML page in a template.
- Django's form handling does a number of things, such as;
  - Display a default form when requested by a user the first time
  - Receive data from a submit request and bind it to the form
  - Clean and validate the data
  - If any data is invalid, re-display the form with error messages and user-populated info
  - If data is valid, perform required actions
  - Then, when all actions are done, redirect to another page.
- The most fundamental tool with Django for this task is the Form class.
  - It specifies the fields in the form and other key attributes and rules about the data they accept
  - When declaring a Form, it follows a similar syntax to that of a Model.
  - The data is stored in the forms.py file.
  - One way to validate data is to override the `clean_<fieldname>()` method for the field you want to check.
- However, while the above information is useful for creating a new form, if all you need is a form to map the fields for a single Model, then most of the work is already done for you and you could far more easily use the ModelForm helper class.
