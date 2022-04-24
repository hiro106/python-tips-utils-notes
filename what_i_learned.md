## Notes of what I (hiro106) learned regarding Python
### ...Things I didn't know, had forgotten, or had known but don't have a good command of.

- `math` is a module. A module is just a collection of variables (a namespace, if you like) defined by someone else. We can see all the names in math using the built-in function dir().
  - We can also call help() on the module itself. This will give us the combined documentation for all the functions and values in the module (as well as a high-level description of the module). 

- ABCMeta Class
  - Motivation to check up: When I executed a command `type(DecisionTreeRegressor)`, the returned output was `abc.ABCMeta`.
  - Official doc: https://docs.python.org/3/library/abc.html#module-abc
  - Implementation: https://github.com/python/cpython/blob/f4c03484da59049eb62a9bf7777b963e2267d187/Lib/abc.py
  - From the docstring in the class definition `class ABCMeta(type):`: 
> Metaclass for defining Abstract Base Classes (ABCs).
        Use this metaclass to create an ABC.  An ABC can be subclassed
        directly, and then acts as a mix-in class.  You can also register
        unrelated concrete classes (even built-in classes) and unrelated
        ABCs as 'virtual subclasses' -- these and their descendants will
        be considered subclasses of the registering ABC by the built-in
        issubclass() function, but the registering ABC won't show up in
        their MRO (Method Resolution Order) nor will method
        implementations defined by the registering ABC be callable (not
        even via super()). 

- Dictionary Comprehension
  - https://www.datacamp.com/community/tutorials/python-dictionary-comprehension
  - Template: `dict_variable = {key:value for (key,value) in dictonary.items()} `
  - Example1: `double_dict1 = {k: v*2 for (k, v) in dict1.items()}`
  - Example2: `dict1_keys = {k*2:v for (k,v) in dict1.items()}`
  - Example3: `new_dict_comp = {n: n**2 for n in numbers if n%2 == 0}`
  - 
       
