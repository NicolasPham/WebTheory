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

```python




```