# Number Methods in JS
There are many JavaScript Number methods that are often used to manipulate number values. These number formats support integers, floating-point numbers, such as decimal, hexadecimal, notations.

Here are a few methods that can make manipulating and modifying numeric values much easier.

## _JavaScript Number Format_

1. Number()

    The Number() method converts a string into a number.
    ```JavaScript
    // Example 1
    const x = '10'
    const num = Number(x)
    console.log(num)                 // Output: 10
    console.log(num * 9)             // Output: 90

    // Example 2
    const x = true
    const num = Number(x)
    console.log(num)                 // Output: 1
    console.log(num + 9)             // Output: 10

    ```
2. parseInt()

    .parseInt() very similar to the number() method, parseInt() formats a string into an integer.
    ```JavaScript
    // Example 1
    const x = '10.99'
    const num = parseInt(x)
    console.log(num)                 // Output: 10
    // Example 2
    const x = '7 days'
    const num = parseInt(x)
    console.log(num)                 // Output: 7
    // Example 3
    const x = 'day 7'
    const num = parseInt(x)
    console.log(num)                 // Output: NaN
    ```
    The parseInt(value) method takes a string x , a decimal number, and returns an integer. It returns the first integer 7, of the value ‘7 days’. If we change the value of xto ‘day 7’, it will return NaN because the method cannot find the number value.

3. __parseFloat()__

    The .parseFloat() method parses a string value and returns the number with its decimal value.

    ```JavaScript
    // Example 1
    const x = '10.99'
    const num = parseFloat(x)
    console.log(num)                 // Output: 10.99
    // Example 2
    const x = '2.49 3.99'
    const num = parseFloat(x)
    console.log(num)                 // Output: 2.49
    // Example 3
    const x = 'day 7'
    const num = parseFloat(x)
    console.log(num)                // Output: NaN
    ```
    Similar to parseInt() , parseFloat() checks to find the first character in the string is a number, if yes, it parses the string and returns it as a number with the decimal value. The main reason that sets parseInt() and parseFloat() methods apart is that parseFloat() after parsing the string, returns the number with its decimal values, whereas parseInt() only returns the integer.

4. toExponential()

    The toExponential() method returns a string that represents the exponential notation of the given number. This method accepts fractionDigits as an optional parameter that specifies the number of digits after the decimal point.

    ```JavaScript
    // Example 1
    const x = 456.789
    const num = x.toExponential()
    console.log(num)                 // Output: 4.56789e+2
    // Example 2
    const x = 456.789
    const num = x.toExponential(2)
    console.log(num)                 // Output: 4.57e+2
    ```
    The parameter with 2 digits, returns the value with two decimal digits.

5. toString()

    The .toString() method converts a numeric value into a string.

    ```JavaScript
    // Example 1
    const x = 10
    const num = x.toString()
    console.log(num)                // Output: '10'
    // Example 2
    const x = 10
    const num = x.toString(2)
    console.log(num)                // Output: 1010 
    ```
    Adding the number 2 as a parameter to .toString() method, returns the binary value of the number.

6. toFixed()

    toFixed() method rounds up a number to the nearest highest or lowest fixed-point notation. It takes in a parameter which signifies the number of digits should be displayed after the decimal point.

    ```JavaScript
    // Example 1
    const num = 4.56789;
    console.log(num.toFixed())             // Output : 5
    // Example 2
    const num = 4.56789;
        
    console.log(num.toFixed(2))            // Output : 4.5
    ```
    In the example above, the .toFixed(digits) method formats the number with 2 number of digits after the decimal point. If you call the .toFixed() method without a parameter, it returns a rounded-up integer.

7. toPrecision()    

    .toPrecision() returns the numeric value with a specific length. It takes an argument that signifies the length. If given without a specific length, the method returns the number as it is.

    ```JavaScript
    // Example 1
    const num = 456.789;
        
    console.log(num.toPrecision())      // Output : 456.789
    // Example 2
    const num = 456.789;
        
    console.log(num.toPrecision(2))     // Output : 4.6e+2
    ```

8. valueOf()

    The valueOf() method is used to return the primitive value of the Number object you’re calling it on. Primitive types in JavaScript are number, string, bigint, symbol, undefined, null, and boolean.

    ```JavaScript
    const x = 45
    const num = x.valueOf()
    console.log(num)                 // Output: 45
    console.log(typeof num);         // Output: Number
    ```

9. toLocaleString()

    The toLocaleString() method uses a local language format to convert a number and returns it as a string. It takes two arguments, locales and options , which defines the language of which conversion you want to use, and the behavior of the function.

    obj.toLocaleString([locales[, options]])

    ```JavaScript
    const num = 226537.883;
    //US English
    console.log(num.toLocaleString('en-US'));     //Output: 226,537.883
    // Indian
    console.log(num.toLocaleString('en-IN'));     //Output: 2,26,537.883
    // Standard French (especially in France)
    console.log(num.toLocaleString('fr-FR'));     //Output: 226 537,883
    ```

10. isInteger()

    .isInteger() checks whether the given value is an integer and returns a boolean value.

    ```JavaScript
    //Example 1
    const x = 10
    const num = Number.isInteger(x)
    console.log(num)                     // Output: true
    //Example 2
    const x = 10.99
    const num = Number.isInteger(x)
    console.log(num)                     // Output: false
    //Example 3
    const x = "10"
    const num = Number.isInteger(x)
    console.log(num)                     // Output: false
    ```
    In the examples above, setting x to 10 returns a boolean value true; when we change the value to 10.99 it returns false because the value has decimal digits, which means it’s not an integer. Similarly, when we wrap the value with quotations, the method returns false because the value is a string.

11. isFinite()

    .isFinite() checks whether the given value is finite and returns a boolean value.

    ```JavaScript
    //Example 1
    const x = 10
    const num = Number.isFinite(x)
    console.log(num)                     // Output: true
    //Example 2
    const x = -10.99
    const num = Number.isFinite(x)
    console.log(num)                     // Output: true
    //Example 3
    const x = "10"
    const num = Number.isFinite(x)
    console.log(num)                     // Output: false
    ```
    The inFinite() method returns true when set x to 10 , -10.99 because these are finite numbers. Returns false when we change the value to a string.

12. isNaN()

    The isNaN() method checks whether a value is a NaN and its type is Number. This method returns true if the given value is NaN and its type is Number, otherwise, it returns false.

    ```JavaScript
    const num1 = NaN;
    console.log(Number.isNaN(num1)); //true
    const num2 = "NaN";
    console.log(Number.isNaN(num2)); //false
    const num3 = Infinity;
    console.log(Number.isNaN(num3)); //false
    const num4 = "string"/5;
    console.log(Number.isNaN(num4)); //true
    const num5 = 32e34;
    console.log(Number.isNaN(num5)); //false
    const num6 = '0';
    console.log(Number.isNaN(num6)); //false
    const num7 = undefined;
    console.log(Number.isNaN(num7)); //false
    const num8 = {};
    console.log(Number.isNaN(num8)); //false
    ```

# Truthy vs Falsy values in JS

JavaScript uses type coercion (implicit conversion of values from one data type to another) in Boolean contexts, such as conditionals. This means that values are considered either truthy (evaluate to true) or falsy (evaluate to false) depending on how they are evaluated in a Boolean context.

__The following values are always falsy:__

- false
- 0 (zero)
- -0 (minus zero)
- 0n (BigInt zero)
- '', "", `` (empty string)
- null
- undefined
- NaN

__Everything else is truty. That includes:__

- '0' (a string containing a single zero)
- 'false' (a string containing the text "false")
- [] (an empty array)
- {} (an empty object)
- function(){} (an "empty"      function)

```JavaScript
Boolean(false);         // false
Boolean(undefined);     // false
Boolean(null);          // false
Boolean('');            // false
Boolean(NaN);           // false
Boolean(0);             // false
Boolean(-0);            // false
Boolean(0n);            // false

Boolean(true);          // true
Boolean('hi');          // true
Boolean(1);             // true
Boolean([]);            // true
Boolean([0]);           // true
Boolean([1]);           // true
Boolean({});            // true
Boolean({ a: 1 });      // true
```

# String in JS

The JavaScript string is an object that represents a sequence of characters.

There are 2 ways to create string in JavaScript

- By string literal
- By string object (using new keyword)

__By string literal__

The string literal is created using double quotes. The syntax of creating string using string literal is given below:
```JavaScript
var stringname="string value";  
```
__By string object (using new keyword)__

The syntax of creating string object using new keyword is given below:

```JavaScript
var stringname=new String("string literal");  
```

We can use single or double quotes to write a string

```JavaScript
const str1 = "Sanjib";  // Double quotes
const str2 = 'Roshan';  // Single quotes
```
We can use quotes inside a string, as long as they don't match the quotes surrounding the string:

```JavaScript
const answer1 = "It's alright"; // It's alright
const answer2 = "He is called 'Johnny'"; //He is called 'Johnny'
const answer3 = 'He is called "Johnny"'; //He is called "Johnny"
```
Because strings must be written within quotes, JavaScript will misunderstand this string:

```JavaScript
const text = "We are the so-called "Vikings" from the north.";
```

The string will be chopped to "We are the so-called ".

The solution to avoid this problem, is to use the backslash escape character.

The backslash (\) escape character turns special characters into string characters:

```JavaScript
const text = "We are the so-called \"Vikings\" from the north.";
```
|Code |Result  |Description |
|-----|--------|------------|
|\\'  |'       |Single quote|
|\\"  |"       |Double quote|
|\\\  |\       |Backslash   |

Six other escape sequences are valid in JavaScript:

|Code |Result              |
|-----|--------------------|
|\\b  |Backspace           |
|\\f  |Form Feed           |
|\\n  |New Line            |
|\\r  |Carriage Return     |
|\\t  |Horizontal Tabulator|
|\\v  |Vertical Tabulator  |


# String method in JS

There are many JavaScript string methods that are often used to manipulate string values. Following are the list method which is used in the JS

1. charAt(index) Method

    The JavaScript String charAt() method returns the character at the given index.

    ```JavaScript
    const str="javascript";  
    document.write(str.charAt(2));
    // v 
    ```

2. concat(str) Method

    The JavaScript String concat(str) method concatenates or joins two strings.

    ```JavaScript
    const s1="javascript ";  
    const s2="concat example";  
    const s3=s1.concat(s2);  
    document.write(s3);
    // javascript concat example
    <!-- OR -->
    s3 = "javascript" + " " + "concat example";
    ```

3. indexOf(str) Method

    It provides the position of a char value present in the given string.

    ```JavaScript
    const s1="javascript from javatpoint indexof";  
    const n=s1.indexOf("from");  
    document.write(n); 
    ```

4. lastIndexOf(str) Method

    It provides the position of a char value present in the given string by searching a character from the last position.

    ```JavaScript
    const s1="javascript from javatpoint indexof";  
    const n=s1.lastIndexOf("java");  
    document.write(n); 
    // 16
    ```
5. toLowerCase() Method

    It converts the given string into lowercase constter.

    ```JavaScript
    const s1="JavaScript toLowerCase Example";  
    const s2=s1.toLowerCase();  
    document.write(s2); 
    // javascript tolowercase example
    ```

6. toUpperCase() Method

    The JavaScript String toUpperCase() method returns the given string in uppercase constters.

    ```JavaScript
    const s1="JavaScript toUpperCase Example";  
    const s2=s1.toUpperCase();  
    document.write(s2); 
    // JAVASCRIPT TOUPPERCASE EXAMPLE
    ```
7. slice(beginIndex, endIndex) Method

    The JavaScript String slice(beginIndex, endIndex) method returns the parts of string from given beginIndex to endIndex. In slice() method, beginIndex is inclusive and endIndex is exclusive. It allows us to assign positive as well negative index.

    ```JavaScript
    const s2=s1.slice(2,5);  
    const s1="abcdefgh";  
    document.write(s2); 
    // cde
    ```
8. trim() Method

    The JavaScript String trim() method removes leading and trailing whitespaces from the string.

    ```JavaScript
    const s1="     javascript trim    ";  
    const s2=s1.trim();  
    document.write(s2);
    // javascript trim
    ```
9. substring() Method

    substring() is similar to slice().

    The difference is that start and end values less than 0 are treated as 0 in substring().

    ```JavaScript
    const str = "Apple, Banana, Kiwi";
    const part = str.substring(7, 13);
    // Banana
    ```
10. substr() Method

    substr() is similar to slice().

    The difference is that the second parameter specifies the length of the extracted part.  

    ```JavaScript
    const str = "Apple, Banana, Kiwi";
    const part = str.substring(7, 6);
    // Banana
    ```
    If you omit the second parameter, substr() will slice out the rest of the string.

    ```JavaScript
    const str = "Apple, Banana, Kiwi";
    const part = str.substr(7);
    // Banana, Kiwi
    ```
11. replace() Method

    The replace() method replaces a specified value with another value in a string:

    ```JavaScript
    const text = "Please visit Microsoft!";
    const newText = text.replace("Microsoft", "gitHub");
    // Please visit gitHub!
    ```

    The replace() method does not change the string it is called on.

    The replace() method returns a new string.

    The replace() method replaces only the first match

ECMAScript 2017 added two String methods: padStart() and padEnd() to support padding at the beginning and at the end of a string.

12. padStart() Method
    The padStart() method pads a string with another string at start:
    ```JavaScript
    const text = "5";
    const padded = text.padStart(4,"x"); //xxx5
    //OR
    const padded = text.padStart(4,"0"); //0005
    ```
    Note
    The padStart() method is a string method.

    To pad a number, convert the number to a string first.

    See the example below.
    ```JavaScript
    const numb = 5;
    const text = numb.toString();
    const padded = text.padStart(4,"0"); //0005
    ```

13. padEnd() Method
    Like the above same it pads a string with another string with end.
    
    ```JavaScript
    const text = "5";
    const padded = text.padEnd(4,"x"); //5xxx
    //OR
    const padded = text.padEnd(4,"0"); //5000
    ```
    Note
    The padEnd() method is a string method.

    To pad a number, convert the number to a string first.

    See the example below.
    ```JavaScript
    const numb = 5;
    const text = numb.toString();
    const padded = text.padEnd(4,"0"); //5000
    ```

14. split() Method

    The split() method divides a string into a list of substrings and returns them as an array.
    ```JavaScript
    const message = "JavaScript::is::fun";

    // divides the message string at :: 
    let result = message.split("::");
    console.log(result);

    // Output: [ 'JavaScript', 'is', 'fun' ]
    ```

__JavaScript Strings are immutable__

In JavaScript, strings are immutable. That means the characters of a string cannot be changed. For example,

```JavaScript
    let a = 'hello';
    a[0] = 'H';
    console.log(a); // "hello"
```
However, you can assign the variable name to a new string. For example,
```JavaScript
    let a = 'hello';
    a = 'Hello';
    console.log(a); // "Hello"
```
__JavaScript is Case-Sensitive__

JavaScript is case-sensitive. That means in JavaScript, the lowercase and uppercase letters are treated as different values. For example,

```JavaScript
    const a = 'a';
    const b = 'A'
    console.log(a === b); // false
```
# Template Literals

Introduced in ES6 is a new way in which we can create a string, and that is the Template Literal. With it comes new features that allow us more control over dynamic strings in our programs. Gone will be the days of long string concatenation!

To create a template literal, instead of ' or " quotes we use the ` character. This will produce a new string, and we can use it in any way we want.

```JavaScript
let newString = `A string`;
console.log(newString);
// A string
```
**Multi-line**

The great thing about Template Literals is that we can now create multi-line strings! In the past, if we wanted a string to be on multiple lines, we had to use the \n or new line character.

```JavaScript
let myMultiString = 'Some text that I want\nOn two lines!';

console.log(myMultiString);
/*
Some text that I want
On two lines!
*/
```
With a Template Literal string, we can just go ahead and add the new line into the string as we write it.

```JavaScript
let myMultiString= `This will be
on two lines!`;

console.log(myMultiString);
/*
This will be
on two lines!
*/
```
This will produce a string with a new line in it. The ability to do this with expressions makes Template Literals a really nice templating language for building of bits of HTML that we will cover later.

**Expressions**

In the new Template Literal syntax we have what are called expressions, and they look like this: ${expression}. Consider the code below.

```JavaScript
let name = `Sanjib`;

console.log(`Hi my name is ${name}`);
// Hi my name is Sanjib
```
The ${} syntax allows us to put an expression in it and it will produce the value, which in our case above is just a variable that holds a string! There is something to note here: if you wanted to add in values, like above, you do not need to use a Template Literal for the name variable. It could just be a regular string.
This will produce the same output. These expressions do more than just let us put in variables that contain strings in them. We can evaluate any sort of expressions that we would like.

```JavaScript
let person = {
    firstName: `Sanjib`,
    lastName: `Sah`,
    sayName() {
        return `Hi my name is ${this.firstName} ${this.lastName}`;
    }
};

console.log(person.sayName());
// Hi my name is Sanjib Sah
```

__HTML Templates__

With the ability to have multi-line strings and use Template Expressions to add content into our string, this makes it really nice to use for HMTL templates in our code.

```JavaScript
const header = "Subjects";
const tags = ["Science", "Maths", "English","Nepali","Social","Health"];

const html = `<h2>${header}</h2><ul>`;
for (const x of tags) {
  html += `<li>${x}</li>`;
}

html += `</ul>`;
```