# Request Object
### Take Request Header as Dictionary
```python
from flask import request

@app.route("/")
def func():
	  request_header = dict(request.headers)
	  # code
```
### Take Request Body as Dictionary
```python
from flask import request

@app.route("/")
def func():
	request_body = dict(request.form)
	# code
```
### Take Request Parameters as Dictionary
```python
from flask import request

@app.route("/")
def func():
	  request_params = dict(request.args)
	  # code
```

### Take Request Type from Request 
```python
from flask import request

@app.route('/' , methods=['POST' , 'GET'])
def func():
	if(request.method=='POST'):
		# code
	elif(request.method=='GET'):
		# code
```
### Take File from Request
```python
from flask import request
from werkzeug import secure_filename

app.config['UPLOAD_FOLDER'] = UPLOAD_FOLDER
app.config['MAX_CONTENT_LENGTH'] 
	= 16 * 1024 * 1024 # bytes

@app.route('/' , methods = ['POST']):
def func():
	f = request.files['file']
	f.save(secure_filename(f.filename))
	return 'file uploaded successfully'
```

