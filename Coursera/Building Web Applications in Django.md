## Week 1

## MVC : Model View Controller

- Model : Data in the data store
- View  : HTML, CSS.. Look and feel of the app
- Controller : Code which does thinking and decision making

## Django Data Models

```python
from django.db import connection
connection.queries()
```
- The above code show under hood SQL code ran by ORM.
Methods of ***`model.objects`*** : ***`values(), filter(), update(), delete().`***
- `values()` has `order_by()` method to sort values.
- pass -ve sign inside `order_by()` method to get values in descending order.

## Django Migrations

- `makemigrations` : reads all models.py from apps specified in the settings file and creates migration files.
- `migrate` : reads all migrations folder from the apps and creates table in database as per migration files.
- Tables are created with `<app_name>_<model_name>` nomenclature inside the database when migrate command is executed.