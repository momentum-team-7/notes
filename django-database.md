# The Database in a Django Project

## Structure and Function of the Database
In general, a database is an organized collection of information. In a Django app,
the database is based on SQL (Structured Query Language). The database contains tables 
that represent each model and columns in those tables that represent each attribute 
of the model. Each record in the table represents an instance of that model.

Some tools help us visualize the database:
- [Graph Models from Django Extensions](https://django-extensions.readthedocs.io/en/latest/graph_models.html#graph-models) provides a pictoral representation of your models.
    - You will need to install the Graphviz(dot) extension for VS Code in order to view
    the .dot file
- [DB Browser for SQLite](https://sqlitebrowser.org/) allows you to see the data in your DB.

## Querying the Database Using the Django ORM
Django's ORM (Object Relational Mapper) provides us methods that allow us
to communicate with the database using python. These methods return collections called querysets.Using Uptact as an example,
let's look at the `Note` model. 
```python
class Note(models.Model):
    text = models.TextField()
    datetime = models.DateTimeField(auto_now_add=True)
    contact = models.ForeignKey('Contact', related_name='notes', on_delete=models.CASCADE)
```
- `all()` gives us all instances of a model.
```python
    notes = Note.objects.all()
```
- `filter()` allows us to obtain a subset of the instances of a model.
    - You can filter on an attribute of the model.
    ```python
       Note.objects.filter(text="my note")
    ```
    gives us `Note` objects whose text is exactly "my note"
    - __icontains allows us to filter on fields that contain search terms, case insensitive.
    ```python
       Note.objects.filter(text__icontains="word")
    ```
    gives us `Note` objects whose text contains "word" or "Word" or "wOrD"
    - __gte and __lte allow us to filter on values >= or <= a value.
    ```python
       Note.objects.filter(date__lte=datetime.datetime.today())
    ```
    gives us `Note` objects whose datetime is before today.
    - You can filter on a related model instance.
    ```python
       contact = Contact.objects.get(pk=1)
       Note.objects.filter(contact=contact)
    ```
       Gives us all `Note` objects whose contact is the `Contact` with pk=1.
    - You can filter on an attribute of the related model instance as well.
    ```python
       Note.objects.filter(contact__name="John Legend")
    ```
       Gives is all `Note` objects whose contact is the `Contact` object with the name "John Legend."
- `first()` and `last()` give us the first and last records, respectively.


