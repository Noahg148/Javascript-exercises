# Javascript exercises
## 🟨Warm Up
### hello_world
```javascript
/*
# Hello World
Write a program that prints the message `Hello, World!`.

HINT: You can might need to import the `io` module first, here and in all exercises
until topic 5.
You can do this by copying the following line to the top of your program:
import io from "../../utils/io-for-pf.js";
*/

import io from "../../utils/io-for-pf.js";

io.write("Hello, World!");
```
### echo
```javascript
/*
# Echo
Write a program that reads one line of input (string) and
that prints that same line.
*/

import io from "../../utils/io-for-pf.js";

const input = io.read("> ");

io.write(input);
```
### rectangle
```javascript
/*
# Rectangle
Write a program that *draws* a rectangle.
When we say *draw* we mean write some text/symbols that make up a drawing
in the command line.

The rectangle should consist of *stars* (i.e., `*`-symbols).
The rectangle should be 3 rows high and has a width of 4.

## Output
    ****
    ****
    ****
*/

import io from "../../utils/io-for-pf.js";
io.write("****");
io.write("****");
io.write("****");
```
### swap
```javascript
/*
# The Swap Trick
Write a program that reads two inputs into the two variables `a` and `b`.
Make sure that the contents of `a` and `b` are swapped before printing.

We already provided the code for the input and the output.
You should only provide the code for 'the swap' (between the two lines of comments)
You can update this program, but are not allowed to change it!

**Hint:** You can introduce a third variable.
*/
import io from "../../utils/io-for-pf.js";

 
let a = io.read(); // do not (re)move this line
let b = io.read(); // do not (re)move this line
 

// Write your program below:

const c = a;
a = b;
b = c;

// Write your program above.

io.write(a); // do not (re)move this line
io.write(b); // do not (re)move this line
```
### circle_surface
```javascript
/*
# Area of a disk (circle)
Write a program that reads the radius of a circle (``float``),
and computes and prints the area up to 3 digits after the decimal point.
You can ignore negative radius's by treating them as regular radius's.

**Hint:** In JavaScript you can represent π by using `Math.PI`.

**Hint:** In JavaScript you can convert a (floating point) number
to a string using `toFixed`(inverse of parseFloat). **Example:** Turning π into
the string `3.14` (two digits after the decimal point) would than look like this:
`Math.PI.toFixed(2)`.

*/

import io from "../../utils/io-for-pf.js";

const radius = parseFloat(io.read("> "));

const area = radius * radius * Math.PI;

io.write(area.toFixed(3));
```
### reverse_sequence
```javascript
/*
# Reverse Sequence
Write a program that reads five numbers (`int`) and
that outputs them in reverse order.

## Example:
### Input
    1
    2
    3
    4
    5

### Output:
    5
    4
    3
    2
    1
*/

import io from "../../utils/io-for-pf.js";

const number1 = parseInt(io.read("> "));
const number2 = parseInt(io.read("> "));
const number3 = parseInt(io.read("> "));
const number4 = parseInt(io.read("> "));
const number5 = parseInt(io.read("> "));

io.write(number5);
io.write(number4);
io.write(number3);
io.write(number2);
io.write(number1);
```
### product
```javascript
/*
# Product
Write a program that expects two numeric inputs from the user.
The program prints the product (result of a multiplication) on screen.
*/

import io from "../../utils/io-for-pf.js";

const number1 = parseInt(io.read("> "));
const number2 = parseInt(io.read("> "));

const product = number1 * number2;

io.write(product);
```
### sum
```javascript
/*
# Sum
Write a program that expects two numeric inputs from the user.
The program prints the sum (result of a addition) on screen.
*/

import io from "../../utils/io-for-pf.js";

const number1 = parseInt(io.read("> "));
const number2 = parseInt(io.read("> "));

const sum = number1 + number2;

io.write(sum);
```
## 🟨Selection
### check_sign
```javascript
/*
# Check Sign
Read one integer (int).
The program prints a `+` when the number is positive or zero.
The program prints a `-` when the number is negative.
*/

import io from "../../utils/io-for-pf.js";

const integer = io.read("> ");

if (integer >= 0) {
  io.write("+");
} else {
  io.write("-");
}
```
### check_sign2
```javascript
/*
# Check Sign (2)
Read one integer (int).
The program prints a `+` when the number is positive.
The program prints a `-` when the number is negative.
The program prints a `0` when the number is zero.
*/

import io from "../../utils/io-for-pf.js";

const integer = io.read("> ");

if (integer > 0) {
  io.write("+");
} else if (integer < 0) {
  io.write("-");
} else {
  io.write("0");
}
```
### circle_surface2
```javascript
/*
# Area of a disk (circle)
Write a program that reads the radius of a circle (`float`),
and computes and prints the area up to 3 digits after the decimal point.
When a negative radius is supplied, the program replies with a `?`.

**Hint:** In JavaScript you can represent π by using `Math.PI`.

**Hint:** In JavaScript you can convert a (floating point) number
to a string using `toFixed`(inverse of parseFloat). Turning π into the string
`3.14` (two digits after the decimal point) would than look like this:
`Math.PI.toFixed(2)`.

*/

import io from "../../utils/io-for-pf.js";

const radius = parseFloat(io.read("> "));

if(radius < 0) {
  io.write("?");
} else {
  const area = radius * radius * Math.PI;
  io.write(area.toFixed(3));
}
```
### odd
```javascript
/*
# Odd or Even
A number is even when it is divisible by two.
Make a program print `odd` or `even` depending on the input (`int`).

**Hint:** Use the `%`-operator.

## Examples
    > 2
    even

    > 3
    odd
*/

import io from "../../utils/io-for-pf.js";

const number = parseInt(io.read("> "));

if (number % 2 === 0) {
  io.write("even");
} else {
  io.write("odd");
}
```
### floating_point
```javascript
/*
# Oh-point-three
Write a program that takes two numbers (`float`) as input.
The program outputs `equal` if the sum of both numbers equals 0.3 or
`not equal` in the other case.

**Hint:** reflect on how a computer stores decimal numbers when
your program behaves unexpectedly.

## Examples:
    > 0.5
    > -0.2
    equal

    > 0.3
    > 0
    equal

    > 0.4
    > -0.2
    not equal

a + b = 0.3
a + b - 0.3 = 0
a + b - 0.3 < 0.001

*/

import io from "../../utils/io-for-pf.js";

const number1 = parseFloat(io.read("> "));
const number2 = parseFloat(io.read("> "));

if (number1 + number2 - 0.3 < 0.001) {
  io.write("equal");
} else {
  io.write("not equal");
}
```
### digit_swap
```javascript
/*
# Digit Swap
Read one number (`int`) as input.

If the number has exactly two digits, the program swaps both digits.
Otherwise, the number is printed as is.
The sign of the number is **always** preserved.

**Non-functional requirement:** The input is a number, do not try to convert it to a string.
**Hint:** The integer division does not exist in JavaScript.
You can simulate an integer division, however, by doing a regular (decimal)
division, and then "round the result to the floor" (naar beneden afronden).
This can be done in JavaScript using `Math.floor(x/y)`.

## Examples:
    > 1234
    1234

    > -1234
    -1234

    > -4
    -4

    > 6
    6

    > 34
    43

    > -12
    -21

    > -70
    -7
*/

import io from "../../utils/io-for-pf.js";

const number = parseInt(io.read("> "));

if (number >= 10 && number < 100) {
  io.write((number % 10) * 10 + Math.floor(number / 10));
} else if (number > -100 && number <= -10){
  io.write((number % 10) * 10 + Math.ceil(number / 10));
} else {
  io.write(number);
}
```
### check_input
```javascript
/*
# Check Input

Ask the user for one line of input.
Now let the user know if the input was a number or not.


> 123
'yes'
> test
'no'

*/

import io from "../../utils/io-for-pf.js";

const input = io.read("> ");

if (isNaN(input)) {
  io.write("no");
} else {
  io.write("yes");
}
```
## 🟨Iteration
### sum
```javascript
/*
# Sum
Keep on asking for input (`float`) until a zero is entered.
Print the sum of these (non-zero) inputs with 1 digit after the decimal point.

**Hint:** In JavaScript you can convert a (floating point) number
to a string using `toFixed`(inverse of parseFloat). Turning π into the string
`3.14` (two digits after the decimal point) would than look like this:
`Math.PI.toFixed(2)`.

## Examples:

    > 1.4
    > -2.1
    > 3.0
    > -4
    > 0
    -1.700

*/

import io from "../../utils/io-for-pf.js";

let sum = 0;
let input = parseFloat(io.read("> "));

while (input !== 0) {
  sum += input;
  input = parseFloat(io.read("> "));
}

io.write(sum.toFixed(1));
```
### count
```javascript
/*
# Sentinel
Keep on asking for input (`float`) until a zero is entered.
Count and print how many non-zero inputs you received.

Counting always results in integers. Hence, there is no need to print any digits after the decimal point.

## Example:

    > 1.4
    > -2.1
    > 3.0
    > -4
    > 0
    4

*/

import io from "../../utils/io-for-pf.js";

let input = parseFloat(io.read("> "));
let sum = 0;

while (input !== 0) {
  input = parseFloat(io.read("> "));
  sum += 1;
}

io.write(sum);

```
### average
```javascript
/*
# Average
Keep on asking for input (`float`) until a zero is entered.
Print the average of these (non-zero) inputs with 3 digits after
the decimal point.
Your program should print `no data` if the first input was a zero.

## Examples:

    > 1.4
    > -2.1
    > 3.0
    > -4
    > 0
    -0.425

    > 0
    no data

*/

import io from "../../utils/io-for-pf.js";

let sum = 0;
let count = 0;

let input = parseFloat(io.read("> "));

while (input !== 0) {
  sum += input;
  count++;
  input = parseFloat(io.read("> "));
}

if (count === 0) {
  io.write("no data");
} else {
  const average = sum / count;
  io.write(average.toFixed(3));
}
```
### all_ex
```javascript
/*
# A range of numbers (exclusive)
Ask for a positive number (``int``) and print
all numbers (line by line) from 0 through the entered number (excluded)

## Example:
    > 3
    0
    1
    2

*/

import io from "../../utils/io-for-pf.js";

const number = parseInt(io.read("> "));

for (let i = 0; i < number; i++) {
  io.write(i);
}
```
### all_in
```javascript
/*
# A range of numbers (inclusive)
Ask for a positive number (``int``) and print
all numbers (line by line) from 0 through the entered number (included)

## Example:
    > 3
    0
    1
    2
    3
*/

import io from "../../utils/io-for-pf.js";

const number = parseInt(io.read("> "));

for (let i = 0; i <= number; i ++) {
  io.write(i);
}
```
### all_in_from_one
```javascript
/*
# A range of numbers (where to start)
Ask for a positive number (``int``) and print
all numbers (line by line) from 1 through the entered number (included)

## Example:
    > 3
    1
    2
    3
*/

import io from "../../utils/io-for-pf.js";

const number = parseInt(io.read("> "));

for (let i = 0; i < number; i++) {
  io.write(i + 1);
}
```
### factorial
```javascript
/*
# Factorial
Ask for a positive number (``int``) as input and output its factorial.

The factorial of a number n is n! with n! = n * (n-1) * ... * 3 * 2 * 1

For negative numbers the factorial is not defined. In this case you can
simply print `does not compute`.
*/

import io from "../../utils/io-for-pf.js";

const input = parseInt(io.read("> "));

if (input < 0) {
  io.write("does not compute");
} else {
  let number = 1;
  for (let i = 1; i <= input; i++) {
    number *= i;
  }
  io.write(number);
}
```
### star_rectangle
```javascript
/*
# Star Rectangle
Write a program that asks for two numerical inputs (`int`): the height and
the width of a rectangle. Print such a rectangle on screen using `*`.

The program has no output if either the height or the width is negative or zero.

**NOTE:** The goal of these exercises is to practice the use and implementation of iteration
(using `while` and/or `for`). Avoid the use of built-in (string) functions such as `repeat` (or others)
as they defeat the purpose of the exercise.

## Example:
    > 4
    > 3
    ***
    ***
    ***
    ***
*/

import io from "../../utils/io-for-pf.js";

let height = parseInt(io.read("> "));
let width = parseInt(io.read("> "));

while (height <= 0 || width <= 0) {
  height = parseInt(io.read("> "));
  width = parseInt(io.read("> "));
}

for (let i = 0; i < height; i++) { 
  let lineWithStars = ""; 
  for (let k = 0; k < width; k++) {
    lineWithStars += "*";
  }
  io.write(lineWithStars);
}
```
### isosceles1
```javascript
/*
# Isosceles 1
Write a program that asks for the height of an isosceles right triangle.
This is a right triangle with the two legs
(and their corresponding angles) equal.

Print such a triangle on screen using `*`.
The triangle is left aligned and has its top on top.

Negative or zero heights are not accepted. Keep on asking for a correct
height until a positive number is entered.

**NOTE:** The goal of these exercises is to practice the use and implementation of iteration
(using `while` and/or `for`). Avoid the use of built-in (string) functions such as `repeat` (or others)
as they defeat the purpose of the exercise.

## Example
    > -3
    > 0
    > 5
    *
    **
    ***
    ****
    *****
*/

import io from "../../utils/io-for-pf.js";

let height = parseInt(io.read("> "));

while (height <= 0) {
  height = parseInt(io.read("> "));
}

let stars = "";
for (let i = 0; i < height; i++) {
  stars += "*";
  io.write(stars);
}
```
### isosceles2
```javascript
/*
# Isosceles 2
Write a program similar to "Isosceles 1".
This time the triangle is left aligned and has its top at the bottom.

**NOTE:** The goal of these exercises is to practice the use and implementation of iteration
(using `while` and/or `for`). Avoid the use of built-in (string) functions such as `repeat` (or others)
as they defeat the purpose of the exercise.

## Example
    > -3
    > 0
    > 5
    *****
    ****
    ***
    **
    *
*/
import io from "../../utils/io-for-pf.js";

let height = parseInt(io.read("> "));

while (height <= 0) {
  height = parseInt(io.read("> "));
}

const temp = height;
for (let k = 0; k < temp; k++) {
  let stars = "";
  for (let j = 0; j < height; j++) {
    stars += "*";
  }
  io.write(stars);
  height--;
}
```
### isosceles3
```javascript
/*
# Isosceles 3
Write a program similar to "Isosceles 1".
This time the triangle is right aligned and has its top at the bottom.

**NOTE:** The goal of these exercises is to practice the use and implementation of iteration
(using `while` and/or `for`). Avoid the use of built-in (string) functions such as `repeat` (or others)
as they defeat the purpose of the exercise.

## Example
    > -3
    > 0
    > 5
    *****
     ****
      ***
       **
        *
*/

import io from "../../utils/io-for-pf.js";

let height = parseInt(io.read("> "));

while (height <= 0) {
  height = parseInt(io.read("> "));
}

const temp = height;
let spaces = "";
for (let k = 0; k < temp; k++) {
  let stars = "";
  for (let j = 0; j < height; j++) {
    stars += "*";
  }
  io.write(spaces + stars);
  height--;
  spaces += " ";
}
```
### isosceles4
```javascript
/*
# Isosceles 4
Write a program similar to "Isosceles 1".
This time triangle is right aligned and has its top on top.

**NOTE:** The goal of these exercises is to practice the use and implementation of iteration
(using `while` and/or `for`). Avoid the use of built-in (string) functions such as `repeat` (or others)
as they defeat the purpose of the exercise.

## Example
    > -3
    > 0
    > 5
        *
       ** 
      *** 
     **** 
    *****
*/

import io from "../../utils/io-for-pf.js";

let height = parseInt(io.read("> "));

while (height <= 0) {
  height = parseInt(io.read("> "));
}

for(let row = 0; row < height; row++) {
  let stars = "";
  const maxStars = row + 1;
  for (let col = 0; col < maxStars; col++) {
    stars += "*";
  }
  const maxSpaces = height - maxStars;
  let spaces = "";
  for (let space = 0; space < maxSpaces; space++) {
    spaces += " ";
  }
  const line = spaces + stars;
  io.write(line);
}
```
### isosceles5
```javascript
/*
# Isosceles 5
Write a program similar to "Isosceles 2".
This time triangle is centered and has its top on top.
Watch out, not all triangles have a top with 1 star. Some have two stars.

**NOTE:** The goal of these exercises is to practice the use and implementation of iteration
(using `while` and/or `for`). Avoid the use of built-in (string) functions such as `repeat` (or others)
as they defeat the purpose of the exercise.

## Example
    > -3
    > 0
    > 5
      *
     ***
    *****

    > -3
    > 0
    > 4
     **
    ****
 */

import io from "../../utils/io-for-pf.js";

let input = parseInt(io.read("> "));

while (input <= 0) {
  input = parseInt(io.read("> "));
}

let stars;
let temp;
if (input % 2 === 0) {
  stars = 2;
  temp = Math.floor(input / 2) - 1;
} else {
  stars = 1;
  temp = Math.floor(input / 2);
}

for (let i = 0; i < Math.ceil(input / 2); i++) {
  let row = "";
  for (let j = 0; j < stars; j++) {
    row += "*";
  }
  let spaces = "";
  for (let k = 0; k < temp; k++) {
    spaces += " ";
  }
  io.write(spaces + row);
  stars += 2;
  temp -= 1;
}
```
### isosceles6
```javascript
/*
# Isosceles 6
Write a program similar to "Isosceles 5".
This time the triangle has its top at the bottom.

**NOTE:** The goal of these exercises is to practice the use and implementation of iteration
(using `while` and/or `for`). Avoid the use of built-in (string) functions such as `repeat` (or others)
as they defeat the purpose of the exercise.

## Example
    > -3
    > 0
    > 5
    *****
     ***
      *

    > -3
    > 0
    > 4
    ****
     **
*/

import io from "../../utils/io-for-pf.js";

let input = parseInt(io.read("> "));

while (input <= 0) {
  input = parseInt(io.read("> "));
}

let temp = input;
let spaces = "";
for (let i = 0; i < Math.ceil(input / 2); i++) {
  let row = "";
  for (let k = 0; k < temp; k++) {
    row += "*";
  }
  if (i > 0) {
    spaces += " ";
  }
  io.write(spaces + row);
  temp -= 2;
}
```
### euclid
```javascript
/*
# Euclid
Write a program that reads two positive integers (no need to check the input).
Print out the largest divisor that both numbers have in common
(the greatest common divisor, GCD or "grootste gemene deler")

**Hint:** use Euclid's algorithm:
    https://en.wikipedia.org/wiki/Euclidean_algorithm
    https://nl.wikipedia.org/wiki/Algoritme_van_Euclides#Het_algoritme
*/

import io from "../../utils/io-for-pf.js";

let num1 = parseInt(io.read("> "));
let num2 = parseInt(io.read("> "));

while (num2 !== 0) {
  const temp = num1 % num2;
  num1 = num2;
  num2 = temp;
}

io.write(num1);
```
### digit_swap2
```javascript
/*
# Full Digit Swap Extra
Take one integer as input.
Output the number with the digits reversed but keep the sign.
Leading zeros are not allowed.

**Hint 1:**: The integer division does not exist in JavaScript.
You can simulate an integer division, however, by doing a regular (decimal)
division, and then "round the result to the floor" (naar beneden afronden).
This can be done in JavaScript using `Math.floor(x/y)`.

**Hint 2:** Take a look at assignment 6 in topic 2. This the extended version of that
assignment.

## Examples:
    > 1234
    4321

    > -4321
    -1234

    > -700
    -7
*/

import io from "../../utils/io-for-pf.js";

const number = parseInt(io.read("> "));

if (number >= 10 && number < 100) {
  io.write((number % 10) * 10 + Math.floor(number / 10));
} else if (number > -100 && number <= -10) {
  io.write((number % 10) * 10 + Math.ceil(number / 10));
} else if (number >= 100 && number < 1000) {
  io.write((number % 10) * 100 + Math.floor((number % 100) / 10) * 10 + Math.floor(number / 100));
} else if (number > -1000 && number <= -100) {
  io.write((number % 10) * 100 + Math.ceil((number % 100) / 10) * 10 + Math.ceil(number / 100));
} else if (number >= 1000 && number < 10000) {
  io.write((number % 10) * 1000 + Math.floor((number % 100) / 10) * 100 + Math.floor((number % 1000) / 100) * 10 + Math.floor(number / 1000));
} else if (number > -10000 && number <= -1000) {
  io.write((number % 10) * 1000 + Math.ceil((number % 100) / 10) * 100 + Math.ceil((number % 1000) / 100) * 10 + Math.ceil(number / 1000));
} else {
  io.write(number);
}
```
### centered_square
```javascript
/*
# Centered Square (partial exam)

Create a JavaScript program that prints a square.
The edges should be pluses (`+`) and in the exact center,
there should be an oh (`o`).

It is only possible to place the `o` in the exact center if
the size of the square is odd. Moreover, the `o` is only visible, for sizes of 3 or higher.

Hence, keep asking for input, until it will yield a square with correctly drawn 'oh'.

**NOTE:** The goal of these exercises is to practice the use and implementation of iteration
(using `while` and/or `for`). Avoid the use of built-in (string) functions such as `repeat` (or others)
as they defeat the purpose of the exercise.

These are the three smallest possible squares:
> 3
+++
+o+
+++

> 5
+++++
+   +
+ o +
+   +
+++++

> 7
+++++++
+     +
+     +
+  o  +
+     +
+     +
+++++++
*/

import io from "../../utils/io-for-pf.js";

let input = parseInt(io.read("> "));

while (input < 3 || input % 2 === 0) {
  input = parseInt(io.read("> "));
}

let firstLine = "";
for (let j = 0; j < input; j++) {
  line += "+";
}
io.write(firstLine);

for (let j = 0; j < Math.floor(input / 2 - 1); j++) {
  let spaces = "";
  for (let i = 0; i < input - 2; i++) {
    spaces += " ";
  }
  io.write("+" + spaces + "+");
}

let middlespaces = "";
for (let j = 0; j < Math.floor(input / 2 - 1); j++) {
  middlespaces += " ";
}
io.write("+" + middlespaces + "o" + middlespaces + "+");

for (let j = 0; j < Math.floor(input / 2 - 1); j++) {
  let spaces = "";
  for (let i = 0; i < input - 2; i++) {
    spaces += " ";
  }
  io.write("+" + spaces + "+");
}

let lastLine = "";
for (let j = 0; j < input; j++) {
  line += "+";
}
io.write(lastLine);
```
### square_of_numbers
```javascript
/*
# Square of numbers (exam second session)
Write a program that takes a number as input.
The number must be between 2 and 9 (two limits included),
if not, the program prints `No Output`.
Otherwise, the program can get to work: it prints a square of numbers:

The first row are just the numbers 1 through the entered number.
The second row contains all the doubles, ...
the last row starts with the entered number and contains all the n-multiples.

Below is the largest possible output, i.e., for 9:

`
  1  2  3  4  5  6  7  8  9
  2  4  6  8 10 12 14 16 18
  3  6  9 12 15 18 21 24 27
  4  8 12 16 20 24 28 32 36
  5 10 15 20 25 30 35 40 45
  6 12 18 24 30 36 42 48 54
  7 14 21 28 35 42 49 56 63
  8 16 24 32 40 48 56 64 72
  9 18 27 36 45 54 63 72 81
`

Make sure your output prints in a nice square,
you do this by preceding each number with spaces if necessary.
You can also do this in the first column if you like.

**Tip:** you know that 81 is the largest value you will
ever have to print and so all the numbers will consist of 1 or 2 digits.

**Side note:** By the end of the semester,
we expect you to use functions to solve this problem.
For now, make it without function and revisit the
exercise after the fall break.
*/

import io from "../../utils/io-for-pf.js";

const input = parseInt(io.read("> "));

if (input < 2 || input > 9) {
  io.write("No Output");
} else {
  for (let i = 1; i <= input; i++) {
    let numString = "";
    for (let j = 1; j <= input; j++) {
      if (j > 1 && i >= 5 || j > 2 && i >= 4 || j > 3 && i >= 3 || j > 4 && i >= 2) {
        numString += " " + (i * j);
      } else {
        numString += "  " + (i * j);
      }
    }
    io.write(numString);
  }
}
```
## 🟨Lists
### reverse_sequence
```javascript
/*
# Reverse sequence
Write a program that asks for 100 numerical inputs and
outputs them in reverse order.
*/

import io from "../../utils/io-for-pf.js";

const arr = [];

for (let i = 0; i < 100; i++) {
  arr[99 - i] = parseInt(io.read("> "));
}

for (let i = 0; i < arr.length; i++) {
  io.write(arr[i]);
}
```
### highest frequency
```javascript
/*
# Highest frequency (I)
Write a program that asks for numerical input (integers)
between 0 and 99 (both bounds inclusive).
When the user inputs a number outside this interval
the program stops asking input.

Finally, print the number that was entered the most.
You can print -1 if there was no valid input.
If multiple numbers apply, print the smallest.

# Hint 1: you can make use of the size of the interval
# Hint 2: you can make an array a priory instead of on the fly

## Example
    > 3
    > 2
    > 1
    > 3
    > 5
    > 3
    > 1
    > -10
    3

    > 1
    > 3
    > 2
    > 1
    > 3
    > 5
    > 3
    > 1
    > 678
    1

    > 123
    -1
*/

import io from "../../utils/io-for-pf.js";

let input = parseInt(io.read("> "));

if (input < 0 || input > 99) {
  io.write("-1");
} else {
  const arr = [input];
  let i = 0;
  while (input >= 0 && input <= 99) {
    input = parseInt(io.read("> "));
    i++;
    arr[i] = input;
  }

  const counts = new Array(100).fill(null);

  for (let j = 0; j < arr.length; j++) {
    counts[arr[j]] += 1;
  }

  let maxCount = 0;
  let mostFrequent;

  for (let k = 0; k < 100; k++) {
    if (counts[k] > maxCount) {
      maxCount = counts[k];
      mostFrequent = k;
    }
  }

  io.write(mostFrequent);
}
```
### highest frequency2
```javascript
/*
# Highest frequency (II)
Write a program that asks for numerical input (integers)
between 0 and 99.
When the user inputs a number outside this interval
the program stops asking input.

Finally, print the number that was entered the most.
You can print -1 if there was no valid input.
If multiple numbers apply, print the largest.

    > 3
    > 2
    > 1
    > 3
    > 5
    > 3
    > 1
    > -10
    3

    > 1
    > 3
    > 2
    > 1
    > 3
    > 5
    > 3
    > 1
    > 678
    3

    > 123
    -1
*/

import io from "../../utils/io-for-pf.js";

let input = parseInt(io.read("> "));

if (input < 0 || input > 99) {
  io.write("-1");
} else {
  const arr = [input];
  let i = 0;
  while (input >= 0 && input <= 99) {
    input = parseInt(io.read("> "));
    i++;
    arr[i] = input;
  }

  const counts = new Array(100).fill(null);

  for (let j = 0; j < arr.length; j++) {
    counts[arr[j]] += 1;
  }

  let maxCount = 0;
  let mostFrequent;

  for (let k = 99; k >= 0; k--) {
    if (counts[k] > maxCount) {
      maxCount = counts[k];
      mostFrequent = k;
    }
  }

  io.write(mostFrequent);
}
```
### highest frequency3
```javascript
/*
# Highest frequency (II)
Write a program that asks for numerical input (integers)
between 0 and 99.
When the user inputs a number outside this interval
the program stops asking input.

Finally, print the number that was entered the most.
You can print -1 if there was no valid input.
Print all numbers that apply (small to large).

## Examples:

    > 3
    > 2
    > 1
    > 3
    > 5
    > 3
    > 1
    > -10
    3

    > 1
    > 3
    > 2
    > 1
    > 3
    > 5
    > 3
    > 1
    > 678
    1
    3

    > 123
    -1
*/

import io from "../../utils/io-for-pf.js";

let input = parseInt(io.read("> "));

if (input < 0 || input > 99) {
  io.write("-1");
} else {
  const arr = [input];
  let i = 0;
  while (input >= 0 && input <= 99) {
    input = parseInt(io.read("> "));
    i++;
    arr[i] = input;
  }

  const counts = new Array(100).fill(null);

  for (let j = 0; j < arr.length; j++) {
    counts[arr[j]] += 1;
  }

  let maxCount = 0;
  for (let k = 0; k < 100; k++) {
    if (counts[k] > maxCount) {
      maxCount = counts[k];
    }
  }

  for (let k = 0; k < 100; k++) {
    if (counts[k] === maxCount) {
      io.write(k);
    }
  }
}
```
### count_sort
```javascript
/*
# Count sort
Write a program that asks for numerical input (integers) between 0 and 99.
When the user inputs a number outside this interval
the program stops asking input.

Print all the numbers that where entered, from small to large.
Numbers that were entered multiple times, however, are only printed once.

## Example
    > 3
    > 2
    > 1
    > 3
    > 5
    > 3
    > 1
    > -10
    1
    2
    3
    5
*/

import io from "../../utils/io-for-pf.js";

let input = 1;
const arr = [];
let i = 0;

while (input > 0 && input < 99) {
  input = parseInt(io.read("> "));
  i++;
  arr[i] = input;
}

const result = [];
for (let n = 0; n <= 99; n++) {
  for (let j = 0; j < arr.length; j++) {
    if (arr[j] === n) {
      let exists = 0;
      for (let k = 0; k < result.length; k++) {
        if (result[k] === n) {
          exists++;
        }
      }
      if (exists === 0) {
        result[result.length] = n;
      }
    }
  }
}

for (let j = 0; j < result.length; j++) {
  io.write(result[j]);
}
```
### count_sort2
```javascript
/*
# Count sort
Write a program that asks for numerical input (integers) between 0 and 99.
When the user inputs a number outside this interval
the program stops asking input.

Finally, print all the number that where entered from small to large.
Numbers that were entered multiple times are printed multiple times.

## Example
    > 3
    > 2
    > 1
    > 3
    > 5
    > 3
    > 1
    > -10
    1
    1
    2
    3
    3
    3
    5
*/

import io from "../../utils/io-for-pf.js";

let input = 1;
const arr = [];
let i = 0;

while (input > 0 && input < 99) {
  input = parseInt(io.read("> "));
  i++;
  arr[i] = input;
}

const result = [];
for (let n = 0; n <= 99; n++) {
  for (let j = 0; j < arr.length; j++) {
    if (arr[j] === n) {
      result[result.length] = n;
    }
  }
}

for (let j = 0; j < result.length; j++) {
  io.write(result[j]);
}
```
### eratosthenes
```javascript
/*
# Sieve of Eratosthenes
Write a program that expects a positive integer as input.
This input is the upper bound.
Then, the program prints all prime numbers below that upper bound.
If the upper bound is a prime number itself, it should also be printed in the list.

**Hint 1:** Look up "Sieve of Eratosthenes" and implement this algorithm.
**Hint 2:** Skip this exercise if you have other exercises left to make.

    > 14
    2
    3
    5
    7
    11
    13
*/

import io from "../../utils/io-for-pf.js";

let input = parseInt(io.read("> "));

while (input < 0) {
  input = parseInt(io.read("> "));
}

const numberArray = [];
const primeArray = [];
let currentCheck = 2;

for (let i = 0; i < input; i++) {
  numberArray[i] = i + 1;
  primeArray[i] = numberArray[i];
}

for (let i = 1; i < input; i++) {
  for (let j = 1; j < input; j++) {
    if (primeArray[j] % currentCheck === 0 && primeArray[j] !== currentCheck) {
      primeArray[j] = null;
    }
  }
  currentCheck++;
  if (primeArray[i] !== null ) {
    io.write(primeArray[i]);
  }
}
```
### battleship
```javascript
/*
# Battleship (partial exam)
Battleship (zeeslag) is a pen-and-paper game played on a field of 10 by 10.
Variables `a` and `b` contain such a field, which is represented in JavaScript as
an array of arrays.

Variable `a` contains the field on which all vessels are marked:
-  `_` implies empty, no vessel;
- a single letter implies a part of vessel;
- no other content is possible.

Variable `b` contains the field on which all attacks are marked:
-  `_` implies no attacks recorded;
- the letter 'x' implies successful attack;
- the letter 'o' implies failed attack;
- no other content is possible.

Write a program that computes two ratios:
- **Damage**: what amount of the fleets has been hit
    (the number of successful attacks divided by
    the total number of vessel(parts));
- **Efficiency**: what amount of the attacks was successful
    (number of successful attacks divided by total number of attacks);

Your programs should print these two ratios. Take a look at the tests to see what the formatting
should look like.

Example output:
Damage: 0.50
Efficiency: 0.50

Preparation:
- Read the given code in `assignment08_battleship_given_code.js`.
- Import at least the two fields `a` and `b` from that file, you can also import the string constants A, B, X, O if needed:
import { a, b, A, B, X, O} from "./assignment08_battleship_given_code.js";
*/

import io from "../../utils/io-for-pf.js";
import { a, b, A, B, X, O} from "./assignment08_battleship_given_code.js";

let successfulAttacks = 0;
let totalAttacks = 0;
let vessels = 0;
for (let i = 0; i < b.length; i++) {
  for (let j = 0; j < b[i].length; j++) {
    if (b[i][j] === X) {
      successfulAttacks++;
      totalAttacks++;
    } else if (b[i][j] === O) {
      totalAttacks++;
    }
    if (a[i][j] === A || a[i][j] === B) {
      vessels++;
    }
  }
}

const damage = successfulAttacks / vessels;
const efficiency = successfulAttacks / totalAttacks;

io.write("Damage: " + damage.toFixed(2));
io.write("Efficiency: " + efficiency.toFixed(2));
```
### battleship_given_code
```javascript
/*
This is not an assignment, but 'given code' for the assignment in `assignment08_battleship.js`.
*/

const _ = null;
const A = "A";
const B = "B";
const X = "x";
const O = "o";

const a = [
  [_, A, _, _, _, _, _, _, _, _],
  [_, _, A, _, _, _, _, _, _, _],
  [_, _, _, _, _, _, _, _, B, _],
  [_, _, _, _, _, _, _, _, B, _],
  [_, _, _, _, _, _, _, _, B, _],
  [_, _, _, _, _, _, _, _, _, _],
  [_, _, _, _, _, _, _, _, _, _],
  [_, _, _, _, _, _, _, _, _, _],
  [_, _, _, _, _, _, _, _, _, _],
  [_, _, _, _, _, _, _, _, _, _]
];
const b = [
  [_, _, _, _, _, _, _, _, _, _],
  [_, _, X, _, _, _, _, _, _, _],
  [_, _, _, _, _, _, _, _, _, _],
  [_, _, _, _, _, _, _, _, _, _],
  [_, _, _, _, O, _, _, _, _, _],
  [_, _, _, _, _, _, _, _, _, _],
  [_, _, _, _, _, _, _, _, _, _],
  [_, O, _, _, _, _, _, _, _, _],
  [_, _, _, _, _, _, _, _, _, _],
  [_, _, _, _, _, _, _, _, _, _]
];

export { a, b, A, B, X, O};
```
## 🟨Allround
### sentinel_extreme
```javascript
/*
# Sentinel Extreme
Keep on asking for input (`int`) until a zero is entered.
Finally, print both the smallest and the largest number
that was entered (zero does not count).

If no numbers were entered (only zero), you should print two zeros.

## Example:
    > -1
    > -2
    > 0
    -2
    -1
*/

import io from "../../utils/io-for-pf.js";

let input = parseInt(io.read("> "));

const numbers = [input];
let i = 0;

while (input !== 0) {
  input = parseInt(io.read("> "));
  i++;
  numbers[i] = input;
}

let smallest = numbers[0];
let largest = numbers[0];

for (let j = 0; j < numbers.length - 1; j++) {
  if (numbers[j] < smallest) {
    smallest = numbers[j];
  }
  if (numbers[j] > largest) {
    largest = numbers[j];
  }
}

io.write(smallest);
io.write(largest);
```
### factorial2
```javascript
/*
  # Factorial (II)
  Ask for a number (`int`) as input and output its factorial.

  The factorial of a number n is n! with n! = n * (n-1) * ... * 3 * 2 * 1
  Your program should print `does not compute` when a negative number is entered.
  */

import io from "../../utils/io-for-pf.js";

const input = parseInt(io.read("> "));

if (input < 0) {
  io.write("does not compute");
} else {
  const arr = [];
  let counter = 2;
  let result = 1;
  for (let i = 0; i < input - 1; i++) {
    arr[i] = counter;
    counter++;
    result *= arr[i];
  }
  io.write(result);
}
```
### factorial3
```javascript
/*
# Factorial (III)
Ask for a number (`int`) as input and output its factorial.
Your program should keep on asking for input until a
positive number is entered.

## Example:
    > -6
    > -3
    > 4
    24
*/

import io from "../../utils/io-for-pf.js";

let input = parseInt(io.read("> "));

while (input < 0) {
  input = parseInt(io.read("> "));
}

const arr = [];
let counter = 2;
let result = 1;

for (let i = 0; i < input - 1; i++) {
  arr[i] = counter;
  counter++;
  result *= arr[i];
}

io.write(result);
```
### variation
```javascript
/*
# K-permutations of n (Dutch: "Variation")

K-permutations of n is number of possible ways to we select k unique
element from a set of size n, and we preserve order.
This number can be computed using the following formula:

(n)k = n! // (n-k)!

 Where n! means faculty of n.

Write a program that asks for such and k and n and computes the number
of k-permutations of n.
If either n or k is negative, your program should print ``does not compute```

EXTRA REQUIREMENT: You should minimize the number of computations,
otherwise the program will be to slow for large numbers.
If your program is too slow, the tests will fail.
*/

import io from "../../utils/io-for-pf.js";

const k = parseInt(io.read("> "));
const n = parseInt(io.read("> "));

if (k < 0 || n < 0){
  io.write("does not compute");
} else if (n < k) {
  io.write(0);
} else {
  let result = n;
  let temp = n - 1;
  for (let i = 1; i < k; i++) {
    result *= temp;
    temp--;
  }
  io.write(result);
}
```
### sentinel_extreme_pro
```javascript
/*
# Sentinel Extreme Pro
Keep on asking for input (`int`) until a zero is
entered or when 10 numbers have been entered.
Finally, print both the smallest and the largest
number that was entered (zero does not count).

If no numbers were entered (only zero), you should print two zeros.
*/

import io from "../../utils/io-for-pf.js";

let input = parseInt(io.read("> "));

const numbers = [input];
let i = 0;

while (input !== 0 && i < 9) {
  input = parseInt(io.read("> "));
  i++;
  numbers[i] = input;
}

if (numbers.length > 1 && numbers[numbers.length - 1] === 0) {
  numbers.pop();
}

let smallest = numbers[0];
let largest = numbers[0];

for (let j = 0; j < numbers.length; j++) {
  if (numbers[j] < smallest) {
    smallest = numbers[j];
  }
  if (numbers[j] > largest) {
    largest = numbers[j];
  }
}

io.write(smallest);
io.write(largest);
```
### sentinel_armageddon with arrays
```javascript
/*
# Sentinel Armageddon
Keep on asking for input (`int`) until a zero is entered or when
10 numbers have been entered. Finally, print *the index* of both
the smallest and the largest number that was entered (zero does not count).
The index of the first number is 1, the index of the second is 2, ...

Try not to use an array.

If no numbers were entered (only zero), you should print two zeros.
*/

import io from "../../utils/io-for-pf.js";

let input = parseInt(io.read("> "));
if (input === 0) {
  io.write(0);
  io.write(0);
} else {
  const numbers = [input];
  let i = 0;

  while (input !== 0 && i < 9) {
    input = parseInt(io.read("> "));
    i++;
    numbers[i] = input;
  }

  if (numbers.length > 1 && numbers[numbers.length - 1] === 0) {
    numbers.pop();
  }

  let smallest = numbers[0];
  let largest = numbers[0];
  let indexOfSmallest = 0;
  let indexOfLargest = 0;

  for (let j = 0; j < numbers.length; j++) {
    if (numbers[j] < smallest) {
      smallest = numbers[j];
      indexOfSmallest = j;
    }
    if (numbers[j] > largest) {
      largest = numbers[j];
      indexOfLargest = j;
    }
  }

  io.write(indexOfSmallest + 1);
  io.write(indexOfLargest + 1);
}
```
### sentinel_armageddon without arrays
```javascript
/*
# Sentinel Armageddon
Keep on asking for input (`int`) until a zero is entered or when
10 numbers have been entered. Finally, print *the index* of both
the smallest and the largest number that was entered (zero does not count).
The index of the first number is 1, the index of the second is 2, ...

Try not to use an array.

If no numbers were entered (only zero), you should print two zeros.
*/

import io from "../../utils/io-for-pf.js";

let input = parseInt(io.read("> "));

if (input === 0) {
  io.write(0);
  io.write(0);
} else {
  let smallest = input;
  let largest = input;
  let indexOfSmallest = 1;
  let indexOfLargest = 1;
  let count = 1;

  while (input !== 0 && count < 10) {
    input = parseInt(io.read("> "));
    count++;

    if (input !== 0) {
      if (input < smallest) {
        smallest = input;
        indexOfSmallest = count;
      }
      if (input > largest) {
        largest = input;
        indexOfLargest = count;
      }
    }
  }

  io.write(indexOfSmallest);
  io.write(indexOfLargest);
}
```
## de
### de-demo
```javascript
// Plaats deze file in de (nieuwe) map "de" in de map "exercises".
// Plaats de test file in de "test" map, naast de andere test files.

/*

Voor deze opgave zijn de tussenresultaten even belangrijk als het eindresultaat.
Ook als het efficiënter zou zijn om twee delen in één keer te doen, volg de opgave en
implementeer de delen apart.

# Deel 1: de invoer
Schrijf een programma dat aan de gebruiker geheel getal vraagt tussen de 1 en de 5.
Maak een array dat even lang als het gegeven getal, gevuld met nullen.
Geeft een gebruiker een getal in buiten dit interval of een niet-getal,
maak je zo een array van lengte 5.
Print deze array ook af.

Voorbeelden:
> 3
[0, 0, 0]

> 0
[0, 0, 0, 0, 0]

> stop
[0, 0, 0, 0, 0]

# Deel 2: de verwerking

**Vervang** nu in de array alle nullen door de letters van de string `"abcde"` (in volgorde, voor zover er plaats is).

**Belangrijk:** In de opgave staat *vervang*, je moet dus de originele array aanpassen en, je mag geen nieuwe array maken die de originele vervangt.

Voorbeeld uitvoer:
["a", "b", "c"]
["a", "b", "c", "d", "e"]
["a", "b", "c", "d", "e"]


# Deel 3: de uitvoer

Vraag de gebruiker om een getal op te geven.
Print "het zoveelste element" (human count) uit deze array af.
Als de positie niet bestaat, druk dan "Ongeldige positie" af.

Voorbeeld :
> 2
b

Voorbeeld 2:
> 0
Ongeldige positie

Voorbeeld 3:
> vier
Ongeldige positie

 */

import io from "../../utils/io-for-pf.js";

const size = parseInt(io.read("Give a number between 1 and 5: "));
let arr;

if (size < 1 || size > 5 || isNaN(size)) {
  arr = new Array(5).fill(0);
  io.write(arr);
} else {
  arr = new Array(size).fill(0);
  io.write(arr);
}

const string = "abcde";
for (let i = 0; i < arr.length; i++) {
  arr[i] = string[i];
}
io.write(arr);

const index = parseInt(io.read("Give a number: "));

if (index > 0 && index <= arr.length) {
  io.write(arr[index - 1]);
} else {
  io.write("Ongeldige positie");
}
```
