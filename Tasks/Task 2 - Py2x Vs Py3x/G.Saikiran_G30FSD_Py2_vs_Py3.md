1. Print Function

 Python 2
print "Hello World"

Python 3
print("Hello World")

In Python 3, print is a proper function (more consistent)

2. Division Behavior
   
Python 2
5 / 2   # 2 (integer division)

Python 3
5 / 2   # 2.5 (true division)
5 // 2  # 2 (floor division)

Python 3 always uses true division unless you use //  

3. Unicode Handling
   
Python 2
text = "hello"    # ASCII by default

Python 3
text = "hello"    # Unicode by default

Python 3 handles Unicode naturally — no extra “u” prefix needed.

4. Range vs xrange
   
Python 2
range(5)   # returns list
xrange(5)  # returns iterator

Python 3
range(5)   # optimized iterator (xrange removed)

Python 3 merges both into one efficient version of range().

5. Input Function
   
Python 2
raw_input()   # returns string  
input()       # evaluates input (unsafe)

Python 3
input()       # always returns string

Python 3 keeps only the safe version.

6. Exception Syntax
   
Python 2
except ValueError, e:

Python 3
except ValueError as e:


Cleaner and more structured.

7. Dictionary Changes
   
Python 2
dict.keys()    # list
dict.items()   # list

Python 3
dict.keys()    # view
dict.items()   # view

 Views are faster and memory-efficient.
