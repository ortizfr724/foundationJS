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


