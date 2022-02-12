# Routing
### Basic Routing
```python
@app.route('/link_get' , methods=['GET'])
def func_GET():
	# code
@app.route('/link_post' , methods=['POST'])
def func_POST():
	# code
@app.route('/link_put' , methods=['PUT'])
def func_PUT():
	# code
@app.route('/link_delete' , methods=['DELETE'])
def func_DELETE():
	# code
```
### Multiple Methods with Same Link
```python
@app.route('/link' , 
		   methods=['GET','POST','PUT','DELETE'])
def func():
	# code
```

### Different Link with Same Function
```python
@app.route('/link_GET' , methods=['GET'])
@app.route('/link_POST' , methods=['POST'])
@app.route('/link_PUT' , methods=['PUT'])
@app.route('/link_DELETE' , methods=['DELETE'])
def func():
	# code
```

### Take parameter from URL
```python
@app.route('/<paramname>' , methods=['GET'])
def func_GET(paramname):
	# code
@app.route('/link/<paramname>' , methods=['POST'])
def func_POST(paramname):
	# code
@app.route('/<param1>/<param2>' , methods=['PUT'])
def func_PUT(param1 , param2):
	# code
```

