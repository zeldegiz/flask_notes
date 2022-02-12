# Redirect
### Redirect URL
```python
from flask import redirect
@app.route('/route')
def func():
	return redirect("https://www.google.com")
```

### Redirect Function
```python
from flask import redirect , url_for
@app.route("/index")
def func():
  return redirect(url_for("admin" , 
						  param1=value1 ,
						  param2=value2))
```

