# Advanced js - Day 5

## Appx I - Vid 12

-   loops
    -   loops to the repeatitive things
        -   for example adding ! at the end of array elements

```js
var todos = [
	"to Bs project",
	"learn js",
	"study for konkur",
	"do web projects",
];
// adds ! at each str ending
for (var i = 1; i < todos.length; i++) {
	todos[i] = todos[i] + "!";
}
// remove from end until become []
// needs length to be stored before, so loop works well
var todosLength = todos.length;
for (var i = 1; i < todosLength; i++) {
	todos.pop();
}
```

```js
// while is another type of loop
var counter = 0;
while (counter > 0) {
	console.log(counter);
	counter++;
}
```

```js
// do while runs the first iteration without checking the condition
var counter = 10;
do {
	console.log(counter);
	counter--;
} while (counter > 0);
```

```js
// another type of for that is easier
// takes each el & index in a function and process them
todos.forEach(function (todo, index) {
	console.log(todo, index);
});

// it is good to separate the function and make forEach reusable
function logTodo(todo, index) {
	console.log(todo, index);
}
// for todos or any other array do the same thing
todos.forEach(logTodo);
anotherArray.forEach(logTodo);

// check canisuse.com to check that browser supports forEach
```

---

## Appx I - Vid 13

-   facebook like clone - version 2

```js
var database = [
	{
		username: "moba",
		password: "secret",
	},
	//adding more users
	{
		username: "mia",
		password: "miasecret",
	},
	{
		username: "mana",
		password: "manasecret",
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

// loop through db and search if the user & pass is valid
function userIsValid(user, pass) {
	for (var i = 1; i < database.length; i++) {
		if (user === database[i].username && pass === database[i].password) {
			return true;
		}
	}
	return false;
}
// check user & pass to show the newsfeed
function signIn(user, pass) {
	if (userIsValid(user, pass)) {
		console.log(newsFeed);
	} else {
		alert("wrong auth data");
	}
}

signIn(usernamePrompt, passwordPrompt);
```

---

## Appx I - Vid 14
- keywords
    - js has reserved keywords that are not usable for anything else (like var names)
        - ex. `var if = 1` is an error