# WebTheory

### Havard University Course

<details>

```javascript
- BASIC HTML/CSS
    - Viewport: the visual part of the screen that the users can actually see
        > <meta name="viewport" content="width=device-widht, initial-scale=1.0">
    - Media Queries:
        > @media (max-width: 1024px) {}
    - Grid display:
        > grid-column-gap: 20px;
        > grid-template-columns: 200px 200px auto;
    - Variables in SASS:
        > create a file called "variables.scss"
            > $color: red;
        > compile sass file to css:
            > sass variables.scss:variables.css (manually compile)
            > sass --watch variables.scss:variables.css (automatically compile)
        > Inheritance:
            > %message { //make this as inheritance
                font-family, background-color, color, etc
            }
            > .success {
                @extend %message;
                padding:...
            }
            
- Git: 
    > git clone <url>: take the repository from the internet and download to your own computer
        - HTTPs: is the url we need
    > git add <filename>: add file to keep track of
        - We can only keep track of specific files we want
        > git commit -am "message": commit all files that have changed
    > git commit -m "message": save the state of the folder
    > git status: what currently happening inside the repository
    > git push: push commited files to server
    > git pull: pull any changed files from server to local computer
    > git log: keep tracks of all commits that have been made
    > 
    
    







        

```
</details>

###  Python

#### Basic syntax
<details>

```python
- List Methods:
    > list1 = [1,2,3,4,5]
    > list2 = ["banana", "mango", "apple", "grape"]

    > list1.extend(list2) -> [1,2,3,4,5,"banana", "mango", "apple", "grape"]

    > list2.append("cherry") -> ["banana", "mango", "apple", "grape", "cherry"]
    > list2.insert(1, "cherry") -> ["banana", "cherry", "mango", "apple", "grape"]
    > list2.remove("banana") -> ["mango", "apple", "grape"]
    > list2.pop() -> ["banana", "mango", "apple"]
    > list2.pop(1) -> ["banana", "apple", "grape"]
    > del list2[1] -> ["banana", "apple", "grape"]
    > del list2 -> delete the list variable
    > list2.clear() -> empty the list
    
    > print(list2.index("mango")) -> 1
    > print(list2.count("mango")) -> 1 ~ return how many times value appear in the list

    > list1.sort() -> sort the list in ascending order
    > list2.reverse() -> sort the list in the reversing order
    
- Tuple Methods: tuple is an immutable list
- Function:
    > def greetings_function(*names):
        print("Welcome" + names[1])
    > greetings_function("Nick", "Ana", "Ryan")

    > name = input("Please enter your name:")
    > def greetings_function(name):
        print("Welcome" + names[1])
    > greetings_function(name)

- IF statment:
    if condition:
    elif condition2:
    else:

- While loops:
    > i = 1
    > while i < 6 or i == 6:
        print (i)
        i += 1

- for loop:
    > for letter in "Hello":
        print(letter)
        if letter == l:
            break

    > for x in range(4):
        print(x)

    > for x in range(3,7):
        print(x)
    > else:
        print("Finish looping")

- try / except:
    > try :
        x = int(input("Input an integer: "))
        print(x)
    > except ValueError: # wrong input
        print("Value not an integer" + name)
    > except NameError: # undefined variable
        print("Something went wrong ... please try again")

    > try :
        x = int(input("Input an integer: "))
        print(x)
    > except:
        print("Something went wrong")
    > else: #only run if everything went through
        print("Nothing went wrong")
    > finally: # always run
        print("Try except finished")

- Reading/Writing Files:
    > file = open(<filename>, "r")
    # r: reading, w: writing, editing, a: append, r+: reading + writing
    
    > print(file.readable()) # true / false
    > for line in countries_file.readlines():
        print(line)

    > file.close()

    # Writing files
    > countries_file = open("newFile.txt", "w")
    > countries_file.write("This is a new line")
    

- Classes and Objects:
    - Class: a construct of different objects (we have various objects in the class)
    > class Person:
        def __init__(self, name, age):
            self.name = name
            self.age = age
    > p1 = Person("Nick", 33)
    > print(p1.name) #Nick

- Modules:
    > import app
    > app.say_hi() #Hi, welcome to the world

- Introduction to PIP: is used for installing external modules from the web
    - what is pip: pip is package management system used to install and manage software packages
    - pypi: the python package index

```
</details>

#### Django
<details>

```python
> pip install django
> pip install virtualenvwrapper-win 
    #install virtual environment on win
> mkvirtualenv myapp
    # create a virtual environment called myapp





```
</details>
