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

## Week 2: Django Views

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

## Django Template Language

- It does internal escaping on the elements, i.e JS code will not get executed if passed as context to HTML.
- ***`{{ ele }}`*** : substitution of value. modifiers like **safe, inttocomma** can be used after `|` in the block.
- ***`{% for ele in list %}`*** : code, logic, blocks

## Template Inheritance

- ***`{% extends '<template_name> '%}`*** extends a base template into a new template.

## URL Mapping / Reversing

- ***`"{% url '<app_name>:<view_name>' <id_param> %}"`*** : this provides functionality for url reversing, The **view name** has to be specified as **name** paramter inside the **url()** function
- can use **namespace** param to refer to an app inside project. This namespace has to be used inside ***`urls.py`**** of the django project only.
- In order to use the url name mappings inside python files pass them as arguments to **reverse()** and **reverse_lazy()** functions imported from **django.urls**.

## Week 3 : Django Generic Views

- ***`__init__`*** is constructor method and ***`__del__`*** is destructor method.
- Object get destroyed when point of reference for the given variable name changes.
- model name can be extracted by ***`<model_object>._meta.verbose_name`***
- ***`from django.views import generic`*** **generic.ListView** class can be extend inside a view class to make the class view as generic, but require to pass the model inside **`model`** variable.