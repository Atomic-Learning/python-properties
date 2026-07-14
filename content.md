In Python, a property is a special kind of attribute that, when accessed, will execute some code and return a value. This returned value is usually derived from other attributes of the object and, as such, describe some aspect of the state of the object.

# Accessing Properties

To access a property, we use the name of a variable which references the object, followed by a dot `.`, followed by the name of the property. 

For example, the `pathlib.Path` class can be used to represent a file path. The `Path` class has a property called `name` which returns the name of the file or directory represented by the `Path` object:

```py-cell
# Don't worry too much about how we import `Path` or create a `Path` object
# Focus on how we access the `name` property and what happens when we do so
from pathlib import Path # Import the Path class from the pathlib module

my_path = Path("/home/user/file.txt") # Create a Path object representing the file path
print(my_path.name)  # Accessing the 'name' property
```

In the example above, the `Path` object stores the entire path to the file, but when we access the `name` property, it returns just the name of the file `file.txt`, which it calculates from the whole path.

Notice that, even though we are causing code to be executed when we access the `name` property, we do not use parentheses `()` after the property name (as we would do if we were calling a function).
