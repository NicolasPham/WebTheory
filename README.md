# WebTheory

### Typescript

<details>

```javascript
- What is typescript:
    > A programming language to address shortcomings of Javascript
    > Benefits: static typing, code completion, refactoring, shorthand notations
    > Drawbacks: compilation (tranlate ts to js - transpilaiton),  discipline in coding

- Setting up the Development Environment
    > npm i -g typescript
    > tsc -v (check version of ts compiler)

- Config the TS compiler:
    > tsc (compiler all ts to js)
    > tsc --init
    > tsconfig.json:
        > "target": "es2016" (change it by Ctr + space)
        > "module": "commonjs"
        "rootDir": "./src" (also create a src folder)
        "outDir": "./dist" (store javascript files)
        "removeComment": true, (remove all the comments in js)
        "noEmmitOnError":true (compiler wont generate js if there is an error)
        "sourceMap": true

- Debugging:
    > in file launch.json add:
        > "preLaunchTask": "tsc build - tsconfig.json"

```
</details>

###  Python
<dtails>

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
    > class MyClass:
        x = 5
    > p1 = MyClass();
    > print(p1.x) #5


```
</details>