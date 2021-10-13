## Week 1 : Cookies and Sessions

- cookies are stored in form of dictinoary inside ***request.COOKIES***.
- ***set_cookies()*** method sets the cookie inside the browser, ***max_age*** parameter is used specify the expiration time for the cookie in number of seconds, be default the cookie remains till the browser is closed.
- sessions are stored inside session table as base64 encoded keys.
- similar to cookies session can also be accessed through ***request.session***.

## Week 2 : Users and Authentication

- Can use the next parameter inside django template to redirect to a url after execution of some other url.
***```{% url '<url_name>' %}?next={% url '<url_name>' %}```***
- ***LoginRequiredMixin*** class allows views to be accessed only by loggedin users.
***`from django.contrib.auth.mixins import LoginRequiredMixin`*** 

## Week 3 : Django Forms

- Form values can be prefilled by passing a dictionary with model fields as keys and input values as values to Form class.
- ***validators*** parameters takes list of validation to be applied to a particular field of the model.

## Week 5 : Owned Rows

- Crispy forms styles the form using internal css. Add ***`{% load crispy_form_tags %}`*** on top of the form elements inside html file and add escape while rendering the form data using ***`{{ form| crispy }}`***
- ***crispy_forms*** app need to be present inside ***INSTALLED_APPS***