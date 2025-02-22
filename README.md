# foundationJS

My notes and references for JavaScript lessons.

Step one -   Absorb: Read lesson and supplemental materials thoroughly.
Step two -   Process & Practice: Deconstruct lessons into smaller concepts and actively code examples.
Step three - Reinforce: Test comprehension with end-of-lesson knowledge questions.

Variables and Operators

This section of the curriculum contains an overview for the topics covered in this lesson

* Running JavaScript code using an HTML file
* Declaring variables using the let and const
* Performing number operations
* Performing string operations
* Using logical and mathematical operations

Variables

let: which can be reassigned 
const: which we can't reassign and throws an error if we try

There is a third way, which was the original way to declare a variable in JavaScript.

var: var works similar to let, in that variables assigned this way can be reassigned, however 
     it has other quirks that were cleared up when the language introduced the let and const keywords.
     var is found in older code bases and it is likely to come across code which uses var at some point.

Variable Naming 

let:

Names must contain only letters, digits, or the symbols $ and _ (underscore)
You can not start a name in JavaScript using a digit.

When name contain multiple words camelCase is commonly used and is considered best practice.

camelCase examples: myName, myNumber, myString

Case matters: apple and Apple are two different variable names

Reserved words: let, class, return, and function are reserved, because they are words used by the JavaScript 
                language itself. for a list of reserved keywords check the link
                https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#keywords

const:

To declare a constant (unchanging) variable, use const instead of let.

Variables declared using const are called "constants". They cannot be reassigned and any attempt to do so will cause and error.
When programmer is sure that a variable will not change, they use the const to guaranty and communicate that fact to everyone.

const examples: birthdate, social security numbers, company name, ect...

Uppercase Constants

There is wide spread practice to use constants as aliases for difficult to remember values that are known before execution.
Such constants are named using capital letters and underscores.

Examples: COLOR_ORANGE is much easier to remember than #FF7F00 
It is also easier to mistype the #hexadecimal number than using the upper case constants, it is also much more meaningful than the 
#hexadecimal number it self.

Naming Things Right 

A variable name should have a clean, obvious meaning, describing the data that it stores.

Variable naming is one of the most important and complex skills in programming. A glance at variable names can reveal which code was written by a beginner 
versus an experienced developer.

Some good-to-follow rules are:

* Use human-readable names like userName or shoppingCart.
* Stay away from abbreviations or short names like a, b, and c, unless you know what you’re doing.
* Make names maximally descriptive and concise. Examples of bad names are data and value. Such names say nothing. It’s only okay to use them if the context 
  of the code makes it exceptionally obvious which data or value the variable is referencing.

* Agree on terms within your team and in your mind. If a site visitor is called a “user” then we should name related variables currentUser or newUser instead of
  currentVisitor or newManInTown.

Numbers

Numbers are the building blocks of programming logic.

JavaScript Arithmetic Operators:

* (+)  Addition (or Concatenation)
* (-)  Subtraction
* (*)  Multiplication
* (**) Exponentiation
* (/)  Division
* (%)  Modulus 
* (++) Increment
* (--) Decrement 

Operators and Operand 

Operator (100) Operand (+) Operator (50).

Data Types and Conditions

* Name the eight data types in JavaScript.
* Understand the difference between single, double, and backtick quotes.
* Embed a variable/expression in a string.
* Understand what a method is.
* Name the three logical operators.
* Understand what the comparison operators are.
* Understand what conditionals are.
* Understand what nesting is.
* Understand what truthy and falsy values are.

There are eight (8) basic data types in javaScript

* Seven primitive data types:
     
     * numbers: for numbers of any kind, integer or floating point, integers are limited by ±(253-1).
     * bigint: for integer numbers of arbitrary length.
     * string: for strings. A string may have zero or more characters, there's no separate single-character type.
     * boolean: for true/false.
     * null: for unknown values - a standalone type that has a single value null.
     * undefined: for unassigned values a standalone type that has a single value 'undefined'.
     * symbol: for unique identifiers.

* One non-primitive data type:
     
     * object for more complex data structures.

* The typeof operator allows us to see which type is stored in a variable.
     
     * Usually used for typeof x, but typeof(x) is also possible.
     * Returns a string with the name of the type, like string.
     * For null returns 'object' this is an error in the language, its not actually an object.

Strings: Depending on what kind of work you’re doing, you might end up working more with pieces 
         of text rather than numbers. A string is a piece of text… and is a fundamental building block 
         of the language.

MDN tutorial on strings in JavaScript

* Creating strings literals.
* Escaping characters in strings.
* Template literals, including using variables and multiline template literals.

HTML provides structure and meaning to text, CSS allows us to precisely style it, and JavaScript offers many features for manipulating strings. 

Declaring Strings

Just like we did with numbers, we are declaring a variable, initializing it with a string value, and then returning the value. The only difference 
here is that when writing a string, you need to surround the value with quotes. Any text without quotes around it is interpreted as a variable name, 
property name, reserved word, or similar. Single quotes, double quotes, and backticks In JavaScript, you can choose single quotes ('), double quotes ("), 
or backticks (`) to wrap your strings in. You must use the same character for the start and end of a string, or you will get an error.

Strings declared using single quotes and strings declared using double quotes are the same, and which you use is down to personal preference — although 
it is good practice to choose one style and use it consistently in your code.

Strings declared using backticks are a special kind of string called a template literal. In most ways, template literals are like normal strings, 
but they have some special properties:

  * you can embed javaScript in them.
  * you can declare template literals over multiple lines.

Embedding JavaScript

Inside a template literal, you can wrap JavaScript variables or expressions inside ${ }, and the result will be included in the string:

     const firstName = 'Chris';
     const greeting = `Hello ${firstName}`;
     console.log(greeting);

You can use the same technique to join together two variables:

     const variableOne = 'Hello, ';
     const variableTwo = 'how are you?';
     const joined = `${variableOne} ${variableTwo}`;
     console.log(joined);

Joining strings together like this is called concatenation.

Including Expressions in Strings

     const song ='You got to Fight';
     const score = 9;
     const highestScore = 10;
     const favoriteSongRating = `I like the song ${song}. I gave it a score of ${(score / highestScore) * 100}%.`;
     console.log(favoriteSongRating);

Multiline Strings

Template literals respect the line breaks in the source code, so you can write strings that span multiple lines.

     const smallParagraph = `The brown fox jumped over the hound dog, 
     the spoon ran away with the bowl, 
     and humpty-dumpty fell off the wall!`;
     console.log(smallParagraph);

To have the equivalent output using a normal string you'd have to include line break characters '(\n)' in the string.

Including Quotes in Strings

Since we use quotes to indicate the start and end of strings, how can we include actual quotes in strings?

One common option is to use single quotes to enclose the whole string and double quotes to enclose the quoted characters:

  * const message = ' We used single quotes "this is a message that is a quote" to enclose the string'; 

Another option is to escape the problem quotation mark. Escaping characters means that we do something to them to make 
sure they are recognized as text, not part of the code. In JavaScript, we do this by putting a backslash just before the character.

  * const escapeQuote = 'I\'ve written the other option to escape the problem quotation mark';

Knowledge Check Quiz:

The following questions are an opportunity to reflect on key topics in this lesson. If you can’t answer a question, click on it to review the material, 
but keep in mind you are not expected to memorize or master this knowledge.


* What three keywords can you use to declare new variables?
  
  * let, const, and var. Although var is found in code bases prior to introducing let and const, it is suggested to avoid using var to declare variables 
    to avoid quirks in your source code. Note: As a part of maintain JavaScript the authorities go to great lengths to insure any and all future 
    updates to the language don't drastically change to avoid breaking existing source code. Book that explains in more depth:'You don't know JS yet.' 
    second addition.

* Which of the three variable declarations should you avoid and why?

  * You should avoid using the keyword var when declaring variables. This key word has some quirks that revolve around the global and block scope visibility, 
    which at times can cause unpredicted results in your code.

* What rule should you follow when naming variables?

  * Using human-readable names that speak to what types of data the variables will hold. Making sure to use descriptive and concise names.
    * Examples: userName, shoppingList, accountBalance, favoriteSongRating. These types of names, while scanning source code can provide a straight forward
      and meaningful understanding for what the variable and it's intended purpose is for.

* What happens when you add (+) numbers and strings together?

  * When trying to add numbers and strings together you should expect concatenation to be the outcome. Although the arithmetic operator (+) is used for addition 
    when introducing characters that are incased in quotes or also referred to as a string, the plus sign changes it's meaning from addition to concatenation. Combing
    the number to the string.
      * Example: let myNumber = 10; let bobsNumber = "10"; console.log(myNumber + bobsNumber); // output is 1010

* How does the Modulus (%) or remainder, operator work?

  * The Modulus operator works by displaying the remainder of a mathematical equation, not the entire answer.
    * Example: 2 / 5 will result in a display of the number 1 and not 0.4 as the answer.

* What is the difference between == and ===?
  
  * == is know as a comparison operator. It compares two types of data to see if they are equal to. It's a loose comparison.
    * Example: 10 "10" 

  * === is also know as a comparison operator. It compares two types of data to insure they are alike and of the same typeof data. It is a strict comparison
    meaning that it checks both the value and typeof.
      * Example: 'stringOne' === 'stringTwo'

* When would you receive an NaN result?

  * NaN - Not a number would indicate that a number is not a legal number. 

* What is operator precedence and is it handled in JS?

  * Operator precedence is the order in which JS uses for mathematics. As it was taught in school Exponentiation, Multiplication, Division, Addition, Subtraction
    is handled in that order. A way for you to change this is by adding parentheses, and if there are no parentheses the next line of order would be read from left
    to right.
      * Example: 1 / 2 * 3 + 5 - 1 division will be performed first because the JS compiler will read the math problem left to right.

* How do you increment and decrement numbers?

  * ++ is to increment the variable by one and -- is to decrement the variable by one.
    * Example: 1++ increment, 1-- is decrement 

* What's the difference between prefixing and postfixing increment/decrement operators?

  * The operators ++ and -- can be placed either before or after a variable.
    When the operator goes after the variable, it is in “postfix form”: counter++.
    The “prefix form” is when the operator goes before the variable: ++counter.
    Both of these statements do the same thing: increase counter by 1.

    Is there any difference? Yes, but we can only see it if we use the returned value of ++/--.

    Let’s clarify. As we know, all operators return a value. Increment/decrement is no exception. The prefix form returns the new value while the postfix form returns the old value (prior to increment/decrement).

    To see the difference, here’s an example:
       This is prefixing:
     * let counter = 1;
       let a = ++counter; // (*)

       alert(a); // 2
       In the line (*), the prefix form ++counter increments counter and returns the new value, 2. So, the alert shows 2.
       
       This is postfixing
     * let counter = 1;
       let a = counter++; // (*) changed ++counter to counter++

       alert(a); // 1
       In the line (*), the postfix form counter++ also increments counter but returns the old value (prior to increment). So, the alert shows 1.

* How do you access developer tools in the console?

  * You will need to first create and index.html file and create your boilerplate using the !doctype html, html tag, inside the head you will add all the meta tags
    that will be needed, fill in the title so it will display in the browser tab, create the body tag and inside the closing body tag just above it create your script 
    tag using the src attribute to link your external script.js file. Once you've completed that right click the index.html file and preview using live preview in the code editor to display your blank index.html file in the browser. Right click the blank page and scroll down to inspect page this will open the development tools.
    On the right bottom corner there will be a set of developer tabs choose the console tab to open the console so you can start writing JavaScript inside the browser.
    Another option is to use the shortcut key and press F12 on your keyboard to also access the developer tools.

* How do you log information to the console?

  * using the console.log(). Console is the object and the log() is the method of the console object.

* What does unary plus operator do to string representation of integers ('10')?

  * When the operand is not a number, the unary plus operator converts it into a number. 
     * console.log(+x); // Expected output: 1
       console.log(+y); // Expected output: -1
       console.log(+""); // Expected output: 0

