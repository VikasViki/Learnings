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

<br>

**Reference:** https://flask.palletsprojects.com/en/2.0.x/tutorial/
 
 