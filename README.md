# Subject-Matter-Expert-Take-Home-Assignment

# 
**Closures in JavaScript**

In this repo you will find Roger Fleenor’s Subject Matter Expert Take Home Assignment for 2U. Included is a lesson plan on Closures in JavaScript.


### 
**Assumptions**

Students:



*   Have exposure to basics of 
    *   Data types: numbers, strings, objects.
    *   Functions: arrow, anonymous and self-executing (IIFE).
    *   Lexical scope and hoisting.
*   Can engage with the material via live or recorded lectures.
*   Continue to learn online, remotely during the pandemic with access to instructors, TA’s and peers via zoom and slack.

## 
**Overview**


This lesson plan features three Instructor demos with corresponding student activities and instructor reviews. Contents include a closure overview, scope chain and common use cases.


## 
**Class Objectives**

By end of lesson, students should be able to explain the following with an example of each in their own words:



*   Closure in JavaScript
*   Scope Chain and Lexical Environment
*   Common Use Cases

## 



## 
**Class Activities**


## 
**1.1 Everyone Activity: Intro to Closures (10min)**

*   Tell students to follow along by powering up our JavaScript V8’s engines! Aka Chrome browser’s console by  opening the unsolved <span style="text-decoration:underline;">evr-bank-hacker.html</span>
*   Express to students that many object oriented coding languages have private methods and instance variables that allow us to control access to sensitive data. Some examples of those languages include Java, JavaScript, PHP and Python.
*   In Javascript, we have our own way to limit access to sensitive data when necessary. Show students the code from unsolved <span style="text-decoration:underline;">evr-bank-hacker.html</span>:
*   `allTheMoneys` is local to the function `mySavingsAccount`. Your moneys are safe because only `mySavingsAccount `has access to the `allTheMoneys` variable because it is within local scope. However, If we simply return `allTheMoneys`, it's not so safe especially if `bankHacker` calls it. 
*   Instruct students to copy the functions above to their console and take a few minutes to find a way to check if an `accountNumber` is valid to keep the bankHacker from getting `allTheMoneys` without revealing the `accountNumber`
*   Notice that `validAccountNumber` is declared inside of  `mySavingsAccount`, that makes this a closure. `mySavingsAccount` is the 'parent' of `validAccountNumber` meaning `mySavingsAccount` has access to `accountNumber.` Children inherit all methods and variables from their parents!

## 
**1.2 Instructor Demo: Intro to Closures (5min)**

*   Explain that the big idea behind a closure is a function inside of a function! These bundled functions have references to its surrounding state (the lexical environment). 
*   A closure gives you access to an outer function’s scope from an inner function even after the outer function has completed since the inner function will have the state that was created in still in memory. In JavaScript, closures are created every time a function is created at function creation time.
*   Closures are frequently used in JavaScript for object data privacy, in event handlers and callback functions, and in partial applications, currying, and other functional programming patterns.
*   Feel free to offer perspective on how you have used closures throughout your career to help students relate to their future as developers.
*   Next, we will demo the unsolved <span style="text-decoration:underline;">ins-coconut-layers.html</span> file in the browser and open the console. Ask students to predict the output when you run `console.log(coconut())`. 
*   Elaborate on the possibilities and invoke the `insideCoconut` function.
*   Tell students that `insideCoconut()` is a closure, and that they should be able to explain this in their own words at a high-level.
*   Ask students: how can they access `insideCoconut()`? Show students `coconut()()` and_ _Demo alternatives to invocation (Students may not have seen this type of syntax before).
*   After invoking the closure, notice the output in the console and ask the following: What does this tell them about closures and scope? What do they have access to? 
*   Closures have access to variables and parameters that belong to all parent functions.
*   Ask a few students to explain in their own words: A closure is a function inside of a parent function, many ways to invoke a closure, and that closures have access to the parent function’s variables and parameters.

## 
**1.3 Student Activity: Intro to Closures (15min)**


Students will:



*   Debug & invoke the correct translation functions.
*   Have students attempt to create their own closure translating another language of their choice.

## 
**1.4 Instructor Review: Intro to Closures (10min)**

*   Ask a student to volunteer walking through their closure using the custom translator solution and share their findings.
*   Review answers in solved <span style="text-decoration:underline;">stu-translate-with-closures.html</span> focusing on the following:
*   Did anyone notice what happened when the closure is an anonymous function in the `spanishTranslator `?
*   Discuss whether or not the `germanTranslator` inner function is a closure, since it doesn't reference any variables in its lexical environment.
*   Encourage students to explain the takeaways on closures.

## 
**2.1 Instructor Demo: Scope Chain (5min)**

*   Students learn about scope and inheritance in this section, start by opening the solved <span style="text-decoration:underline;">ins-scope-chain.html</span>
*   The function `howManyCoconutLayers` shows us how scope chain works at a basic foundational level. After Invoking the function, ask students to share what they notice about how each of the layer variables are passed down to the inner functions. 
*   Elaborate scope chain as follows: when a variable is used in JavaScript, the JavaScript engine will try to find the variable’s value in the current scope. If it could not find the variable, it will look into the outer scope and will continue to do so until it finds the variable or reaches global scope.
*   Explain that the function `earthLayerDistance` shows us how arguments are also accessible through inner functions via scope chain. 
*   Ask students the following to confirm conceptual understanding:
    *   How many closures do we see?
    *   Which variables do the functions have access to?
    *   How to invoke `layer1 `Demo the different outcomes in the solved version.
    *   Does the closure in `layer1` have access to the variable `innerCore` despite being initialized later?
*   Have a different student explain scope chain in their own words.

## 
**2.2 Student Activity: Scope Chain (15min)**

*   Students will create custom closures and variables in unsolved <span style="text-decoration:underline;">stu-custom-scope-chain.html</span> to exercise the concept of Scope Chain.

## 
**2.3 Instructor Review: Scope Chain (10min)**

*   Note to Instructor: prepare to live code a closure demonstrating scope chain with context coming from experience in your career.
*   Have two students demo (screen share) the closures they have created and explain how scope chain and closures are related.
*   Open the <span style="text-decoration:underline;">ins-custom-scope-chain.html</span> and live code and walkthrough creating a closure.

## 
**3.1 Instructor Demo: Common Use Cases for Closures (5min)**

*   Explain Lexical Environment to students as follows: very simply, a lexical environment is a place where variables and references to the objects are stored.
*   Open solved <span style="text-decoration:underline;">ins-common-use-case.html</span> and walk through the `bankAccount()` function as an example of a lexical environment.
*   Show students that each instance the outer function is called, a separate lexical environment is created. 
*   Even if we call the same function, we are calling a different environment that holds a different value.
*   Ask the class to imagine how this lexical environment can be beneficial in a real world use case.
*   Give students another example with perspective from experience in your career, reinforce this with the idea that data is stored in a lexical environment so that it can only be modified with certain methods.

## 
**3.2 Student Activity: Common Use Cases for Closures (15min)**

*   Students will open the unsolved <span style="text-decoration:underline;">stu-common-use-case.html</span> and recreate the `bankAccount` function with closures to emulate a real world scenario of making deposits and withdrawals using closures.

## 
**3.3 Instructor Review: Common Use Cases for Closures (10min)**

*   Volunteer a student to share their screen and demo the deposit and withdrawal functionality in their `bankAccount`. Guide the student to the solution if there is a small error.
*   Open solved <span style="text-decoration:underline;">ins-common-use-case.html</span> and walkthrough the solution demoing the variety of use case invocations.
*   Elaborate on other practical implications for using closures including any examples you have experienced throughout your career.
*   Share with students that the concepts reviewed today are foundational to their future as a developer working with object-oriented programming.
*   Wrap up today’s lesson with a final definition of the following: 
    *   Closure
    *   Scope Chain
    *   Lexical Environment
    *   Common Use Case