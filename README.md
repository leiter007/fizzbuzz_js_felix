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

## Q3:
The `===`operator also checks the datatype, i.e meaning that the two conditions need to be exactly the same. With `==` the datatype could be a comparison between integer and string and still work for example (also called coercion)

Source: https://stackoverflow.com/questions/523643/difference-between-and-in-javascript

## Q4:
Since the `5 === 0` is a stricter condition than than `3 === 0` , there could be situations when both conditions meet (a conflict). If so, you want the right "hierarchy of conditions" to kick in, meaning in this case if something is divisble by both 5 and 3, it should first "listen" to divisible by 5 and return "Buzz", not "Fizz".

## Q5:
Unit test: Checking a single part of the code to make sure it is functioning on its own. It's tests that can be run by frameworks such as rSPEC.

Feature test: Testing a full feature from the user's perspective - ensuring the user experience is as it should be. When more than just one fraction of the code is tested - with feature tests you (to a greater extent) test the connection between different blocks of code.

## Q6:
Description of the different code blocks below:
````
before(async () => {
        await  browser.init()
        await  browser.visitPage('http://localhost:8080/')
    });
````
1.The async/await function - a method used in asynchronous programming. For the test above, it means that before each test we open a (chromium) browser and test the functionality in the webpage listed above.

````
beforeEach(async () => {
        await  browser.page.reload();
    }
````
...and this block says that before each test is run, we should reload the browsers webpage

````
after(async ()=> {
        await  browser.close();
    })
````
...and this block says that after a whole test scenario is run, the browser should close.

## Author
________
**Felix Bonnier** - [leiter007](https://github.com/leiter007)

 