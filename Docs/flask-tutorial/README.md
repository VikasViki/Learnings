- ***`__name__`*** holds the name of the current python module.
- In order to start the app, the below commands needs to be executed outside of the app, by setting ***FLASK_ENV*** to ***development***, live debugging and auto update of site is achieved.
```shell
export FLASK_APP=flaskr
export FLASK_ENV=development
flask run
```

## Database

- Concurrent write operations makes the sqlite database slower.
- ***`flask.current_app`*** points to the Flask application handling the request.
- Tables need to be created before storing and retriving data i.e schema has to be defined beforehand.
- ***`flask.current_app.open_resource(<file_name>)`*** locates the ***<file_name>*** within the flask app. This helps in moving files like schema.sql within package with having to modify the code.
- After intializing the db a new file gets created inside ***instance*** directory paraller to ***flask app i.e flaskr*** directory r.

## Blueprints and Views

- ***Blueprint*** is a way to organize group of related views and code.
- ***`db.execute()`*** takes SQL query with ? placehodlers and tuple of values to replace the placeholders.
- ***session*** is a dict that stores data across requests. Flask securely signs the data so that it can't be tampered.
- ***`<blueprint>.before_app_request()`*** registers function that runs before the view functions for subsequent requests.

## Templates

- ***`{{ expression }}`*** expression will be the final output to the document. ***`{% if/for %}`*** is used for defining control flows.
- ***g and url_for()*** is automatically available inside templates.
- ***get_flashed_messages()*** stores all the messages used inside ***flash()*** function.
- The templates for a blueprint will be placed in a directory with the same name as the blueprint. i.e ***flask_app/templates/<blueprint_name>/template_file.html***

## Static Files

- Flask automatically adds a static view that takes path to ***flask_app/static*** directory. It can be called using ***`url_for('static', file_name='<static_file>')`***

## Blog Blueprint

- ***loop.last*** is a special variable inside jinja that returns a boolean based on whether current loop iteration is last or not.
- ***`app.add_url_rule()`*** associates the endpoint with specified view in parameters. i.e 2 different endpoints can point to same view function.

## Test Coverage

- ***`tests`*** directory has to be created along side the ***flask app*** to contain all test files.
- ***conftest.py*** will hold all fixtures that each test function can use.
- Each test will create a new temporary database file and populate some data that will be used in the tests.
- Pytest uses fixtures by matching their function names with the names of the arguments in the test functions.
- Pytest has its own ***monkeypatch*** fixture that is used to override the behaviour of the function with different function using the ***`monkeypatch.setattr('<actual_function_name>', <dummy_function_name>)`*** method.
- Using ***client*** in a ***with*** block allows accessing context variables such as ***sessions*** after the response is returned, which would normally will throw an error.

<br>

**Reference:** https://flask.palletsprojects.com/en/2.0.x/tutorial/
 
 