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
    > git reset: go back to older version commit
        > git reset --hard <commit> : go back to version with commit hash
        > git reset --hard origin/master: get back to current version on github
    > git branch: tell me what branch I'm currently on, and all branches that I have
        > git checkout -b <branch name> : create a new branch with <branch name>
        > git checkout master: switch to master branch
    > git merge <branch name> : merge one branch to the current branch
    > fork: make your own copy of a repository, then we can clone, pull and work on it
    
    - Github page: a github website provide to user
        - Create a repository as username.github.io
        - URL in Setting
        
```
</details>

###  Python
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
    
- Set: a collection where value only appears once. If add another one already exist, will show only one
    > s = set()
    > s.add(1)
    > s.add(2)
    > s.remove(2)
    
- Dict:
    > names = {"first": "Nicolas", "last": "Pham"}
    > print(names["first"]
    
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

- Exceptions:
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
    > class Flight():
        def __init__(self, capacity):
            self.capacity = capacity
            self.passengers = []
        def add_passenger(self, name):
            if not self.open_seats():
                return False
            self.passengers.append(name)
            return True
        def open_seats(self):
            return self.capacity - len(self.passengers)
    > flight = Flight(3)
    > people = ["Nick", "Ana", "Ryan", "Nobody"]
    > for person in people:
        success = flight.app_passenger(person)
        if success:
            print(f"Added {person} to flight successfully")
        else:
            print(f"No available seat for {person}")

- Modules:
    > import app
    > app.say_hi() #Hi, welcome to the world
    
    > from <filename> import <variable name>
        > from function import square
    - or
    > import function
        > print(function.square)

- Introduction to PIP: is used for installing external modules from the web
    - what is pip: pip is package management system used to install and manage software packages
    - pypi: the python package index
    
- Additional info:
    format String: 
        > print (f"Hello, {name}")
    convert variable into another type:
        > n = int(input("Enter number: "))
    exit the program:
        import sys
        sys.exit(1)
        
- Decorator:
    def annouce(f):
        def wrapper():
            print("About to run the function...")
            f()
            print("Done with the function")
        return wrapper

    @annouce
    def hello():
        print("Hello world")
    
    hello()
    
- Lambda:
    people = [
        {"name": "Nick", "house": "Pham"},
        {"name": "Ana", "house": "Nguyen"},
        {"name": "Ryan", "house": "PN"},
    ]
    
    def f(person):
        return person["name"]
    people.sort(key=f)
    print(people)
    
    --- equals to ---
    people.sort(key=lambda person: person["name"])
    
    
    

    
    
```
</details>

#### Django
<details>

```python
> pip install virtualenvwrapper-win 
    #install virtual environment on win
> mkvirtualenv myapp
    # create a virtual environment called myapp

- Havard University:
> pip3 install django
> django-admin startproject <PROJECT NAME>
> python manage.py runserver #run the server
> python manage.py startapp <APP NAME> #create an app called <APP NAME>
    > python manage.py startapp hello

- setting.py configuration:
    #show what apps are installed in the projects
    > INSTALLED_APP = [
        'hello',
        'django.contrib.admin',
        'django.contrib.auth',
    ]
- views.py of the application:
    > from django.http import HttpResponse
    > import datetime
    > def index(request):
        return HttpResponse("Hello World")
    > def greet(request, name):
        return HttpResponse(f"Hello, {name.capitalize()}!")
    #Real router:
    > def index(req):
        return render(req, "hello/index.html")
    > def greet(req, name):
        return render(req, "hello/greet.html", {
            "name": name.capitalize()
        })
    > def newyear(req):
        now = datetime.datetime.now()
        return render(req, "hello/newyear.html", {
            "newyear": now.month == 1 and now.day == 1
        })
    
- create urls.py in hello directory:
    > from django.urls import path
    > from . import views
    > urlpatterns = [
          path("", views.index, name="index"),
          path("<str:name>", views.greet, name="greet")
      ]
- in urls.py of main directory:
    > from django.urls import include, path
    > urlpatterns = [
        path("admin/", ...),
        path("hello/", include("hello.urls"))
      ]
    
#Real router: create a templates folder inside hello, then create hello folder inside templates
    - create index.html inside ./hello/templates/hello
        <h1>Hello, {{name}}</h1>
        
        {% if newyear %}
            <h1>YES</h1>
        {% else %}
            <h1>NO</h1>
        {% endif %} #since we dont have intentation, we must have endif
        
    - create a "static" folder in hello dir, and create files "./hello/static/newyear/styles.css"
    - in file newyear.html include: \
        > {%  load static %}
        > <link href="{%  static newyear/styles.css %}" rel="stylesheet">
        




```
</details>
