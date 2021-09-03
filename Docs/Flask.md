- If the main file is not named ***`app.py`*** or ***`wsgi.py`*** then, app name has to be set to ***`FLASK_APP`*** environment variable.
- To run the app use ***`flask run`*** or ***`python -m flask`*** commands from the shell where the app is present.
- To pass dynamic value to a function, pass it as ***`<parameter_name>`*** to the request url, the ***parameter_name*** must be same as functions parameter.
- ***`url_for()`*** function helps to assign url for specific function. It gives functionality of adding dynamic parameteres to the url.
- All static files can be stored inside ***static*** folder inside the package. ***`url_for('static', filename=<file_name>)`*** helps to generate url for the ***<file_name>*** static file.
- ***`render_templates()`*** method is used to render html files. If the application is a module, a ***template*** folder must be created adjacent to the module. If the application is a package, the ***template*** folder must be present inside the package with template files.
- Flask supports jinja2 template as default from latest versions.
- ***`request`*** object is global inside the flask application. While doing unit test, need to pass our own request object using ***`test_request_context()`***
- ***`form`*** data can be accessed using ***`request.form[]`*** attribute. similary ***`request.method`*** tells kind of the request method.
- Files can be passed as part of request to the functions inside flask. ***`request.files['the_file']`*** attribute refers to the file uploaded by the user. ***`enctype="multipart/form-data"`*** must be specified in the HTML form to transfer the files.
- Files can be saved on the server using ***`save()`*** method of the file object.
- ***`request.cookies`*** can be used to access cookies. ***`set_cookie('<key>', '<value>')`*** is used to set cookies present as method of response object. ***`make_response()`*** function creates response for the string/html template.
- ***`errorhandler`*** decorator is used to decorate error pages.
```python
from flask import render_template

@app.errorhandler(404)
def page_not_found(error):
    return render_template('page_not_found.html'), 404
```
- Flask implicitly converts the result of the views functions into a response object. Whereas ***`make_response()`*** function can be used to customise the response of the views.