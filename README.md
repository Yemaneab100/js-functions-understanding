# Understanding Functions
This exercise is designed to improve your understanding of functions, function arguments and return statements.

## Learning Objectives
* Explain how functions, function arguments and `return` statements work

## Instructions
Go through each of the questions below, one by one, using the following process:

1. *Write down* a description of what you believe the function(s) are doing and what you think the answer to the question is. Do not skip the writing down step.

2. Run the code by typing (don't copy and paste, *type* the code for this exercise) it in to a js file and running the file with `node`. Name the file based on the question name (i.e `q1.js`, `q2.js`, etc.). Add `console.log` statements to observe values where required.
3. Did you answer correctly? If not, try to understand why not. What did you misunderstand about the code? **This step is crucial to this exercise. If the answer is not what you expected, do not move on until you understand why**. You can experiment with the code adding `console.log` messages to help you see what is happening. You can ask another member of the Cohort, you can look at previous exercises, online references, and of course you can ask the instructors using the support channel.
4. If necessary update your written answer (keep the original!) with your updated understanding.
5. Commit and push your updates
6. Move on to the next question.

Look at the `example-question.md` file for an example of what your writeup should look like (you don't need to include the actual code in your own write up, it's just provided in the example for clarity).

At the end of all questions, in a new MD file describe in your own words:

* What a function is
* How function arguments work
* How return statements work

Share this final write up with your instructor.

## Learning Cycle
This process is an example of applying a *learning cycle*. Remember this diagram from the beginning of the course?

![Learning Cycle](learning-cycle.png)

Be conscious of this process as you go through the exercise. If the code for a particular question does something you didn't expect, ask yourself why. Modify the code as necessary to help understand it's behavior, copy the code to a new file, add console.log messages to give you visibility. This process is the key to developing your own understanding of how specific concepts work. Keep this diagram in mind as you go through the exercise.

## Instructor Demo
Your instructor will demonstrate this process for the first question.

## Questions

### Q1
What is the value of `result` after calling this function? Why?
```javascript
function myFunction(num1, num2) {
  return num1+num2
}

const result = myFunction(5,5)
```
The code calls the myFunction function and passes two arguments, 5 and 5. The function adds these two numbers together and returns the result (10 in this case). The return value of the function is stored in the variable result - so when this code runs, the value of the result variable will be 10.

### Q2
What is the value of `result` after calling this function? Why?

```javascript
function myFunction(num1, num2) {
  num1+num2
}
// line 56 should have return for this code to run correctly and return result as 10.
const result = myFunction(5,5)
```

This function is nearly idemtical to the one in Q1, passes same arguments. However, due to no "return" command in it the return will be underfined.
### Q3
What is the value of `num` at the end of the program? Why?

```javascript
function myFunction(num) {
  return num-1
}

let num = 10
num = myFunction(num)
num = myFunction(num)
``` 
The code calls the myFunction function and passes one argument num 10. The function is decrising num by one each time it is called. End value of the return command will be 8, due to function called twice, and every time num has been decrised by 1.

### Q4
What is the value of `add` and `num` at the end of the program? Why?

 The code calls myFunction function and originaly passes two arguments num and add, however while calling the function num has been substituted with add. End value of add will be 1, due to function has been called twice (3-1-1=1). Value of num will not be changed to to not beeing used.

```javascript
function myFunction(num) {
  return num-1
}

let num = 10
let add = 3
add = myFunction(add)
add = myFunction(add)
```
### Q5
What value will be logged inside the function call? Why?

The code calls myFunction function and passes two arguments num and num1. Due to this function does not have return command it should print whatever specifed inside in console.log(). However when this function has been called, only one argument has been used insted of two specified in the function. As a result function will return underfined.

```javascript
function myFunction(num, num1) {
  console.log(num1)
}

let num = 10
let num1 = 2

myFunction(num)
The code calls myFunction function and originaly passes two arguments 
```

### Q6
What value will be logged inside the function call? Why?

```javascript
function myFunction(num, num1) {
  console.log(num1)
}

let num = 10
let num1 = 2

myFunction(num1, num)
```
The code calls myFunction function and passes two arguments num and num1. Due to this function does not have return command it should print whatever specifed inside in console.log(). However while calling this function num and num1 have been swaped. as the result this function will return 10 insted of 2.

### Q7
What will the value of counter be at the end of this program? Why?

```javascript
let counter = 1

function myFunction() {
  counter++
  return counter
}

myFunction()
const num = myFunction()
```
The code calls myFunction function and has one variable counter with value 1. Every time this function called our value increases by one. Due to this function called twice, counter will show result as 3 at the end.
 
### Q8
What will the value of `result` be at the end of this program? Why?

```javascript
function myFunction(num1, num2) {
  return num1 + num2
}

const num1 = 10
const num2 = 1
const num3 = 4

const result = myFunction(num3, num1)
```
The code calls myFunction function and passes two arguments. Howevew when we are calling this function we are substituting num1 to num3 and num2 to num1 . Result will show 14 (4 + 10)

### Q9
What will be logged out on the console when this code rus? Why?

```javascript
function myFunction(num1, num2) {
  console.log(num3)
}

const num1 = 10
const num2 = 1
const num3 = 20

myFunction(num3, num1)
```
The code calls myFunction function and passes two arguments. Howevew when we are calling this function we are substituting num1 to num3. Result value will be 20.

### Q10
What will be logged out on the console when this code runs? Why?

```javascript
function myFunction(num1, num2, num3) {
  console.log(num3)
}

const num1 = 10
const num2 = 1
const num3 = 20

myFunction(num3, num1, 100)
```
The code calls myFunction function and passes three arguments. Howevew when we are calling this function we are substituting num3 with 100. Rusult value will be 100.

### Q11
What will be the value of `result` when this code runs? Why?

```javascript
function myFunction(num1, num2, num3) {
  return num1 + num2 + num3
}

const num1 = 10
const num2 = 1
const num3 = 20

const result = myFunction(1, 1, 1)
```
The code calls myFunction function and passes three arguments. Howevew when we are calling this function we are substituting each argument with number 1. Result value will be 3. (1+1+1)
### Q12
What will be the value of `result` when this code runs? Why?

```javascript
function getSomeValue() {
  return 2
}

function myFunction(num1) {
  const num2 = getSomeValue()
  return num1 * num2
}

const result = myFunction(5)
```
This is a nested function. First one to run is function called getSomeValue.  num2 is equel to result of this function. It is 2 as specified in the return command.
myFunction function  substituting num1 with number 5. In this case this function will return result 10 (5*2)
### Q13
What will be the value of `result` when this code runs? Why?

```javascript

function getSomeValue() {
  return 2
}

function myFunction(num1) {
  const num2 = getSomeValue()
  return num1 * getSomeValue()
}

const result = myFunction(5)
```
This is a nested function. First one to run is function called getSomeValue.  
myFunction function  substituting num1 with number 5 and multiplies by the value of getSomeValue function, which in this case 2. So, the result will be 5 * 2, which is 10.
### Q14
What will be the value of `result` when this code runs? Why?

```javascript
function getSomeValue() {
  return 2
}

function myFunction(num1) {
  return getSomeValue() * getSomeValue()
}

const result = myFunction(5)
```
First the getSomeValue function will excute and it returns the value of 2. When myFunction function is excutes, it will return the value of getSomeValue multiplies by getSomeValue, which is 4.

### Q15
What will be the value of `result` when this code runs? Why?

```javascript
function myFunction(num1) {
  if(true) {
    return -10
  }

  return num1 * 10
}

const result = myFunction(5)
```
When we pass the value of 5 to myFunction function, it will be true. So, it will stop excuting in the if block as there is a return keyword, which the value is -10.

### Q16
What will be the value of `result` when this code runs? Why?

```javascript
function myFunction(num1) {
  if(false) {
    return -100
  }

  return num1 * 10
}

const result = myFunction(5)
```
When we pass the value of 5 to myFunction function, the if block is false, So, it will not stop excuting in the if block it will continue the next line, which will result 5*10 which is 50.
### Q17
What will be the value of `result` when this code runs? Why?

```javascript
function myFunction(num1) {
  return -100

  return num1 * 10
}

const result = myFunction(5)
```
As there is a return keyword in the myfunction, and its value is -100. The result will return -100, it will stop going further once it excutes a return keyword.

### Q18
What will be the value of `result` when this code runs? Why?

```javascript
function myFunction(num1) {

  return num1 * 10

  return -100
}

const result = myFunction(5)
```
when myFunction is called, it will pass 5 to the fuction. As there is a return keyword in the myfunction, and its value is num1(5) multiplies by 10. The result will return 50, and it will stop excuting after the return keyword.
### Q19
What will be the value of `result` when this code runs? Why?

```javascript
function myFunction(num1, num2, num3) {
  return num2
}

const result = myFunction(5, 10, 15)
```
Three arguements are passed to myFunction function, and only the value of num2 will be returned which is 10.

### Q20
What will be the value of `result` when this code runs? Why?

```javascript
function myFunction(num1, num2, num3) {
  return num1 + num3
}

const num1 = 20
const num2 = 200
const num3 = 1000

const result = myFunction(5, 10, num3, 15)
```
This function has three arguments and it will return the value of num1(5) plus num3 (1000), which is 1005. While calling this function num1 will be substituted with 5 and num3 will remain the same value as defined, which is 1000, and number 15 will be ignored by this function. 

### Q21
What will be the value of `result` when this code runs? Why?

```javascript
function myFunction(num1, num2) {
  const result = num1+num2
  return result
}

let result = myFunction(10, 20)
 result = myFunction(100, 2)
```
The result of the function will be 30. Because this function supposed to return the value of the result, and in the result, arguments 10 and 20 are passed. 

### Q22
What will be the value of `result` when this code runs? Why?

```javascript
function myFunction(num1, num2) {
  let result = num1+num2
  return result
}

let result = 0
myFunction(100, 2)

```
The result will be 0, because the value of the result is not replaced by the value of the function, whic is num1 + num2. 
### Q23
What will be the value of `result` when this code runs? Why?

```javascript
function myFunction(num1, num2) {
  result = num1+num2
}

let result = 0
myFunction(100, 2)
```

In this case the functios is updating the value of the result. Previous the value of the result was 0, when it updates by the function it will be num1(100) plus num2(2), which is 102.

### Q24
What will be the value of `result` when this code runs? Why?

```javascript
function myFunction(num1, num2) {
  const result = num1+num2
  return 100
}

const result = myFunction(5, 2)
```
The function will pass 5 and 2, but it will return 100, as the function tells 100 no matter the value of the result is. 

### Q25
What will be the printed out by the console log statements when this code runs? Why?
```javascript
function myFunction(a) {
  let b = 20
  
  console.log("a:", a)
  console.log("b:", b)
  console.log("c:", c)
}

let a = 1
let b = 2
let c = 3

myFunction(100)
```
First the function will try to find the values of a, b, and c from insde, if it finds the values it will excute, and if it does not find from the inside block of the function it will try to find either from the bracket or from outside of the function. Thus, in this case value of a is found from the bracket, and value of b found inside the block of the functions and value of c found from outside of the function. So, the results of a, b and c will be 100, 20 and 3 respectively. 