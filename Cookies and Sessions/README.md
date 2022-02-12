# Cookies
### Read Cookies as Dictionary
```python
from flask import request

@app.route("/")
def index():
	  cookie_dict = dict(request.cookies)
	  # code
```
### Set Cookie
```python
from flask import make_response

@app.route("/")
def index():
	resp = make_response()
	resp.set_cookie("key","value")
	return resp
```
### Set Cookie with Time
```python
from flask import make_response

@app.route("/")
def index():
	resp = make_response()
	resp.set_cookie("key","value",60*60*24) # second
	return resp
```
### Delete Cookie
```python
@app.route("/")
def logout():
	resp = make_response()
	resp.set_cookie("username","admin" ,0)
	return resp
```

# Sessions
### Read Session 
```python
from flask import session

app = Flask(__name__)
app.secret_key = "some_secret_key"

@app.route("/")
def admin():
	if("username" in session):
		session["username"]
	# code
```
### Set Session
```python
from flask import session

app = Flask(__name__)
app.secret_key = "some_secret_key"

@app.route("/login")
def login():
	session["username"] = "admin"
	# code
```
### Delete Session
```python
from flask import session

app = Flask(__name__)
app.secret_key = "some_secret_key"

@app.route("/logout")
def logout():
	session.pop("username")
	# code
```
### Set Session Timeout
```python
from datetime import timedelta

app.config['PERMANENT_SESSION_LIFETIME'] =
	timedelta(seconds=60*60)
```
