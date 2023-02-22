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
    > def greetings_function(name):
        print("Welcome" + name)
    > greetings_function("Nick")



```
</details>