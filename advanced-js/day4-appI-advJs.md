# Advanced js - Day 4

## Appx I - Vid 9

-   objects

    -   objects index is not numbers, they are string keys
    -   so that array and object are both Object types with differrent key names

    ```js
    var user = {
    	name: "moba",
    	age: 24,
    };
    user.name; // --> "moba"
    user.age = 25; // --> 25 -- age --> 25
    user.isMarried = false; // --> false -- isMarried --> false (added to user)
    user.shout = function () {
    	console.log("AHHH");
    };
    // shout is a method of user
    user.shout(); // "AHHH"
    ```

    ```js
    // console is also an Object with multiple methods
    console; // log its properties
    console.error("err"); // logs an error
    ```

    ```js
    // objects could declare empty
    emptyArr = [];
    emptyObj = {};
    // or null -- another js type
    nullObj = null;
    emptyArr[0]; //undefined
    emptyObject.name; // undefined
    nullObj.name; // error

    emptyObj.name = "moba"; // "moba"
    nullObj.name = "moba"; // error
    ```

---

## Appx I - Vid 10

-   facebook like clone - version 1

```js
var database = [
	{
		username: "moba",
		password: "secret",
	},
];

var newsFeed = [
	{
		username: "baQ",
		timeline: "javascripts sucks",
	},
	{
		username: "mia",
		timeline: "programming sucks",
	},
];

var usernamePrompt = prompt("what is your username");
var passwordPrompt = prompt("what is your password");

function signIn(user, pass) {
	if (user === database[0].username && pass === database[0].password) {
		console.log(newsFeed);
	} else {
		alert("wrong auth data");
	}
}

signIn(usernamePrompt, passwordPrompt);
```

---

## Appx I - Vid 11

-   js recap up to now

    ```js
    // - function declaration
    function funcName() {}

    // - function expression
    // notice the semicolon
    // could be named or ananymous
    var funcExp = function () {};

    // - expression
    //  is something that returns a vlue
    1 + 3;
    var a = 2;
    return true;

    // - calling or invoking a function
    alert();
    funcName(param);

    // - assign a variable
    var a = true;

    // - functions vs methods
    // ways to call differs
    function thisIsAFunction() {}
    var obj = {
    	thisIsAMethod: function () {},
    };
    thisIsAFunction();
    obj.thisIsAMethod();
    ```
