# Send Response
### Send Text Response
```python
from flask import make_response

@app.route('/')
def func():
	# 200 is response status code
	return make_response('Text Message' , 200)
```
### Send JSON Response
```python
from flask import jsonify, make_response

@app.route('/')
def func():
	# my_dict is dictionary
    return make_response(jsonify(my_dict), 200)
```
### Send HTML Response
```python
from flask import render_template , make_response

@app.route('/')
def func():
	# html files stored in templates folder
	return make_response(render_template('hello.html'))
```
### Send File Response
```python
from flask import send_file

@app.route("/")
def func():
	   file =
		send_file("file_path",as_attachment=True)
	  return file
```
### Send Image Response
```python
from flask import send_file

@app.route("/")
def func():
	  result =
		send_file("file_path",mimetype='image/gif')
	  return result
```
