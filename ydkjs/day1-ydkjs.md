# you don't know js book - Day 1

## Up & Going - ch 1: into programming

Learning programming doesn't have to be a complex and overwhelming process. There are just a few basic concepts you need to wrap your head around.

These act like building blocks. To build a tall tower, you start first by putting block on top of block on top of block. The same goes with programming. Here are some of the essential programming building blocks:

---

### Code

-   Statements
-   Expressions
-   Executing a Program

### Try It Yourself

use <shift> + <enter> to move to the next new line. Once you hit <enter> by itself, the console will run everything you've just typed.
I prefer to do this by typing about:blank into the address bar
https://blog.teamtreehouse.com/mastering-developer-tools-console

-   output
    alert and console.log
-   input
    prompt

### Operators

you only need to declare a variable once for each scope
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators

### Values & Types

Values that are included directly in the source code are called literals.

-   Converting Between Types
    Using Number(..) (a built-in function) as shown is an explicit coercion from any other type to the number type.

### Code Comments

```js
var a = /* arbitrary value */ 42;
```

### Variables

JavaScript variables as constants are usually capitalized, with underscores \_ between multiple words.

toFixed(..) lets us specify how many decimal places we'd like the number rounded to, and it produces the string as necessary.

### Blocks

a block statement does not need a semicolon (;) to conclude it.

### Conditionals

### Loops

"loop until a condition fails" concept

### Functions

Functions are often used for code that you plan to call multiple times, but they can also be useful just to organize related bits of code into named collections, even if you only plan to call them once.

-   Scope
    a scope can be nested inside another scope, just like if a clown at a birthday party blows up one balloon inside another balloon.
    If one scope is nested inside another, code inside the innermost scope can access variables from either scope.

### Practice

answer to the exercise:

```js
const TAX_RATE = 0.09;
const PHONE_PRICE = 66;
const ACCESSORY_PRICE = 7;
const SPENDING_TRESHOLD = 200;

var bank_balance = Number(prompt("enter your bank balance")); //enter 150 or 170
var amount = 0;

function calculateTax(amount) {
	return (amount = amount * TAX_RATE);
}

function formatAmount(amount) {
	return (amount = "$" + amount.toFixed(2));
}

while (amount < bank_balance) {
	amount = amount + PHONE_PRICE;
	if (amount < SPENDING_TRESHOLD) {
		amount = amount + ACCESSORY_PRICE;
	}
}

amount = amount + calculateTax(amount);

console.log("purchase amount: " + formatAmount(amount));

if (amount > bank_balance) {
	console.log("cant afford the purchase :(");
}
```

---

## original practice with answer

-   Write a program to calculate the total price of your phone purchase. You will keep purchasing phones (hint: loop!) until you run out of money in your bank account. You'll also buy accessories for each phone as long as your purchase amount is below your mental spending threshold.
-   After you've calculated your purchase amount, add in the tax, then print out the calculated purchase amount, properly formatted.
-   Finally, check the amount against your bank account balance to see if you can afford it or not.
-   You should set up some constants for the "tax rate," "phone price," "accessory price," and "spending threshold," as well as a variable for your "bank account balance.""
-   You should define functions for calculating the tax and for formatting the price with a "$" and rounding to two decimal places.
-   **Bonus Challenge:** Try to incorporate input into this program, perhaps with the `prompt(..)` covered in "Input" earlier. You may prompt the user for their bank account

Here's my JavaScript solution for this exercise:

```js
const SPENDING_THRESHOLD = 200;
const TAX_RATE = 0.08;
const PHONE_PRICE = 99.99;
const ACCESSORY_PRICE = 9.99;

var bank_balance = 303.91;
var amount = 0;

function calculateTax(amount) {
	return amount * TAX_RATE;
}

function formatAmount(amount) {
	return "$" + amount.toFixed( 2 );
}

// keep buying phones while you still have money
while (amount < bank_balance) {
	// buy a new phone!
	amount = amount + PHONE_PRICE;

	// can we afford the accessory?
	if (amount < SPENDING_THRESHOLD) {
		amount = amount + ACCESSORY_PRICE;
	}
}

// don't forget to pay the government, too
amount = amount + calculateTax( amount );

console.log(
	"Your purchase: " + formatAmount( amount )
);
// Your purchase: $334.76

// can you actually afford this purchase?
if (amount > bank_balance) {
	console.log(
		"You can't afford this purchase. :("
	);
}
// You can't afford this purchase. :(
```