# FizzBuzz challenge
## Description
This repo contains the second challenge of the [Craft Academy Bootcamp](https://craftacademy.se/english/curriculum/), by April 2019 Cohort.

## Objective 
________
In this chasllenge, the "traditional" programming kata of FizzBuzz is expected to be implemented using JavaScript. Expectations of the final delivery by end of weekend:

* A deployed website with some styling
* All test are going green
* Good and readable commits messages, commits made after every test going green or when you have added implementation code
* Usage of branches
* A PR towards your own master branch
* Answers to all of the questions in the README
* Markdown syntax used in the README with proper code formatting

 ## Learning objectives from Craft Academy
 ________
* Ability to explain concepts
* Practice JS
* Combine both feature and unit test and understand their difference
* Read and understand documentation
* Debug and find errors
* Find and remove unneccesary code and files.

## Exercise questions from the course material
________
### Q1:
````
let  fizzBuzz = fs.readFileSync('./src/js/fizz-buzz.js');
eval( fizzBuzz + `\nexports.FizzBuzz = FizzBuzz;`)
````
Explanation:\
The variable fizzbuzz (defined by the let syntax) is calling on the pre-defined constant variable called fs. This is a module that (when required) provides an API for interacting with the FILE SYSTEM, which provides access to already built in methods.

The readFileSynch function then defines which file we will use the built in methods on - in our case the fizz-buzz.js file we will use for implementation code.

The eval() function evaluates or executes a string argument. If the argument has one or more JavaScript statements, it executes the statement.

Sources: 
* https://nodejs.org/api/fs.html#fs_file_system
* https://www.w3schools.com/jsref/jsref_eval.asp

## Q2:
Why is the fizzBuzz variable defined outside of the it block? This since the definition will be used in more it blocks (tests) within the describe block going forward. This means we do not need to define it aagin inside coming it blocks - unless we want to change it for that specicif test.

## Author
________
* **Felix Bonnier** - [leiter007](https://github.com/leiter007)

 