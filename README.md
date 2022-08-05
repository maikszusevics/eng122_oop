# Python OOP

![image](https://user-images.githubusercontent.com/110176257/182826772-6d741bb1-4970-4838-aabc-0e5c6f6bec2a.png)


## Step 1: Creating animal class
### Created a animal.py file for this:
```
# create an animal class
# syntax class Name:
# good practise to name class with capital letter

class Animal:
    # need to initialise a class every time
    # __init__ to declare class attributes
    def __init__(self): #refers to current class
        self.alive = True
        self.spine = True

    def sleep(self):
        return "all animals sleep"

    def eat(self):
        return "eating is vital"

# create an object of the class before using it
cat = Animal()

# print(cat.eat()) # abstracted how eat was created or what info is available
```


## Creating a reptile class
### Created a reptile.py file for this:

```
# inherit everything from Animal class into reptile
from animal import Animal

# create reptile class
class Reptile(Animal): # write the name of the class in () to inherit
    # parent class / base class / superclass
    def __del__(self):
        # let it know to inherit everything from parent class
        super().__init__() # super() is used to inherit everything from parent class
        self.cold_blooded = True
        self.heart_chamber = [3, 4]

    def seek_heat(self):
        return "looking for direct sunlight"

    def hunt(self):
        return "they do be hunting for food"

# create object of reptile class

reptile_object = Reptile()

print(reptile_object.eat())
print(reptile_object.hunt())



```
