# Note of Python Basic

The following content is based on the Edx course [Using Python for Research]( https://courses.edx.org/courses/course-v1:HarvardX+PH526x+3T2016/course/)  whose instrutor is Professor [Jukka-Pekka “JP” Onnela ](https://www.hsph.harvard.edu/onnela-lab/people/). Hope this note could help you learn fundamental knowledge of Python better.

## Week 1
#### 1.1.1 Python Basic<br>
* :star:Name: from the inimitive BBC shows called Monty Python's Flying Circus
* Python is an interpreted language
* :star:Two different mode in Editor
   * Interactive mode 
      * experimenting code one line or one expression at a time
   * standard mode
      * running your programs from start to finish
* Editor
   * Anaconda ( many people would recommend this software as their first editor but here I would like to say anaconda has some conflict with npm, if you would use npm in the future, be careful!)
      * Jupyter
      * Spyder
   * Pycharm (Someone consider this editor as a professional software since it will show the possible functions automatically, which might save lots of time while programming)
   * Jupyter (Actually, jupyter can operate independently on your computer without installing Anaconda and it is much convenient for programmers to use since you can type Javascript/R/Java by setting different kernels.)

#### 1.1.2 Objects
* Obejcts and the relationship between objects
   * can change——mutable
   * can not change——immutable
   * object：type-what kind of obejects/value/identity-identity number in computer memory
* :star: `attribute`
   * data attribute
   * method attached to a object

```Python
import numpy as np
x=np.array([1,3,5])
y=np.array([1,5,9])     
x.mean()
y.mean()              # Method
x.shape               # Data attribute
y.shape
# the difference between method and data attribute on Python format is ()
# Methods are functions associated with objects, whereas data attributes are data associated with objects.
```
#### 1.1.3 Modules and Methods
- Modules
```Python
import math
math.pi
math.sprt(10)
math.sin(math.pi/2)
# Since math package contains bunch of functions or attributes, here use command "from math import pi" to only import pi
```

```Python
import math 
import numpy as np
math.sqrt(2)
np.sqrt(2)
# exist in different namespace
np.sqrt([2,3,4])    #np can process sequence of numbers but math can not
```

- :star: import
   - new namespace
   - run
   - np(reference)
   - np.sqrt(within the numpy namespace)

```Python
name="Amy" #create a namespace "name" and the object "Amy" is stored somewhere in the memory
type(name)
dir(name)   # dir function return the methods you can use on this attribute
dir(str)    # the same exact methods
help(name.upper) #ask python for help
name.upper()  # return the result
name.upper  # return the method
# make sure you did not run the function
```
#### 1.1.4 Numbers and basic calculations
- three different numeric types
   - integers
   - floating point numbers 
   - complex numbers
```Python
123+34
123*34
123**34
123*345
# unlimitation for integers
=========================================================
6/7
15/7
15//7  # (floor integers less than the floating answer)
=========================================================
15/2.3
_   #return the latest number
_**2.3
10*2
_+5
_**2
```

* factorial operation (n!)

```Python
import math
math.factorial
```

#### 1.1.5 Random Choice
```
import random
random.choice([2,44,55,66])
#random.choice only requires that the object has several values regardless of mutability
```
#### 1.1.6 Expressions and Booleans
* Expressions——Boolean（True False）
* or/and/not
```
True or false
```
* eight different camprison
```
[2,3] == [2,3]
True
[2,3] is [2,3]
False
#same contents but different objects

2==2.0 # Python will take the int 2 into floating number and then the statement becomes 2.0==2.0
True
```
**Attention**: The difference between is and ==
"==" tests whether objects have the same value, whereas "is" tests whether objects have the same identity.

**Update by Feb.7th, 2019**
