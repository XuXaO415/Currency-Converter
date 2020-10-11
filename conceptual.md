# Conceptual Exercise

Answer the following questions below:

- What are important differences between Python and JavaScript?  
  | Comparisons                | Python                                                       | JS                                         |
  | -------------------------- | ------------------------------------------------------------ | ------------------------------------------ |
  | REPL(Read-Eval-Print-Loop) | Included with installation                                   | Can be used in Node, not needed in browser |
  | Mutability                 | mutable and immutable data types                             | no concept of mutable and immutable        |
  | Strings                    | ASCII by default                                             | should be encoded as UTF-16                |
  | Numbers                    | different numeric types like int, float, fixed-point decimal | only floating point                        |
  | Inheritance                | class-based inheritance model                                | prototype based inheritance model          |
  | Code blocks                | indentation                                                  | curly brackets                             |

---

- Given a dictionary like ``{"a": 1, "b": 2}``: , list two ways you
  can try to get a missing key (like "c") *without* your programming
  crashing.
  - `dict.get()`
  - `dict.getitem()`

- What is a unit test?
  - Testing of individual units or modules by themselves.

- What is an integration test?
  - Testing of how modules work together

- What is the role of web application framework, like Flask?
  - To take care of the grunt work to make it easier for developers to start and run a server, setting up routes, and creating backend APIs.

- You can pass information to Flask either as a parameter in a route URL
  (like '/foods/pretzel') or using a URL query param (like
  'foods?type=pretzel'). How might you choose which one is a better fit
  for an application?
  - If the app has a search function, use the URL query param.
  - If the app needs a way of categorizing pages and information (for example, Reddit), then use parameters in route URLs

- How do you collect data from a URL placeholder parameter using Flask?
  
```python
@app.route('/example/<name>')
def func(name):
    print(name)
```

- How do you collect data from the query string using Flask?

```python
request.args['data']
```

- How do you collect data from the body of the request using Flask?

```python
request.json['data']
```

- What is a cookie and what kinds of things are they commonly used for?
  - Small piece of data stored on the users computer by the browser
  - Commonly used for:
    - User specific info
    - If user has dismissed something to be shown only once
    - Shopping cart info

- What is the session object in Flask?
  - A way for the user to interact with browser cookies and store them on the backend server
  - Easier then setting up normal cookies, just call the dict

- What does Flask's `jsonify()` do?
  - Creates a JSON response from the server to the request source
