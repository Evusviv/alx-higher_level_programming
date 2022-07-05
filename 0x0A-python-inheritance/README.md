Tasks 0. Lookup mandatory Write a function that returns the list of available attributes and methods of an object:

Prototype: def lookup(obj): Returns a list object You are not allowed to import any module guillaume@ubuntu:~/0x0A$ cat 0-main.py #!/usr/bin/python3 lookup = import('0-lookup').lookup

class MyClass1(object): pass

class MyClass2(object): my_attr1 = 3 def my_meth(self): pass

print(lookup(MyClass1)) print(lookup(MyClass2)) print(lookup(int))

guillaume@ubuntu:/0x0A$ ./0-main.py ['class', 'delattr', 'dict', 'dir', 'doc', 'eq', 'format', 'ge', 'getattribute', 'gt', 'hash', 'init', 'le', 'lt', 'module', 'ne', 'new', 'reduce', 'reduce_ex', 'repr', 'setattr', 'sizeof', 'str', 'subclasshook', 'weakref'] ['class', 'delattr', 'dict', 'dir', 'doc', 'eq', 'format', 'ge', 'getattribute', 'gt', 'hash', 'init', 'le', 'lt', 'module', 'ne', 'new', 'reduce', 'reduce_ex', 'repr', 'setattr', 'sizeof', 'str', 'subclasshook', 'weakref', 'my_attr1', 'my_meth'] ['abs', 'add', 'and', 'bool', 'ceil', 'class', 'delattr', 'dir', 'divmod', 'doc', 'eq', 'float', 'floor', 'floordiv', 'format', 'ge', 'getattribute', 'getnewargs', 'gt', 'hash', 'index', 'init', 'int', 'invert', 'le', 'lshift', 'lt', 'mod', 'mul', 'ne', 'neg', 'new', 'or', 'pos', 'pow', 'radd', 'rand', 'rdivmod', 'reduce', 'reduce_ex', 'repr', 'rfloordiv', 'rlshift', 'rmod', 'rmul', 'ror', 'round', 'rpow', 'rrshift', 'rshift', 'rsub', 'rtruediv', 'rxor', 'setattr', 'sizeof', 'str', 'sub', 'subclasshook', 'truediv', 'trunc', 'xor', 'bit_length', 'conjugate', 'denominator', 'from_bytes', 'imag', 'numerator', 'real', 'to_bytes'] guillaume@ubuntu:/0x0A$ No test cases needed

Repo:

GitHub repository: alx-higher_level_programming Directory: 0x0A-python-inheritance File: 0-lookup.py

My list mandatory Write a class MyList that inherits from list:
Public instance method: def print_sorted(self): that prints the list, but sorted (ascending sort) You can assume that all the elements of the list will be of type int You are not allowed to import any module guillaume@ubuntu:~/0x0A$ cat 1-main.py #!/usr/bin/python3 MyList = import('1-my_list').MyList

my_list = MyList() my_list.append(1) my_list.append(4) my_list.append(2) my_list.append(3) my_list.append(5) print(my_list) my_list.print_sorted() print(my_list)

guillaume@ubuntu:/0x0A$ ./1-main.py [1, 4, 2, 3, 5] [1, 2, 3, 4, 5] [1, 4, 2, 3, 5] guillaume@ubuntu:/0x0A$ Repo:

GitHub repository: alx-higher_level_programming Directory: 0x0A-python-inheritance File: 1-my_list.py, tests/1-my_list.txt

Exact same object mandatory Write a function that returns True if the object is exactly an instance of the specified class ; otherwise False.
Prototype: def is_same_class(obj, a_class): You are not allowed to import any module guillaume@ubuntu:~/0x0A$ cat 2-main.py #!/usr/bin/python3 is_same_class = import('2-is_same_class').is_same_class

a = 1 if is_same_class(a, int): print("{} is an instance of the class {}".format(a, int.name)) if is_same_class(a, float): print("{} is an instance of the class {}".format(a, float.name)) if is_same_class(a, object): print("{} is an instance of the class {}".format(a, object.name))

guillaume@ubuntu:/0x0A$ ./2-main.py 1 is an instance of the class int guillaume@ubuntu:/0x0A$ No test cases needed

Repo:

GitHub repository: alx-higher_level_programming Directory: 0x0A-python-inheritance File: 2-is_same_class.py

Same class or inherit from mandatory Write a function that returns True if the object is an instance of, or if the object is an instance of a class that inherited from, the specified class ; otherwise False.
Prototype: def is_kind_of_class(obj, a_class): You are not allowed to import any module guillaume@ubuntu:~/0x0A$ cat 3-main.py #!/usr/bin/python3 is_kind_of_class = import('3-is_kind_of_class').is_kind_of_class

a = 1 if is_kind_of_class(a, int): print("{} comes from {}".format(a, int.name)) if is_kind_of_class(a, float): print("{} comes from {}".format(a, float.name)) if is_kind_of_class(a, object): print("{} comes from {}".format(a, object.name))

guillaume@ubuntu:/0x0A$ ./3-main.py 1 comes from int 1 comes from object guillaume@ubuntu:/0x0A$ No test cases needed

Repo:

GitHub repository: alx-higher_level_programming Directory: 0x0A-python-inheritance File: 3-is_kind_of_class.py

Only sub class of mandatory Write a function that returns True if the object is an instance of a class that inherited (directly or indirectly) from the specified class ; otherwise False.
Prototype: def inherits_from(obj, a_class): You are not allowed to import any module guillaume@ubuntu:~/0x0A$ cat 4-main.py #!/usr/bin/python3 inherits_from = import('4-inherits_from').inherits_from

a = True if inherits_from(a, int): print("{} inherited from class {}".format(a, int.name)) if inherits_from(a, bool): print("{} inherited from class {}".format(a, bool.name)) if inherits_from(a, object): print("{} inherited from class {}".format(a, object.name))

guillaume@ubuntu:/0x0A$ ./4-main.py True inherited from class int True inherited from class object guillaume@ubuntu:/0x0A$ No test cases needed

Repo:

GitHub repository: alx-higher_level_programming Directory: 0x0A-python-inheritance File: 4-inherits_from.py

Geometry module mandatory Write an empty class BaseGeometry.
You are not allowed to import any module guillaume@ubuntu:~/0x0A$ cat 5-main.py #!/usr/bin/python3 BaseGeometry = import('5-base_geometry').BaseGeometry

bg = BaseGeometry()

print(bg) print(dir(bg)) print(dir(BaseGeometry))

guillaume@ubuntu:/0x0A$ ./5-main.py <5-base_geometry.BaseGeometry object at 0x7f2050c69208> ['class', 'delattr', 'dict', 'dir', 'doc', 'eq', 'format', 'ge', 'getattribute', 'gt', 'hash', 'init', 'le', 'lt', 'module', 'ne', 'new', 'reduce', 'reduce_ex', 'repr', 'setattr', 'sizeof', 'str', 'subclasshook', 'weakref'] ['class', 'delattr', 'dict', 'dir', 'doc', 'eq', 'format', 'ge', 'getattribute', 'gt', 'hash', 'init', 'le', 'lt', 'module', 'ne', 'new', 'reduce', 'reduce_ex', 'repr', 'setattr', 'sizeof', 'str', 'subclasshook', 'weakref'] guillaume@ubuntu:/0x0A$ No test cases needed

Repo:

GitHub repository: alx-higher_level_programming Directory: 0x0A-python-inheritance File: 5-base_geometry.py

Improve Geometry mandatory Write a class BaseGeometry (based on 5-base_geometry.py).
Public instance method: def area(self): that raises an Exception with the message area() is not implemented You are not allowed to import any module guillaume@ubuntu:~/0x0A$ cat 6-main.py #!/usr/bin/python3 BaseGeometry = import('6-base_geometry').BaseGeometry

bg = BaseGeometry()

try: print(bg.area()) except Exception as e: print("[{}] {}".format(e.class.name, e))

guillaume@ubuntu:/0x0A$ ./6-main.py [Exception] area() is not implemented guillaume@ubuntu:/0x0A$ No test cases needed

Repo:

GitHub repository: alx-higher_level_programming Directory: 0x0A-python-inheritance File: 6-base_geometry.py

Integer validator mandatory Write a class BaseGeometry (based on 6-base_geometry.py).
Public instance method: def area(self): that raises an Exception with the message area() is not implemented Public instance method: def integer_validator(self, name, value): that validates value: you can assume name is always a string if value is not an integer: raise a TypeError exception, with the message must be an integer if value is less or equal to 0: raise a ValueError exception with the message must be greater than 0 You are not allowed to import any module guillaume@ubuntu:~/0x0A$ cat 7-main.py #!/usr/bin/python3 BaseGeometry = import('7-base_geometry').BaseGeometry

bg = BaseGeometry()

bg.integer_validator("my_int", 12) bg.integer_validator("width", 89)

try: bg.integer_validator("name", "John") except Exception as e: print("[{}] {}".format(e.class.name, e))

try: bg.integer_validator("age", 0) except Exception as e: print("[{}] {}".format(e.class.name, e))

try: bg.integer_validator("distance", -4) except Exception as e: print("[{}] {}".format(e.class.name, e))

guillaume@ubuntu:/0x0A$ ./7-main.py [TypeError] name must be an integer [ValueError] age must be greater than 0 [ValueError] distance must be greater than 0 guillaume@ubuntu:/0x0A$ Repo:

GitHub repository: alx-higher_level_programming Directory: 0x0A-python-inheritance File: 7-base_geometry.py, tests/7-base_geometry.txt

Rectangle mandatory Write a class Rectangle that inherits from BaseGeometry (7-base_geometry.py).
Instantiation with width and height: def init(self, width, height): width and height must be private. No getter or setter width and height must be positive integers, validated by integer_validator guillaume@ubuntu:~/0x0A$ cat 8-main.py #!/usr/bin/python3 Rectangle = import('8-rectangle').Rectangle

r = Rectangle(3, 5)

print(r) print(dir(r))

try: print("Rectangle: {} - {}".format(r.width, r.height)) except Exception as e: print("[{}] {}".format(e.class.name, e))

try: r2 = Rectangle(4, True) except Exception as e: print("[{}] {}".format(e.class.name, e))

guillaume@ubuntu:/0x0A$ ./8-main.py <8-rectangle.Rectangle object at 0x7f6f488f7eb8> ['_Rectangle__height', '_Rectangle__width', 'class', 'delattr', 'dict', 'dir', 'doc', 'eq', 'format', 'ge', 'getattribute', 'gt', 'hash', 'init', 'le', 'lt', 'module', 'ne', 'new', 'reduce', 'reduce_ex', 'repr', 'setattr', 'sizeof', 'str', 'subclasshook', 'weakref', 'area', 'integer_validator'] [AttributeError] 'Rectangle' object has no attribute 'width' [TypeError] height must be an integer guillaume@ubuntu:/0x0A$ No test cases needed

Repo:

GitHub repository: alx-higher_level_programming Directory: 0x0A-python-inheritance File: 8-rectangle.py

Full rectangle mandatory Write a class Rectangle that inherits from BaseGeometry (7-base_geometry.py). (task based on 8-rectangle.py)
Instantiation with width and height: def init(self, width, height):: width and height must be private. No getter or setter width and height must be positive integers validated by integer_validator the area() method must be implemented print() should print, and str() should return, the following rectangle description: [Rectangle] / guillaume@ubuntu:~/0x0A$ cat 9-main.py #!/usr/bin/python3 Rectangle = import('9-rectangle').Rectangle

r = Rectangle(3, 5)

print(r) print(r.area())

guillaume@ubuntu:/0x0A$ ./9-main.py [Rectangle] 3/5 15 guillaume@ubuntu:/0x0A$ No test cases needed

Repo:

GitHub repository: alx-higher_level_programming Directory: 0x0A-python-inheritance File: 9-rectangle.py

Square #1 mandatory Write a class Square that inherits from Rectangle (9-rectangle.py):
Instantiation with size: def init(self, size):: size must be private. No getter or setter size must be a positive integer, validated by integer_validator the area() method must be implemented guillaume@ubuntu:~/0x0A$ cat 10-main.py #!/usr/bin/python3 Square = import('10-square').Square

s = Square(13)

print(s) print(s.area())

guillaume@ubuntu:/0x0A$ ./10-main.py [Rectangle] 13/13 169 guillaume@ubuntu:/0x0A$ No test cases needed

Repo:

GitHub repository: alx-higher_level_programming Directory: 0x0A-python-inheritance File: 10-square.py

Square #2 mandatory Write a class Square that inherits from Rectangle (9-rectangle.py). (task based on 10-square.py).
Instantiation with size: def init(self, size):: size must be private. No getter or setter size must be a positive integer, validated by integer_validator the area() method must be implemented print() should print, and str() should return, the square description: [Square] / guillaume@ubuntu:~/0x0A$ cat 11-main.py #!/usr/bin/python3 Square = import('11-square').Square

s = Square(13)

print(s) print(s.area())

guillaume@ubuntu:/0x0A$ ./11-main.py [Square] 13/13 169 guillaume@ubuntu:/0x0A$ No test cases needed

Repo:

GitHub repository: alx-higher_level_programming Directory: 0x0A-python-inheritance File: 11-square.py

My integer #advanced Write a class MyInt that inherits from int:
MyInt is a rebel. MyInt has == and != operators inverted You are not allowed to import any module guillaume@ubuntu:~/0x0A$ cat 100-main.py #!/usr/bin/python3 MyInt = import('100-my_int').MyInt

my_i = MyInt(3) print(my_i) print(my_i == 3) print(my_i != 3)

guillaume@ubuntu:/0x0A$ ./100-main.py 3 False True guillaume@ubuntu:/0x0A$ No test cases needed

Repo:

GitHub repository: alx-higher_level_programming Directory: 0x0A-python-inheritance File: 100-my_int.py

Can I? #advanced Write a function that adds a new attribute to an object if it’s possible:
Raise a TypeError exception, with the message can't add new attribute if the object can’t have new attribute You are not allowed to use try/except You are not allowed to import any module guillaume@ubuntu:~/0x0A$ cat 101-main.py #!/usr/bin/python3 add_attribute = import('101-add_attribute').add_attribute

class MyClass(): pass

mc = MyClass() add_attribute(mc, "name", "John") print(mc.name)

try: a = "My String" add_attribute(a, "name", "Bob") print(a.name) except Exception as e: print("[{}] {}".format(e.class.name, e))

guillaume@ubuntu:/0x0A$ ./101-main.py John [TypeError] can't add new attribute guillaume@ubuntu:/0x0A$ No test cases needed

Repo:

GitHub repository: alx-higher_level_programming Directory: 0x0A-python-inheritance File: 101-add_attribute.py