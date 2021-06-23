## Week 1: Data Models

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
- ***`values()`*** has ***`order_by()`*** method to sort values.
- pass -ve sign inside ***`order_by()`*** method to get values in descending order.

## Django Migrations

- ***`makemigrations`*** : reads all models.py from apps specified in the settings file and creates migration files.
- ***`migrate`*** : reads all migrations folder from the apps and creates table in database as per migration files.
- Tables are created with ***`<app_name>_<model_name>`*** nomenclature inside the database when migrate command is executed.

## Week 2: URL Routing

- To design URL's you can create URLconf module which is pure python code and is mapping between URL path expressions to python functions i.e views.
```python
from django.views.generic import TemplateView
path('', TemplateView.as_view(template_name='views/main.html')) # Inside urlpatterns list
```
- The above code can be used display static webpage as a view.

## Django Views

- ***`request.GET`*** dict stores all the get request parameters.
- use ***`from django.utils.html import escape`*** to avoid cross site scripting.
- ***`<int:guess>`*** inside url path, pass parameter guess inside view function.
- Create class based view using ***`from django.views import View`*** inherited class can have ***`get() and post()`*** methods with self as first param and request as second param.

## Django Templates

```python
from django.shortcuts import render
render(request, template, context)
```
- The above render function will allow to use context inside the template.
- To include templates inside namespace, place the template html inside ***`templates/<app_name>`*** directory.